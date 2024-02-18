# bananasquad malware
For the moment, I will only put (manual) instructions to remove the Bananasquad malware. I will make a program that does these steps itself later on.

## DISCLAIMER
I am not responsible for any kind of problem that you might have. 

You can either contact me on Discord (check my profile) or on GitHub if you want some help.

Finally, as the malware can continue to evolve, this guide might be outdated in few times after I've posted it. But I will keep investigating the malware, don't worry! 

1. If you've got one of these programs installed on your computer:
- Discord
- Exodus Wallet
- Atomic Wallet
- BetterDiscord
<br><br>please reinstall them with the official websites:
- https://discord.com/
- https://www.exodus.com/
- https://atomicwallet.io/
- https://betterdiscord.app
2. On CMD, with Administrator permissions, do:
```
del %temp%\hakabonk.exe
del %appdata%\Microsoft\runpython.py
rmdir /S /Q C:\Windows\WinEmptyfold
powershell.exe -Command "Remove-MpPreference -ExclusionExtension '.exe'"
powershell.exe -Command "Remove-MpPreference -ExclusionExtension '.dll'"
powershell.exe -Command "Remove-MpPreference -ExclusionExtension 'exe'"
powershell.exe -Command "Remove-MpPreference -ExclusionExtension 'dll'"
powershell.exe -Command "Remove-MpPreference -ExclusionPath 'C:'"
del %temp%\*
```
3. Always on this CMD window, run ``notepad.exe C:\Windows\System32\drivers\etc\hosts``. You will arrive to a file window. At the bottom of the line, add this line:
```0.0.0.0     bananasquad.ru``` and save the file. This will prevent your PC to make requests in the bananasquad.ru domain.
4. CHANGE ALL YOUR CREDENTIALS.
5. And voilà!