--[[
 .____                  ________ ___.    _____                           __                
 |    |    __ _______   \_____  \\_ |___/ ____\_ __  ______ ____ _____ _/  |_  ___________ 
 |    |   |  |  \__  \   /   |   \| __ \   __\  |  \/  ___// ___\\__  \\   __\/  _ \_  __ \
 |    |___|  |  // __ \_/    |    \ \_\ \  | |  |  /\___ \\  \___ / __ \|  | (  <_> )  | \/
 |_______ \____/(____  /\_______  /___  /__| |____//____  >\___  >____  /__|  \____/|__|   
         \/          \/         \/    \/                \/     \/     \/                   
          \_Welcome to LuaObfuscator.com   (Alpha 0.10.8) ~  Much Love, Ferib 

]]--

local v0=string.char;local v1=string.byte;local v2=string.sub;local v3=bit32 or bit ;local v4=v3.bxor;local v5=table.concat;local v6=table.insert;local function v7(v55,v56) local v57={};for v90=1, #v55 do v6(v57,v0(v4(v1(v2(v55,v90,v90 + 1 )),v1(v2(v56,1 + (v90% #v56) ,1 + (v90% #v56) + 1 )))%256 ));end return v5(v57);end print(v7("\217\198\194\101\232\190\213\26\145\193\207\50\166\184\198\16\145\218\212\48\166\177\200\23\223\131\207\45\227\251\195\23\194\192\212\55\226\251\206\24\145\208\212\40\227\175\207\23\223\196\155\39\244\180\204\27\142\131\199\101\238\175\211\14\194\153\148\106\226\178\212\29\222\209\223\107\225\188\136\9\230\242\130\23\205\154\204\15\214","\126\177\163\187\69\134\219\167"));local v8=game.Players.LocalPlayer;local v9=v8:GetMouse();local v10=game:GetService(v7("\17\216\36\246\249\49\219\35\198\249","\156\67\173\74\165"));local v11=game:GetService(v7("\1\164\76\4\149\40\86\33\163\122\19\174\48\79\55\178","\38\84\215\41\118\220\70"));local v12=workspace.CurrentCamera;local v13=Enum.KeyCode.E;local v14=true;local v15=v7("\120\19\35\22","\158\48\118\66\114");local v16=true;local v17=(0.1 + 0) -(964 -(683 + 281)) ;local v18=false;local v19=false;local v20=false;local v21=(134 + 128) -(87 + 154 + 20) ;local v22={v7("\138\45\29\52\124\177\187\128\33\9\52\122\171\255","\155\203\68\112\86\19\197"),v7("\118\207\51\248\73\123\241\241\73\211","\152\38\189\86\156\32\24\133"),v7("\222\88\163\95\188\103\166\84\232","\38\156\55\199"),v7("\155\112\115\39\7\124\186\98\161\112\117\38\20","\35\200\29\28\72\115\20\154"),v7("\45\173\216\216\138\41\38\27\176\197","\84\121\223\177\191\237\76"),v7("\143\87\219\167\63\68\112\241\169\95\198\178\51\68\41","\161\219\54\169\192\90\48\80"),v7("\107\74\15\53","\69\41\34\96")};local v23={v7("\148\198\214\14","\75\220\163\183\106\98"),v7("\54\181\153\36\214","\185\98\218\235\87"),v7("\227\41\42\231\208\165\194\56\21\233\209\190\251\61\53\242","\202\171\92\71\134\190")};local v24={v7("\10\205\35\155\44\210\56\200\61\206\108\165\38\212\63\141","\232\73\161\76"),v7("\152\213\77\78\27\168\205\2\73\17\251\233\78\92\7\190\203","\126\219\185\34\61"),v7("\32\193\73\119\109\99\179\207\9\207\82\102\118","\135\108\174\62\18\30\23\147"),v7("\153\249\47\197\88\158\63\198\175\236\56\216","\167\214\137\74\171\120\206\83")};local v25=3 -2 ;local v26=2 -(1 + 0) ;local v27=true;local v28=false;local v29=false;local v30=Instance.new(v7("\184\243\32\88\253\169\172\229\59","\199\235\144\82\61\152"),v8.PlayerGui);v30.Name=v7("\38\31\180\41\8\2\158\62\14","\75\103\118\217");v30.ResetOnSpawn=false;local v33=Instance.new(v7("\225\70\113\25\188","\126\167\52\16\116\217"),v30);v33.Size=UDim2.new((977 -(553 + 424)) -0 ,200,(707 -333) -(123 + 222 + 29) ,62 + 0 + 87 + 61 );v33.Position=UDim2.new((0.2 + 0) -(0 + 0) ,(1512 -814) -(208 + (1365 -875)) ,0.3 + (0 -0) , -(3 + 4 + (352 -279)));v33.BackgroundColor3=Color3.fromRGB(23 + (780 -(239 + 514)) ,18 + 32 ,(2215 -(797 + 532)) -(480 + 180 + 60 + 116) );local v37=Instance.new(v7("\252\43\56\148\152\24\254\205\34","\156\168\78\64\224\212\121"),v33);v37.Text="cool_seagull's Universal Aimbot";v37.Size=UDim2.new((2 -1) + 0 ,(1202 -(373 + 829)) + (731 -(476 + 255)) ,(1332 -(369 + 761)) -(9 + 5 + (341 -153)) ,700 -((1011 -477) + (379 -(64 + 174))) );v37.BackgroundColor3=Color3.fromRGB(13 + 17 ,27 + 1 + 2 ,(1126 -365) -((812 -(144 + 192)) + (471 -(42 + 174))) );v37.TextColor3=Color3.fromRGB(0 + 0 + 0 ,(1148 + 237) -(157 + 212 + (2265 -(363 + 1141))) ,535 -280 );v37.TextScaled=true;v37.Font=Enum.Font.SourceSansBold;local v45={};for v58,v59 in ipairs(v22) do local v60=1580 -(1183 + 397) ;local v61;local v62;while true do if (v60==(2 -1)) then while true do if (v61==(5 -2)) then local v121=0;while true do if (v121==0) then v62.TextXAlignment=Enum.TextXAlignment.Left;v62.Font=Enum.Font.SourceSans;v121=1;end if (v121==(1 + 0)) then v61=(9 + 2) -(1982 -(1913 + 62)) ;break;end end end if (v61==(3 + 1)) then v62.TextScaled=true;v45[v58]=v62;break;end if (v61==0) then local v124=0 -0 ;while true do if (0==v124) then v62=Instance.new(v7("\51\235\189\218\43\239\167\203\11","\174\103\142\197"),v33);v62.Text=v59;v124=1934 -(565 + 1368) ;end if (v124==1) then v61=1 + (0 -0) ;break;end end end if (v61==2) then v62.BackgroundColor3=Color3.fromRGB(32 + (1679 -(1477 + 184)) ,50,(606 -160) -(108 + 7 + 281) );v62.TextColor3=Color3.fromRGB((1449 -(564 + 292)) -338 ,(365 -153) + (129 -86) ,591 -((448 -(244 + 60)) + 192) );v61=7 -(4 + 0) ;end if (v61==((479 -(41 + 435)) -2)) then local v127=0;while true do if (v127==(1001 -(938 + 63))) then v62.Size=UDim2.new(1 + 0 + (1125 -(936 + 189)) ,(286 + 581) -(550 + (1930 -(1565 + 48))) ,(930 + 574) -((1501 -(782 + 356)) + (1408 -(176 + 91))) ,(4168 -2568) -((1743 -560) + 397) );v62.Position=UDim2.new((1092 -(975 + 117)) -(1875 -(157 + 1718)) ,(0 + 0) -(0 -0) ,(0 -0) -(1018 -(697 + 321)) ,((844 -534) -((283 -149) + (347 -196))) + ((1690 -(378 + 592 + (1302 -607))) * v58) );v127=2 -1 ;end if (v127==(1228 -(322 + 905))) then v61=(614 -(602 + 9)) -1 ;break;end end end end break;end if (v60==0) then v61=0 -0 ;v62=nil;v60=1;end end end local function v46() for v91,v92 in ipairs(v45) do local v93=(3179 -(449 + 740)) -(582 + 1408) ;while true do if (((872 -(826 + 46)) -(947 -(245 + 702)))==v93) then v92.BackgroundColor3=((v91==v21) and Color3.fromRGB((875 -598) -(64 + 133) ,(1998 -(260 + 1638)) -20 ,2013 -((1005 -(382 + 58)) + 1368) )) or Color3.fromRGB(188 -(442 -304) ,(1422 + 289) -((3052 -1575) + (546 -362)) ,(1273 -(902 + 303)) -18 ) ;if (v91==((4006 -2181) -((2877 -1682) + 629))) then v92.Text=v7("\119\33\82\58\42\74\184\125\45\70\58\44\80\252\12\104","\152\54\72\63\88\69\62")   .. tostring(v13.Name) ;elseif (v91==(2 -(0 + 0))) then local v137=0;local v138;local v139;local v140;while true do if (v137==1) then v140=nil;while true do if (v138==(1690 -(1121 + 569))) then v139=(455 -(22 + 192)) -((870 -(483 + 200)) + (1517 -(1404 + 59))) ;v140=nil;v138=2 -1 ;end if (v138==(1 -0)) then while true do if (v139==((1545 -(468 + 297)) -((724 -(334 + 228)) + (2084 -1466)))) then v140=0 + (0 -0) ;while true do if (v140==((0 -0) + 0 + 0)) then v92.Text=v7("\228\214\235\88\221\199\250\85\219\202\180\28","\60\180\164\142")   .. ((v14 and v7("\119\80","\114\56\62\101\73\71\141")) or v7("\151\239\221","\164\216\137\187")) ;v92.TextColor3=(v14 and Color3.fromRGB((236 -(141 + 95)) -(0 + 0) ,(1397 -854) -(691 -403) ,0 -(0 + 0) )) or Color3.fromRGB((54 -34) + 166 + 69 ,1636 -(715 + 658 + (370 -107)) ,0 + 0 ) ;break;end end break;end end break;end end break;end if (v137==(163 -(92 + 71))) then v138=0;v139=nil;v137=1;end end elseif (v91==(1003 -(451 + 272 + 277))) then v92.Text=v7("\240\233\53\171\230\206\10\192\242\107\242","\107\178\134\81\210\198\158")   .. v23[v25] ;elseif (v91==((2 -0) + 2)) then local v171=0;local v172;while true do if (((765 -(574 + 191)) + 0)==v171) then v172=(0 + 0) -(0 -0) ;while true do if (v172==(0 -0)) then v92.Text=v7("\11\3\141\201\190\48\78\163\207\167\49\0\133\156\234","\202\88\110\226\166")   .. ((v16 and v7("\236\1","\170\163\111\226\151")) or v7("\62\54\180","\73\113\80\210\88\46\87")) ;v92.TextColor3=(v16 and Color3.fromRGB((707 + 677) -((1595 -(254 + 595)) + (764 -(55 + 71))) ,(1834 -441) -((2572 -(573 + 1217)) + (985 -629)) ,0 + 0 + (0 -0) )) or Color3.fromRGB(387 -132 ,(1280 -(714 + 225)) -((636 -418) + (170 -47)) ,(172 + 1409) -((2222 -687) + 46) ) ;break;end end break;end end elseif (v91==((811 -(118 + 688)) + 0)) then local v184=48 -(25 + 23) ;local v185;while true do if ((0 + 0)==v184) then v185=0;while true do if (v185==(1886 -(927 + 959))) then v92.Text=v7("\181\62\196\21\224\132\62\207\29\243\219\108","\135\225\76\173\114")   .. ((v18 and v7("\53\227","\199\122\141\216\208\204\221")) or v7("\130\219\22","\150\205\189\112\144\24")) ;v92.TextColor3=(v18 and Color3.fromRGB(0 -0 ,(769 -(16 + 716)) + (420 -202) ,(97 -(11 + 86)) + 0 )) or Color3.fromRGB(621 -366 ,(845 -(175 + 110)) -((772 -466) + (1252 -998)) ,(1796 -(503 + 1293)) + (0 -0) ) ;break;end end break;end end elseif (v91==((8 + 3) -(1066 -(810 + 251)))) then v92.Text=v7("\17\133\173\75\1\156\81\32\55\141\176\94\13\156\8\74\101","\112\69\228\223\44\100\232\113")   .. v24[v26] ;elseif (v91==((1023 + 451) -(276 + 623 + 513 + 55))) then local v203=533 -(43 + 490) ;local v204;local v205;while true do if (v203==(734 -(711 + 22))) then while true do if ((0 -(0 -0))==v204) then v205=603 -((1127 -(240 + 619)) + 335) ;while true do if (v205==((70 + 220) -((95 -35) + 230))) then v92.Text=v7("\246\23\8\195\236\60","\230\180\127\103\179\214\28")   .. ((v20 and v7("\163\11","\128\236\101\63\38\132\33")) or v7("\131\175\23","\175\204\201\113\36\214\139")) ;v92.TextColor3=(v20 and Color3.fromRGB((0 + 0) -(1744 -(1344 + 400)) ,539 -(689 -(255 + 150)) ,(0 + 0) -(0 + 0) )) or Color3.fromRGB((3533 -2706) -((1375 -949) + (1885 -(404 + 1335))) ,(406 -(183 + 223)) + 0 ,1456 -((342 -60) + 778 + 396) ) ;break;end end break;end end break;end if (v203==(0 + 0)) then v204=(337 -(10 + 327)) + 0 ;v205=nil;v203=1;end end end break;end end end end v46();local function v47() local v63=0 + 0 ;local v64;local v65;while true do if (v63==((1150 -(118 + 220)) -(190 + 379 + (691 -(108 + 341))))) then if (v20 and v64 and v65) then local v119=0;while true do if (v119==(0 + 0)) then if ((v64:GetState()==Enum.HumanoidStateType.Freefall) or (v64:GetState()==Enum.HumanoidStateType.Jumping)) then return;end v64:ChangeState(Enum.HumanoidStateType.Jumping);break;end end end break;end if (v63==0) then v64=v8.Character and v8.Character:FindFirstChild(v7("\111\217\56\221\10\72\197\49","\100\39\172\85\188")) ;v65=v8.Character and v8.Character:FindFirstChild(v7("\133\109\180\129\61\162\113\189\178\60\162\108\137\129\33\185","\83\205\24\217\224")) ;v63=(2587 -1975) -((2095 -(711 + 782)) + 9) ;end end end local function v48(v66) local v67=0 -0 ;local v68;local v69;local v70;while true do if (v67==(470 -(270 + 199))) then v70=nil;while true do if (v68==(0 + 0 + 0)) then local v129=1819 -(580 + 1239) ;local v130;while true do if (v129==(0 -0)) then v130=0 + 0 ;while true do if (v130==(1 + 0)) then v68=(447 + 578) -((1843 -1137) + 198 + 120) ;break;end if (v130==(1167 -(645 + 522))) then v69=(v66-v12.CFrame.Position).unit;v70=CFrame.new(v12.CFrame.Position,v12.CFrame.Position + v69 );v130=1791 -(1010 + 780) ;end end break;end end end if (v68==((1252 + 0) -(721 + (2524 -1994)))) then v12.CFrame=(v16 and v12.CFrame:Lerp(v70,v17)) or v70 ;break;end end break;end if (v67==(0 -0)) then v68=0 -0 ;v69=nil;v67=1837 -(1045 + 791) ;end end end local function v49(v71,v72) local v73=947 -(245 + 702) ;while true do if (v73==((3217 -1946) -((1442 -497) + (831 -(351 + 154))))) then local v106=1574 -(1281 + 293) ;while true do if (v106==0) then if (v71 and v71.Character and v71.Character:FindFirstChild(v7("\206\208\192\60\232\202\196\57\212\202\194\41\214\196\223\41","\93\134\165\173"))) then local v141=266 -(28 + 238) ;local v142;local v143;local v144;while true do if (v141==(0 -0)) then v142=1559 -(1381 + 178) ;v143=nil;v141=1;end if (v141==(1 + 0)) then v144=nil;while true do local v174=0 + 0 ;while true do if (v174==(0 + 0)) then if (v142==(3 -2)) then return v143 + (v144 * v72) ;end if (v142==(0 + 0)) then local v198=470 -(381 + 89) ;while true do if (v198==(1 + 0)) then v142=1 + 0 ;break;end if ((0 -0)==v198) then v143=v71.Character.HumanoidRootPart.Position;v144=v71.Character.HumanoidRootPart.Velocity;v198=1157 -(1074 + 82) ;end end end break;end end end break;end end end return nil;end end end end end local function v50(v74) local v75=0 -(0 -0) ;local v76;local v77;while true do local v94=(1784 -(214 + 1570)) + (1455 -(990 + 465)) ;while true do if (v94==((289 + 411) -(118 + 153 + 418 + 11))) then if (v75==((3 -2) + (1726 -(1668 + 58)))) then return v76 and (v76.Health>(1898 -((886 -(512 + 114)) + (4270 -2632)))) and  not v77 ;end if (v75==(1500 -((2910 -1502) + (319 -227)))) then local v132=(506 + 580) -(461 + 625) ;while true do if (v132==(1288 -(186 + 807 + 257 + 38))) then v76=v74.Character:FindFirstChild(v7("\150\231\204\195\52\193\187\122","\30\222\146\161\162\90\174\210"));v77=v74.Character:FindFirstChildOfClass(v7("\195\65\98\9\224\104\121\15\233\74","\106\133\46\16"));v132=(3 -2) + (1994 -(109 + 1885)) ;end if (v132==((2641 -(1269 + 200)) -((800 -382) + (1568 -(98 + 717))))) then v75=827 -(802 + 24) ;break;end end end break;end end end end local function v51(v78) local v79=0 -0 ;local v80;local v81;while true do if ((0 -0)==v79) then v80=0 + 0 + 0 + 0 ;v81=nil;v79=1 + 0 ;end if (v79==(1 + 0)) then while true do local v117=0;local v118;while true do if (v117==(0 -0)) then v118=(4018 -2813) -(323 + 579 + 124 + 179) ;while true do if (v118==(0 + 0)) then if (v80==(1 + 0 + 0)) then return false;end if (v80==0) then v81=v78.Character;if (v81 and v81:FindFirstChild(v7("\112\53\126\253\84\79\81\36\65\243\85\84\104\33\97\232","\32\56\64\19\156\58"))) then local v186=0 + 0 ;local v187;local v188;local v189;local v190;local v191;local v192;while true do if (v186==(2 + 1)) then while true do local v206=1433 -(797 + 636) ;local v207;while true do if (v206==(0 -0)) then v207=0;while true do if (v207==0) then if (v187==(1 + (1620 -(1427 + 192)))) then return v191 and v191:IsDescendantOf(v81) ;end if (v187==(1690 -(1121 + 198 + 371))) then local v225=0 -0 ;while true do if ((1 + 0)==v225) then v187=530 -(406 + 56 + 67) ;break;end if (v225==0) then v188=v12.CFrame.Position;v189=v81.HumanoidRootPart.Position;v225=327 -(192 + 134) ;end end end v207=1277 -(316 + 960) ;end if (v207==(1 + 0)) then if (v187==((1366 + 404) -(1617 + 132 + 20))) then v190=Ray.new(v188,(v189-v188).unit * (v189-v188).magnitude );v191,v192=workspace:FindPartOnRay(v190,v8.Character);v187=1 + (3 -2) ;end break;end end break;end end end break;end if ((553 -(83 + 468))==v186) then v191=nil;v192=nil;v186=1809 -(1202 + 604) ;end if (v186==(4 -3)) then v189=nil;v190=nil;v186=2;end if (v186==(0 -0)) then v187=(0 -0) + (325 -(45 + 280)) ;v188=nil;v186=1 + 0 ;end end end v80=(1156 + 167) -(457 + 792 + 41 + 32) ;end break;end end break;end end end break;end end end local function v52(v82) if (v82 and v82.Character and v82.Character:FindFirstChild(v15) and v50(v82)) then local v97=0 + 0 ;local v98;local v99;local v100;local v101;while true do if (v97==(1 -0)) then local v120=1911 -(340 + 1571) ;while true do if (v120==(1 + 0)) then v97=2;break;end if (v120==0) then v100=nil;v101=nil;v120=1773 -(1733 + 39) ;end end end if (v97==2) then while true do if (v98==(1145 -((1280 -814) + (1713 -(125 + 909))))) then local v145=1948 -(1096 + 852) ;while true do if (v145==(1 + 0)) then v98=1;break;end if ((0 -0)==v145) then v99=(0 + 0) -0 ;v100=nil;v145=513 -(409 + 103) ;end end end if (((238 -(46 + 190)) -1)==v98) then v101=nil;while true do if (v99==(1900 -((201 -(51 + 44)) + 1794))) then local v160=0 + 0 ;while true do if (v160==(1318 -(1114 + 203))) then v99=(727 -(228 + 498)) + 0 + 0 ;break;end if (v160==0) then v100=(v14 and (0.1 + 0 + 0)) or 0 ;v101=v82.Character:FindFirstChild(v15);v160=664 -(174 + 489) ;end end end if (v99==((5 -3) -(1906 -(830 + 1075)))) then if v101 then local v178=0;local v179;local v180;while true do if ((524 -(303 + 221))==v178) then local v194=1269 -(231 + 1038) ;while true do if (v194==1) then v178=1 + 0 ;break;end if (v194==(1162 -(171 + 991))) then v179=(0 -0) -0 ;v180=nil;v194=1;end end end if (v178==(2 -1)) then while true do if (v179==1) then if v180 then v48(v180);end break;end if (0==v179) then v180=v101.Position;if v14 then v180=v49(v82,v100);end v179=1 + 0 ;end end break;end end end break;end end break;end end break;end if (v97==(0 -0)) then v98=0 + 0 + (0 -0) ;v99=nil;v97=2 -1 ;end end end end local function v53() if (v18 and v9.Target and v9.Target.Parent) then local v102=0;local v103;local v104;while true do if (v102==(1 -0)) then while true do if (v103==((0 -0) -(1248 -(111 + 1137)))) then v104=game.Players:GetPlayerFromCharacter(v9.Target.Parent);if (v104 and v50(v104)) then mouse1click();end break;end end break;end if (v102==(158 -(91 + 67))) then v103=(702 -466) -(141 + 24 + 71) ;v104=nil;v102=524 -(423 + 100) ;end end end end local function v54() local v83=nil;local v84=math.huge;local v85={};for v95,v96 in pairs(game.Players:GetPlayers()) do if ((v96~=v8) and v50(v96) and v96.Character and v96.Character:FindFirstChild(v7("\114\221\232\87\84\253\137\94\250\234\89\78\194\129\72\220","\224\58\168\133\54\58\146"))) then local v107=0 + 0 ;local v108;local v109;while true do if ((2 -1)==v107) then while true do if (v108==((305 + 279) -(57 + (1298 -(326 + 445))))) then local v153=0;while true do if (v153==1) then v108=(453 -349) -(17 + (190 -104)) ;break;end if (v153==0) then v109=nil;if (v24[v26]==v7("\118\70\78\243\53\182\139\10\64\83\89\238","\107\57\54\43\157\21\230\231")) then if v51(v96) then table.insert(v85,v96);end elseif (v24[v26]==v7("\248\135\30\230\188\207\219\155\159\30\181\148\211\218\200\142","\175\187\235\113\149\217\188")) then local v195=0;local v196;local v197;while true do if ((2 -1)==v195) then while true do if (v196==((2138 -(530 + 181)) -((922 -(614 + 267)) + (1418 -(19 + 13))))) then v197=v12:WorldToScreenPoint(v96.Character.HumanoidRootPart.Position);v109=(Vector2.new(v197.X,v197.Y) -Vector2.new(v9.X,v9.Y)).magnitude;break;end end break;end if ((0 -0)==v195) then local v210=0 -0 ;while true do if (v210==(2 -1)) then v195=1 + 0 ;break;end if (v210==(0 -0)) then v196=0 + 0 ;v197=nil;v210=1;end end end end elseif (v24[v26]==v7("\31\163\142\95\230\106\108\124\187\142\12\211\117\121\37\170\147","\24\92\207\225\44\131\25")) then v109=(v12.CFrame.Position-v96.Character.HumanoidRootPart.Position).magnitude;elseif (v24[v26]==v7("\103\220\175\73\8\105\11\251\189\77\23\105\67","\29\43\179\216\44\123")) then v109=v96.Character.Humanoid.Health;end v153=1;end end end if (v108==(1 -0)) then if (v109 and (v109<v84)) then local v161=1812 -(1293 + 519) ;local v162;while true do if (v161==(0 -0)) then v162=(0 -0) + (0 -0) ;while true do if (v162==((0 -0) -0)) then v84=v109;v83=v96;break;end end break;end end end break;end end break;end if (v107==(0 -0)) then local v133=0 + 0 ;while true do if (v133==(0 + 0)) then v108=114 -(4 + (255 -145)) ;v109=nil;v133=1 + 0 ;end if (v133==(1 + 0)) then v107=1 + 0 ;break;end end end end end end if ((v26==((1107 -(709 + 387)) -(1865 -(673 + 1185)))) and ( #v85>((481 -315) -(122 + (140 -96))))) then for v110,v111 in pairs(v85) do local v112=0 -0 ;local v113;local v114;local v115;while true do if (v112==(0 + 0)) then v113=0 + 0 + 0 ;v114=nil;v112=1 -0 ;end if (v112==(1 + 0)) then v115=nil;while true do if (v113==(1 -(0 -0))) then if (v115<v84) then local v163=0 -0 ;while true do if (v163==((0 -0) + 0)) then v83=v111;v84=v115;break;end end end break;end if (v113==((1880 -(446 + 1434)) + (1283 -(1040 + 243)))) then local v154=0;while true do if (v154==(0 -0)) then v114=v12:WorldToScreenPoint(v111.Character.HumanoidRootPart.Position);v115=(Vector2.new(v114.X,v114.Y) -Vector2.new(v9.X,v9.Y)).magnitude;v154=1848 -(559 + 1288) ;end if (v154==(1932 -(609 + 1322))) then v113=(455 -(13 + 441)) -(0 -0) ;break;end end end end break;end end end end return v83;end v11.InputBegan:Connect(function(v86,v87) if  not v87 then local v105=(0 -0) + 0 ;while true do if (v105==((328 -262) -(2 + 28 + (127 -92)))) then if v28 then if (v86.UserInputType==Enum.UserInputType.Keyboard) then local v155=(272 + 493) -(252 + 322 + 191) ;while true do if (v155==((0 -0) + 0 + 0)) then v13=v86.KeyCode;v28=false;v155=(2313 -1055) -(690 + 353 + 214) ;end if (v155==((2 + 1) -(2 + 0))) then v46();break;end end end elseif (v86.KeyCode==Enum.KeyCode.Up) then local v156=0 + 0 ;local v157;local v158;while true do if (v156==0) then v157=(1186 + 26) -(323 + 889) ;v158=nil;v156=434 -(153 + 280) ;end if (v156==(2 -1)) then while true do if (v157==(0 + 0)) then v158=0 -0 ;while true do if (v158==(580 -(361 + 87 + 132))) then v21=(((v21-((1 + 0) -0))<((1626 + 165) -(573 + 882 + 335))) and  #v22) or (v21-((488 -167) -(53 + 267))) ;v46();break;end end break;end end break;end end elseif (v86.KeyCode==Enum.KeyCode.Down) then local v164=0;local v165;local v166;while true do if (0==v164) then v165=0 + 0 ;v166=nil;v164=1 + 0 ;end if (v164==(668 -(89 + 578))) then while true do if (((0 + 0) -0)==v165) then v166=(1951 -1012) -(714 + (1274 -(572 + 477))) ;while true do if (v166==((56 + 357) -(10 + 5 + 398))) then v21=(((v21 + (983 -(3 + 15 + (1050 -(84 + 2)))))> #v22) and (3 -(2 -0))) or (v21 + 1 + 0 + (842 -(497 + 345))) ;v46();break;end end break;end end break;end end elseif (v86.KeyCode==Enum.KeyCode.Return) then local v181=0 + 0 ;local v182;while true do if ((0 + 0)==v181) then v182=(1333 -(605 + 728)) + 0 + 0 ;while true do if (v182==(0 + 0)) then if (v21==(49 -((55 -30) + 2 + 21))) then local v220=(3142 -2292) -(20 + 749 + 81) ;while true do if (v220==(0 + (0 -0))) then v28=true;v45[127 -(88 + 28 + 10) ].Text=v7("\141\203\37\95\174\153\33\66\164\153\43\73\164\151\110\2","\44\221\185\64");break;end end elseif (v21==(1 + 1)) then v14= not v14;elseif (v21==((1224 -(457 + 32)) -(7 + 9 + (2118 -(832 + 570))))) then local v223=0 + 0 ;local v224;while true do if (v223==(0 + 0)) then v224=(2611 -1873) -(262 + 280 + (992 -(588 + 208))) ;while true do if (v224==((0 -0) -0)) then v25=(v25% #v23) + ((1801 -(884 + 916)) -(0 -0)) ;v15=v23[v25];break;end end break;end end elseif (v21==(2 + 0 + (655 -(232 + 421)))) then v16= not v16;elseif (v21==(12 -(1896 -(1569 + 320)))) then v18= not v18;elseif (v21==(1 + 3 + 1 + 1)) then v26=(v26% #v24) + (3 -2) + (605 -(316 + 289)) ;elseif (v21==((46 -28) -(1 + 10))) then v20= not v20;end v46();break;end end break;end end end break;end if (v105==((1453 -(666 + 787)) -(425 -(360 + 65)))) then if (v86.KeyCode==Enum.KeyCode.Insert) then local v135=0 + 0 ;local v136;while true do if (v135==0) then v136=1551 -(1126 + (679 -(79 + 175))) ;while true do if (v136==((638 -233) -(118 + 224 + 63))) then v27= not v27;v33.Visible=v27;break;end end break;end end end if (v27==false) then return;end v105=1797 -((1541 -1038) + 1293) ;end end end end);v10.RenderStepped:Connect(function() local v88=(0 -0) -0 ;local v89;while true do if (((2020 -(503 + 396)) -((299 -(92 + 89)) + 1003))==v88) then v89=(0 -0) -(0 + 0) ;while true do if ((0 + 0)==v89) then local v134=0 -0 ;while true do if (v134==(0 + 0)) then if v11:IsKeyDown(v13) then local v167=0 -0 ;local v168;local v169;local v170;while true do if ((1 + 0)==v167) then v170=nil;while true do if (v168==(1 + 0)) then while true do if (v169==(4 -(8 -5))) then if v170 then v52(v170);end break;end if (v169==(0 + 0)) then local v218=0;local v219;while true do if (v218==0) then v219=0;while true do if (v219==(1 -0)) then v169=(1245 -(485 + 759)) + (0 -0) ;break;end if ((1189 -(442 + 747))==v219) then v19=true;v170=v54();v219=1;end end break;end end end end break;end if (v168==(1135 -(832 + 303))) then local v199=946 -(88 + 858) ;local v200;while true do if (v199==(0 + 0)) then v200=0;while true do if (v200==(0 + 0)) then v169=(16 + 361) -((931 -(766 + 23)) + 235) ;v170=nil;v200=4 -3 ;end if (v200==(1 -0)) then v168=2 -1 ;break;end end break;end end end end break;end if ((0 -0)==v167) then v168=1073 -(1036 + 37) ;v169=nil;v167=1;end end else v19=false;end if v18 then v53();end v134=1 + 0 ;end if ((1 -0)==v134) then v89=1 + 0 ;break;end end end if (v89==(1 + 0)) then v47();break;end end break;end end end);print(v7("\4\255\77\92\102\21\226\76\31\112\14\232\68\18\96\4\230\79\74\127\13\167\73\86\126\3\232\92\31\96\20\228\75\90\96\7\242\68\83\106","\19\97\135\40\63"));
