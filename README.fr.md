# (le) logiciel malveillant bananasquad/funcaptcha
> notez que le logiciel malveillant de bananasquad est heureusement obsolète !!!

**Hachure SHA256 actuelle (de chaque logiciel) :**
| Nom du fichier | SHA256 | 
| -------- | -------- |
| pl.py (=bananasquad) (OBSOLÈTE)  | [```d278063c3acc2c145e154f039b94bb36a70d249671deac3ab9df189209b92339```](https://www.virustotal.com/gui/file/d278063c3acc2c145e154f039b94bb36a70d249671deac3ab9df189209b92339)    |
| gruppe.py (=funcaptcha)    | [```41000461584d35c3a691d6f86457639189d22b852db3c7565d5410a413521b79```](https://www.virustotal.com/gui/file/41000461584d35c3a691d6f86457639189d22b852db3c7565d5410a413521b79)     |
***
``(PS: An english version is available (README.md))``
> [!NOTE]  
> Ce fichier ne contient que les étapes à suivre pour supprimer le logiciel malveillant. Les comptes signalés comme diffusant le logiciel malveillant sur GitHub se trouvent dans le fichier ACCOUNTS.md. Merci !

> [!WARNING]
> Je ne suis pas responsable de quelconque problème que vous pourriez rencontrer. Vous pouvez me contacter sur Discord (voir mon profil) ou sur GitHub si vous avez besoin d'aide. Enfin, comme le logiciel malveillant peut continuer à évoluer, ce guide peut être obsolète quelques temps après que je l'ai publié. Mais je continuerai à enquêter sur le logiciel malveillant ; ne vous inquiétez pas !

## Message de précaution
Même si ce guide a pour but de supprimer le logiciel malveillant de votre ordinateur, c'est aussi un bon point d'entrée pour vous avertir des précautions que **vous DEVRIEZ prendre**.
> Prenez toujours un peu de recul lorsque vous téléchargez quelque chose et ne téléchargez pas trop vite, même s'il s'agit d'un logiciel libre ; êtes-vous sûr qu'il ne contient aucun comportement suspect ? Veuillez TOUJOURS vérifier les lignes du code, si vous le pouvez. Par exemple, si vous trouvez quelque chose comme ceci ``exec(Fernet(b'<quelque chose>').decrypt(b'<quelque chose>))`` dans le code, il s'agit probablement de Bananasquad/Funcaptcha.<br><br>Egalement, **N'ENREGISTREZ AUCUN IDENTIFIANTS SUR VOTRE NAVIGATEUR INTERNET.** C'est le moyen le plus facile pour un logiciel malveillant comme celui-ci de **s'emparer de n'importe quel identifiant (tant que vous les avez enregistrés).**

## Étapes pour retirer le logiciel malveillant
Pour l'instant, je me contenterai de donner des instructions (manuelles) pour supprimer le logiciel malveillant Bananasquad/Funcaptcha. Je ferai un programme qui fera ces étapes lui-même plus tard.
1. Si l'un de ces programmes est installé sur votre ordinateur :
- Discord
- Exodus Wallet
- Atomic Wallet
- BetterDiscord

veuillez les réinstaller à l'aide des sites web officiels :
- https://discord.com/
- https://www.exodus.com/
- https://atomicwallet.io/
- https://betterdiscord.app
2. Dans l'invite de commandes, avec les permissions Administrateur, faites les commandes suivantes:
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
Ces commandes vont :
- supprimer le programme HVNC (renommé hakabonk ou RuntimeBroker). Ce programme est utilisé pour contrôler votre PC sans vous avertir.
- supprimer le programme qui exécute le programme HVNC.
- supprimer les exclusions de Windows Defender, pour les fichiers [.]exe et [.]dll et le disque C:\\.
- supprimer tous les dossiers et fichiers du répertoire Temp (dans ce dossier se trouve un fichier de base de données contenant tous vos identifiants lorsque vous avez été infecté par le logiciel malveillant).

3. Toujours dans cette fenêtre CMD, exécutez ``notepad.exe C:\Windows\System32\drivers\etc\hosts``. Vous arriverez à une fenêtre de fichier. En bas du fichier, ajoutez **CES** lignes :
```
0.0.0.0 bananasquad.ru
0.0.0.0 funcaptcha.ru
0.0.0.0 1312stealer.ru
0.0.0.0 kleinanzeigen.ru
```
et enregistrez le fichier. Cela empêchera à votre PC de faire des requêtes au domaine bananasquad.ru. Vous pouvez également bloquer les requêtes vers transfer.sh (```0.0.0.0 transfer.sh```) qui transfère vos identifiants vers leur serveur.


Si vous le pouvez, bloquez ces requêtes précises :
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

4. CHANGEZ TOUS VOS IDENTIFIANTS ET EFFACEZ TOUT CE QUI PEUT L'ÊTRE DE VOTRE NAVIGATEUR (LES IDENTIFIANTS ENREGISTRÉS DANS VOTRE NAVIGATEUR PAR EXEMPLE)
5. Et voilà !
