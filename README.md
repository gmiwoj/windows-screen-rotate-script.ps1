## windows-screen-rotate-script.ps1

Windows Powershell / .NET script

Powershell script to flip screen orientation horizontal / vertical quick and easy with command or shortcut icon. Because switching between vertical and horizontal using Display settings on windows takes too many clicks.

Works with multiple monitors and all display orientation modes (landscape, landscape inverted, portrait, portrait inverted).






![preview2](https://support.content.office.net/en-us/media/96e92630-bbfe-4292-bbfc-fbb4a4908c8e.png)
![preview2](https://www.tenforums.com/attachments/tutorials/268002d1582491524-how-change-display-orientation-windows-10-a-display_orientation.png)





**usage examples (as commands or as shortcuts) :**

switch second screen to portrait (vertical counter clockwise) :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-screen-rotate-script.ps1" 1 270`

switch second screen to portrait inverted (vertical clockwise) :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-screen-rotate-script.ps1" 1 90`

switch second screen back to landscape (horizontal) :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-screen-rotate-script.ps1" 1 0`



**needs 2 arguments! :**
- argument 1 : display id (0: first main screen, 1: second screen, 2: third etc.)
- argument 2 : rotation angle (0: default landscape, 90: portrait inverted, 180: landscape inverted, 270: portrait. can only rotate by 90 in one go for some reason, cant go from 0 straight to 180)

so :

- `... "windows-screen-rotate-script.ps1" 0 270` means first primary display, 90 degrees ccw (vertical)
- `... "windows-screen-rotate-script.ps1" 1 90`  means second display, 90 degrees cw (vertical inverted)




**disclaimer :**

i didn't write 90% this code myself, i barely know how it works. i just mashed various pieces of code that worked for me, that i found here and there, and modified some parts to my needs.
