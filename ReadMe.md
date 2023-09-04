# Quickstart

## Schritt 1:

```powershell
# if using scoop
scoop bucket add extras
scoop install whkd
scoop install komorebi

# if using winget
winget install LGUG2Z.whkd
winget install LGUG2Z.komorebi

# save the example configuration to ~/komorebi.json
iwr https://raw.githubusercontent.com/LGUG2Z/komorebi/master/komorebi.example.json -OutFile $Env:USERPROFILE\komorebi.json

# save the latest generated app-specific config tweaks and fixes
komorebic fetch-app-specific-configuration

# ensure the ~/.config folder exists
mkdir $Env:USERPROFILE\.config -ea 0

# save the sample whkdrc file with key bindings to ~/.config/whkdrc
iwr https://raw.githubusercontent.com/LGUG2Z/komorebi/master/whkdrc.sample -OutFile $Env:USERPROFILE\.config\whkdrc

# start komorebi and whkd
komorebic start -c $Env:USERPROFILE\komorebi.json --whkd
```

## Schritt 2:

Überschreibe Files mit aktuellen Files.


## Schritt 3:

Erstelle einen Task

Programm : powershell
Argumente : -File "C:\Users\<Username>\komorebi_start.ps1" -WindowStyle Hidden
