# bananasquad/funcaptcha malware
> note that the bananasquad malware is now fortunately outdated!!!

**Current SHA256 hash (of each malware):**
| File name | SHA256 | 
| -------- | -------- |
| pl.py (=bananasquad) (OUTDATED)   |  [```d278063c3acc2c145e154f039b94bb36a70d249671deac3ab9df189209b92339```](https://www.virustotal.com/gui/file/d278063c3acc2c145e154f039b94bb36a70d249671deac3ab9df189209b92339)     |
| gruppe.py (=funcaptcha)    | [```41000461584d35c3a691d6f86457639189d22b852db3c7565d5410a413521b79```](https://www.virustotal.com/gui/file/41000461584d35c3a691d6f86457639189d22b852db3c7565d5410a413521b79)     |
***
``(PS: Une version en français est disponible (README.fr.md))``
> [!NOTE]  
> This file only contains the steps on how to remove the malware. Accounts that are reported to be spreading malware on GitHub are in the ACCOUNTS.md file. Thanks! 

> [!WARNING]
> I am not responsible for any kind of problem that you might have. You can either contact me on Discord (check my profile) or on GitHub if you want some help. Finally, as the malware can continue to evolve, this guide might be outdated a few times after I've posted it. But I will keep investigating the malware; don't worry!

## Precaution message
Even if this guide is to remove the malware from your computer, it is also a good entry point for me to warn you about precautions that **you SHOULD have**.

> Always take a step back when you're downloading something and don't download too fast even if it is open source; Are you sure that it does not contain any kind of suspicious behavior? PLEASE always check the lines of the code, if you can. For example, if you find something like this ``exec(Fernet(b'<something>').decrypt(b'<something>'))`` in the code, it's likely to be Bananasquad/Funcaptcha.<br><br>And also, **DON'T SAVE ANY CREDENTIALS ON YOUR BROWSER.** This is the easiest way for a malware like this to **grab any credentials (as long as you've saved them).**

## Steps to remove the malware
For the moment, I will only put (manual) instructions to remove the Bananasquad/Funcaptcha malware. I will make a program that does these steps itself later on.
1. If you've got one of these programs installed on your computer:
- Discord
- Exodus Wallet
- Atomic Wallet
- BetterDiscord

please reinstall them with the official websites:
- https://discord.com/
- https://www.exodus.com/
- https://atomicwallet.io/
- https://betterdiscord.app
2. On CMD, with Administrator permissions, do:
```
del %appdata%\gruppe_storage
del %temp%\RuntimeBroker.exe
del %temp%\RuntimeBroker2.exe
del %temp%\hakabonk.exe
del %appdata%\Microsoft\runpython.py
del "%appdata%\Microsoft\Windows\Start Menu\Programs\Startup\hvnc.py"
rmdir /S /Q C:\Windows\WinEmptyfold
powershell.exe -Command "Remove-MpPreference -ExclusionExtension '.exe'"
powershell.exe -Command "Remove-MpPreference -ExclusionExtension '.dll'"
powershell.exe -Command "Remove-MpPreference -ExclusionExtension 'exe'"
powershell.exe -Command "Remove-MpPreference -ExclusionExtension 'dll'"
powershell.exe -Command "Remove-MpPreference -ExclusionPath 'C:'"
del %temp%\*
```
These commands will:
- delete the backdoor HVNC program (renamed as hakabonk or RuntimeBroker). This program is used to control your PC without warning you.
- delete the program that runs the HVNC one.
- remove the exclusions of Windows Defender, for [.]exe and [.]dll files and the C:\ disk.
- delete all the folders and files from the Temp directory (you've got a database file with your all your credentials when you've been infected by the malware, in this folder).

3. Always on this CMD window, run ``notepad.exe C:\Windows\System32\drivers\etc\hosts``. You will arrive to a file window. At the bottom of the file, add **THESE** lines:
```
0.0.0.0 bananasquad.ru
0.0.0.0 funcaptcha.ru
0.0.0.0 1312stealer.ru
0.0.0.0 kleinanzeigen.ru
``` 
and save the file. This will prevent your PC from making requests to the bananasquad.ru domain. You can also block requests to transfer.sh (```0.0.0.0 transfer.sh```) that transfers your credentials to their server.

If you can, block those precise requests:
- http://bananasquad.ru/paste
- http://bananasquad.ru/handler
- http://bananasquad.ru/hvnc.py
- http://bananasquad.ru/hvnc.exe
- http://bananasquad.ru/app.asar
- http://bananasquad.ru/atomic/app.asar
- http://bananasquad.ru/newwallethandler
- http://bananasquad.ru/delivery
- http://funcaptcha.ru/paste
- http://funcaptcha.ru/paste2
- http://funcaptcha.ru/delivery
- http://funcaptcha.ru/hvnc.py
- http://funcaptcha.ru/hvnc.exe
- http://funcaptcha.ru/newwallethandler
- http://1312stealer.ru/paste
- http://1312stealer.ru/paste2
- http://1312stealer.ru/delivery
- http://1312stealer.ru/hvnc.py
- http://1312stealer.ru/hvnc.exe
- http://1312stealer.ru/newwallethandler
- http://kleinanzeigen.ru/paste
- http://kleinanzeigen.ru/paste2
- http://kleinanzeigen.ru/delivery
- http://kleinanzeigen.ru/hvnc.py
- http://kleinanzeigen.ru/hvnc.exe
- http://kleinanzeigen.ru/newwallethandler
- http://kleinanzeigen.ru/delivery
- http://kleinanzeigen.ru/miner.exe



4. CHANGE ALL YOUR CREDENTIALS AND CLEAR ANYTHING POSSIBLE FROM YOUR BROWSER (CREDENTIALS THAT ARE SAVED IN YOUR BROWSER FOR EXAMPLE)
5. And voilà!
