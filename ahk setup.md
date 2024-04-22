```bash
#Persistent
SetTimer, CheckArch, 5000 ; Check every 5 seconds
return

CheckArch:
If ProcessExist("arch.exe")
{
    Menu, Tray, Icon, C:\Users\ragha\Downloads\arch.ico ; Path to your arch icon
    TrayTip, Arch Status, arch.exe is running, 2
}
Else
{
    Menu, Tray, Icon, C:\Users\ragha\Downloads\narch2.ico ; Icon for no arch
    TrayTip, Arch Status, arch.exe is not running, 2
    return  ; Added return statement to exit the function when arch.exe is not running
}
return

ProcessExist(ProcessName)
{
    Process, Exist, %ProcessName%
    return ErrorLevel
}

```