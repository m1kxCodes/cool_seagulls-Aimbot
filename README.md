print("hey nerd btw can you join the discord if something broke? | https://discord.gg/wWQ9RKAkqg")
-- no skidding allowed ninja
local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
local RunService = game:GetService("RunService")
local UIS = game:GetService("UserInputService")
local Camera = workspace.CurrentCamera

local aimbotKeybind = Enum.KeyCode.E -- Default key (change as needed)
local predictionEnabled = true
local targetBodyPart = "Head" -- Default body part to aim at
local smoothAiming = true
local smoothFactor = 0.1 -- Aiming speed factor (0.1 = very smooth)
local triggerbotEnabled = false
local isAimbotActive = false
local bhopEnabled = false -- New Bhop option
local selectedOption = 1 -- Current option in the GUI
local options = { "Aimbot Keybind", "Prediction", "Body Part", "Smooth Aiming", "Triggerbot", "Target Priority", "Bhop" }
local bodyParts = { "Head", "Torso", "HumanoidRootPart" }
local targetPriorities = { "Closest to Mouse", "Closest to Player", "Lowest Health", "Open Players" }
local selectedBodyPart = 1 -- Current selected body part
local selectedPriority = 1 -- Current selected target priority
local guiVisible = true -- Toggle for the GUI visibility
local changingKeybind = false -- Track if we are waiting for keybind input
local aimKeyHeld = false -- Track if the aim key is held down

local screenGui = Instance.new("ScreenGui", player.PlayerGui)
screenGui.Name = "AimbotGui"
screenGui.ResetOnSpawn = false

local frame = Instance.new("Frame", screenGui)
frame.Size = UDim2.new(0, 200, 0, 210)
frame.Position = UDim2.new(0.2, 0, 0.3, -80)
frame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)

local titleLabel = Instance.new("TextLabel", frame)
titleLabel.Text = "cool_seagull's Universal Aimbot"
titleLabel.Size = UDim2.new(1, 0, 0, 25)
titleLabel.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
titleLabel.TextColor3 = Color3.fromRGB(0, 255, 255)
titleLabel.TextScaled = true
titleLabel.Font = Enum.Font.SourceSansBold

local optionLabels = {}
for i, option in ipairs(options) do
    local label = Instance.new("TextLabel", frame)
    label.Text = option
    label.Size = UDim2.new(1, 0, 0, 20)
    label.Position = UDim2.new(0, 0, 0, 25 + 25 * i)
    label.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
    label.TextColor3 = Color3.fromRGB(255, 255, 255)
    label.TextXAlignment = Enum.TextXAlignment.Left
    label.Font = Enum.Font.SourceSans
    label.TextScaled = true
    optionLabels[i] = label
end

local function updateGui()
    for i, label in ipairs(optionLabels) do
        label.BackgroundColor3 = (i == selectedOption) and Color3.fromRGB(80, 80, 80) or Color3.fromRGB(50, 50, 50)

        if i == 1 then
            label.Text = "Aimbot Keybind: " .. tostring(aimbotKeybind.Name)
        elseif i == 2 then
            label.Text = "Prediction: " .. (predictionEnabled and "On" or "Off")
            label.TextColor3 = predictionEnabled and Color3.fromRGB(0, 255, 0) or Color3.fromRGB(255, 0, 0)
        elseif i == 3 then
            label.Text = "Body Part: " .. bodyParts[selectedBodyPart]
        elseif i == 4 then
            label.Text = "Smooth Aiming: " .. (smoothAiming and "On" or "Off")
            label.TextColor3 = smoothAiming and Color3.fromRGB(0, 255, 0) or Color3.fromRGB(255, 0, 0)
        elseif i == 5 then
            label.Text = "Triggerbot: " .. (triggerbotEnabled and "On" or "Off")
            label.TextColor3 = triggerbotEnabled and Color3.fromRGB(0, 255, 0) or Color3.fromRGB(255, 0, 0)
        elseif i == 6 then
            label.Text = "Target Priority: " .. targetPriorities[selectedPriority]
        elseif i == 7 then
            label.Text = "Bhop: " .. (bhopEnabled and "On" or "Off")
            label.TextColor3 = bhopEnabled and Color3.fromRGB(0, 255, 0) or Color3.fromRGB(255, 0, 0)
        end
    end
end

updateGui()

-- Bhop function
local function bhop()
    local humanoid = player.Character and player.Character:FindFirstChild("Humanoid")
    local humanoidRootPart = player.Character and player.Character:FindFirstChild("HumanoidRootPart")
    if bhopEnabled and humanoid and humanoidRootPart then
        -- Check if the player is on the ground
        if humanoid:GetState() == Enum.HumanoidStateType.Freefall or humanoid:GetState() == Enum.HumanoidStateType.Jumping then
            -- Do not jump if the player is in the air
            return
        end
        humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
    end
end


local function smoothAimAt(targetPosition)
    local aimDirection = (targetPosition - Camera.CFrame.Position).unit
    local newCFrame = CFrame.new(Camera.CFrame.Position, Camera.CFrame.Position + aimDirection)
    Camera.CFrame = smoothAiming and Camera.CFrame:Lerp(newCFrame, smoothFactor) or newCFrame
end

local function getPredictedPosition(target, predictionTime)
    if target and target.Character and target.Character:FindFirstChild("HumanoidRootPart") then
        local targetPosition = target.Character.HumanoidRootPart.Position
        local targetVelocity = target.Character.HumanoidRootPart.Velocity
        return targetPosition + (targetVelocity * predictionTime)
    end
    return nil
