
# Folder-lock-without-software

<h2>Introduction</h2>
<p>You can easily lock any folder on your Windows computer with a simple Notepad hack. By creating a batch file, you can hide a folder and require a password be entered before it becomes visible and accessible. This is a great tool for locking sensitive information, like pictures, financial statements, and a lot more.<br><br>This trick will work on just about any version of the operating system, including Windows 10, Windows 7, Windows XP, Windows 98, and so on.</p>

<h3><b>Step 1: Open Notepad</b></h3>
Start by opening Notepad, either from search, the Start Menu, or simply right-click inside a folder, then choose New -> Text Document.<br><img src="https://github.com/thelegendavanish/Folder-lock-without-software/assets/107942286/1bc0576f-ff89-495e-95b4-e0cf03b5b465" width="800" height="400"><br>

<h3><b>Step 2: Add Code to Document</b></h3>
Now just copy the text below and paste it into your document.

```bash
  @ECHO OFF
if EXIST "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" goto UNLOCK
if NOT EXIST Private goto MDPrivate
:CONFIRM
echo Are you sure to lock this folder? (Y/N)
set/p "cho=>"
if %cho%==Y goto LOCK
if %cho%==y goto LOCK
if %cho%==n goto END
if %cho%==N goto END
echo Invalid choice.
goto CONFIRM
:LOCK
ren Private "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
attrib +h +s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
echo Folder locked
goto End
:UNLOCK
echo Enter password to Unlock Your Secure Folder
set/p "pass=>"
if NOT %pass%== 123 FAIL
attrib -h -s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
ren "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" Private
echo Folder Unlocked successfully
goto End
:FAIL
echo Invalid password
goto end
:MDPrivate
md Private
echo Private created successfully
goto End
:End
```
<h3><b>Step 3: Edit Folder Name & Password</b></h3>
With the text pasted in, you can adjust the locked folder's name, as well as the password used to unlock it. The default folder name is "Private" and the default password is "123"<img src= "https://github.com/thelegendavanish/Folder-lock-without-software/assets/107942286/a952820d-4da1-437d-a6d5-def861901d1f" width="800" height="400"><br>

<h3><b>Step 4:Save Batch File</b></h3>
Now save the file as whatever name you'd like, but make sure the name ends in ".bat" and that you select "All files" in the drop-down box when saving. Also, if you opened Notepad directly rather than using the right-click, be sure to adjust your save location accordingly.<img src= "https://github.com/thelegendavanish/Folder-lock-without-software/assets/107942286/2f53235f-ec6c-405b-8314-b848aaeb487e" width="800" height="400"><br><br>Once saved, your file should look like this in the folder you choose:
<img src= "https://github.com/thelegendavanish/Folder-lock-without-software/assets/107942286/5803bc1d-0d2d-4fd4-9e74-375617261271" width="600" height="100"><br>


<h3><b>Step 5:Create Folder</b></h3>
Now double-click on the batch file you just created (or select and hit Enter). You'll notice a new folder come up.<img src= "https://github.com/thelegendavanish/Folder-lock-without-software/assets/107942286/8bad7f46-93f2-4421-860c-e80ebded72ee" width="600" height="100">

<h3><b>Step 6:Lock the Folder</b></h3>
Once you're ready to lock the folder, simply double-click on the batch file (or select and hit Enter), then choose 'y' on the window that pops up and hit Enter.<img src= "https://github.com/thelegendavanish/Folder-lock-without-software/assets/107942286/3a9f3dc4-79db-4835-80f9-9593612539c1" width="600" height="200"><br><br>You'll notice that your folder has now disappeared.

<h3><b>Step 7:Access Your Hidden & Locked Folder</b></h3>
Now whenever you need access to your folder, just double-click on the batch file, input your password, and hit Enter.<img src= "https://github.com/thelegendavanish/Folder-lock-without-software/assets/107942286/de9b2460-4c1a-48ee-96b7-af38c40153fd" width="600" height="100"><br><br>To re-lock (and hide) the folder, just hit the batch file again. And remember, you can name the batch file and folder whatever you like, you feel free to make sure of this trick in multiple locations on your Windows machine.


<h2>Created By: <a href="https://thelegendavanish.tech">Thelegendavanish</a></h2>
