# Windows Help & Notes

## CRLF Warning 

This is GitBash telling you that git is helping.  Windows uses two characters for a new line `CR` (cariage return) and `LF` (line feed).
Classic Mac Operating system used the `CR` character.  Unix-like systems (including MacOS X) use only the `LF` character. 
If you try to open a file on Windows that has only `LF` characters, Windows will think it's all one line. To help you, 
since git knows people collaborate across file systems, when you check out files from the git database (`.git/` directory)
git replaces `LF` characters with `CRLF` before updating your working directory. 

When working on Windows, when you make a file locally, each new line will have `CRLF` in it. If your collaborator
(or server, eg GitHub) runs not a unix or linux based operating system (it almost certainly does) these extra 
characters will make a mess and make the system interpret your code wrong. To help you out, 
git will automatically, for Windows users, convert `CRLF` to `LF` when it adds
your work to the index (staging area). Then when you push, it's the compatible version. 

[git documentation of the feature](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration#Formatting-and-Whitespace) 


## Jupyter Book - Issues During or After Installation

1. **Check Python Installation**:  
   Run `python --version`. If it shows a version, continue. If not, install Python from https://www.python.org/downloads/
   If you get a "Permission Denied" message, see the "Adding Permissions" section below
   If you know python is installed, see the "Checking Paths" section below

3. **Install Jupyter Book**:  
   Ensure Jupyter Book is installed using `pip install -U jupyter-book`.
   If `jupyter-book --version` returns then "command not found," see "Checking Paths" below
   If you get a "Permission Denied" message, see the "Adding Permissions" section below

5. **Check Installation Errors**:  
   If there were no errors during installation, skip to Step 4.  
   If there were errors with a path (e.g., missing "Scripts" folder), see the "Checking Path" section.

6. **Check for Directory**:
   Ensure the following directories exist:
   (Can check through File Explorer or through terminal)
   ```
   C:\Users\[YOUR USERNAME]\AppData\Roaming\Python\Python[VERSION#]\
   C:\Users\[YOUR USERNAME]\AppData\Roaming\Python\Python[VERSION#]\Scripts\
   ```
   If it does, move on
   If not, ensure that Python was installed correctly from the website download, NOT the Windows Store 

8. **Final Troubleshooting**:  
   If issues persist, contact your Professor or TA for help! :)

### Checking Paths
If you get a `Command Not Found` message when trying to run `python` or `pip`, most likely your environment variable paths missing.
First ensure the following directories exist:
(Can check through File Explorer or through terminal)
```
C:\Users\[YOUR USERNAME]\AppData\Roaming\Python\Python[VERSION#]\
C:\Users\[YOUR USERNAME]\AppData\Roaming\Python\Python[VERSION#]\Scripts\
```
If they do, there are two methods to ensuring the path variables exist and adding them if not:

**Method 1**
1. Go to your taskbar Search
2. Search for and open "Edit the system environment variables"
3. Click "Environment Variables..." in the window that opened
4. Click "Path" line then "Edit..."

**Method 2**
1. Press `Windows + R`, type `sysdm.cpl`, and press Enter.
2. Go to the **Advanced** tab → **Environment Variables**.
3. Add the path containing the "Scripts" folder to the `Path` variable. Save and exit.
4. Reopen Git Bash and try `jupyter-book --version`. If it works, you're done!  
   - If "Access denied" occurs, try `sudo jupyter-book --version`. Windows Defender may prompt you to unlock the file. After unlocking, try the command again.
  
### Adding Permissions
If you get a `Permission Denied` message when trying to run commands, Windows Security is blocking it.
- If you get a pop-up notification when trying to run a command, simply click "unblock" each time
- If you don't get a pop-up notif, follow the steps below to add an exclusion for Python
1. Go to your taskbar Search
2. Search for and open "Windows Security"
3. Go to the "Virus & threat protection" section on the left
4. Under "Virus & threat protection settings" click "manage settings"
5. Scroll down to the "Exclusions" section and click "Add or remove exclusions"
6. Click "Add an exclusion", then "Folder"
7. Find and select the folder Python installed in
   - Should be `C:\Users\[YOUR USERNAME]\AppData\Roaming\Python\`