end

local function isValidTarget(target)
    local humanoid = target.Character:FindFirstChild("Humanoid")
    local forcefield = target.Character:FindFirstChildOfClass("ForceField")
    return humanoid and humanoid.Health > 0 and not forcefield
end

local function isTargetOpen(target)
    local character = target.Character
    if character and character:FindFirstChild("HumanoidRootPart") then
        local startPos = Camera.CFrame.Position
        local endPos = character.HumanoidRootPart.Position
        local ray = Ray.new(startPos, (endPos - startPos).unit * (endPos - startPos).magnitude)
        local hit, _ = workspace:FindPartOnRay(ray, player.Character)
        return hit and hit:IsDescendantOf(character)
    end
    return false
end

local function aimAt(target)
    if target and target.Character and target.Character:FindFirstChild(targetBodyPart) and isValidTarget(target) then
        local predictionTime = predictionEnabled and 0.1 or 0
        local bodyPart = target.Character:FindFirstChild(targetBodyPart)

        if bodyPart then
            local targetPosition = bodyPart.Position
            if predictionEnabled then
                targetPosition = getPredictedPosition(target, predictionTime)
            end
            if targetPosition then
                smoothAimAt(targetPosition)
            end
        end
    end
end

local function triggerbot()
    if triggerbotEnabled and mouse.Target and mouse.Target.Parent then
        local targetPlayer = game.Players:GetPlayerFromCharacter(mouse.Target.Parent)
        if targetPlayer and isValidTarget(targetPlayer) then
            mouse1click() -- Automatically fire when the crosshair is on the target
        end
    end
end

local function findBestTarget()
    local bestTarget = nil
    local bestValue = math.huge
    local openTargets = {}

    for _, targetPlayer in pairs(game.Players:GetPlayers()) do
        if targetPlayer ~= player and isValidTarget(targetPlayer) and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
            local value
            if targetPriorities[selectedPriority] == "Open Players" then
                if isTargetOpen(targetPlayer) then
                    table.insert(openTargets, targetPlayer)
                end
            elseif targetPriorities[selectedPriority] == "Closest to Mouse" then
                local screenPoint = Camera:WorldToScreenPoint(targetPlayer.Character.HumanoidRootPart.Position)
                value = (Vector2.new(screenPoint.X, screenPoint.Y) - Vector2.new(mouse.X, mouse.Y)).magnitude
            elseif targetPriorities[selectedPriority] == "Closest to Player" then
                value = (Camera.CFrame.Position - targetPlayer.Character.HumanoidRootPart.Position).magnitude
            elseif targetPriorities[selectedPriority] == "Lowest Health" then
                value = targetPlayer.Character.Humanoid.Health
            end

            if value and value < bestValue then
                bestValue = value
                bestTarget = targetPlayer
            end
        end
    end

    if selectedPriority == 4 and #openTargets > 0 then
        for _, target in pairs(openTargets) do
            local screenPoint = Camera:WorldToScreenPoint(target.Character.HumanoidRootPart.Position)
            local distToMouse = (Vector2.new(screenPoint.X, screenPoint.Y) - Vector2.new(mouse.X, mouse.Y)).magnitude
            if distToMouse < bestValue then
                bestTarget = target
                bestValue = distToMouse
            end
        end
    end

    return bestTarget
end

-- Input handling
UIS.InputBegan:Connect(function(input, gameProcessedEvent)
    if not gameProcessedEvent then
        if changingKeybind then
            if input.UserInputType == Enum.UserInputType.Keyboard then
                aimbotKeybind = input.KeyCode
                changingKeybind = false
                updateGui()
            end
        else
            if input.KeyCode == Enum.KeyCode.Up then
                selectedOption = (selectedOption - 1 < 1) and #options or selectedOption - 1
                updateGui()
            elseif input.KeyCode == Enum.KeyCode.Down then
                selectedOption = (selectedOption + 1 > #options) and 1 or selectedOption + 1
                updateGui()
            elseif input.KeyCode == Enum.KeyCode.Return then
                if selectedOption == 1 then
                    changingKeybind = true
                    optionLabels[1].Text = "Press any key..."
                elseif selectedOption == 2 then
                    predictionEnabled = not predictionEnabled
                elseif selectedOption == 3 then
                    selectedBodyPart = (selectedBodyPart % #bodyParts) + 1
                    targetBodyPart = bodyParts[selectedBodyPart]
                elseif selectedOption == 4 then
                    smoothAiming = not smoothAiming
                elseif selectedOption == 5 then
                    triggerbotEnabled = not triggerbotEnabled
                elseif selectedOption == 6 then
                    selectedPriority = (selectedPriority % #targetPriorities) + 1
                elseif selectedOption == 7 then
                    bhopEnabled = not bhopEnabled
                end
                updateGui()
            elseif input.KeyCode == Enum.KeyCode.Insert then
                guiVisible = not guiVisible -- Toggle the GUI visibility
                frame.Visible = guiVisible
            end
        end
    end
end)

RunService.RenderStepped:Connect(function()
    if UIS:IsKeyDown(aimbotKeybind) then
        isAimbotActive = true

        local target = findBestTarget()
        if target then
            aimAt(target)
        end
    else
        isAimbotActive = false
    end

    if triggerbotEnabled then
        triggerbot()
    end

    bhop()
end)

print("executed cool-seagull aimbot succesfully")
