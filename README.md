# Zen Browser Linux Desktop Environment
This repository provides a .desktop entry and an icon for integrating the Zen Browser AppImage into Linux desktop environments.

## Files
```
zen.desktop — Desktop launcher file
zen-browser.png — Application icon
```

## Installation Steps
### Step 1 - Edit .desktop File
Open the zen.desktop file in a text editor.

You will see placeholder text like:
```
Exec=<path-to-your-AppImage-file>
```

You must replace <path-to-your-AppImage-file> with the full absolute path to where your Zen Browser AppImage is located.

**Important:**
Update all ```Exec=``` fields in the following sections:
```
[Desktop Entry]
[Desktop Action new-window]
[Desktop Action private-window]
[Desktop Action safe-mode]
```
Each Exec= line must point correctly to your Zen Browser AppImage location.

**Example:**
If your Zen Browser AppImage is saved at /home/yourusername/Applications/zen-x86_64.AppImage, then update all Exec= lines like this:
```
Exec=/home/yourusername/Applications/zen-x86_64.AppImage
Exec=/home/yourusername/Applications/zen-x86_64.AppImage --new-window
Exec=/home/yourusername/Applications/zen-x86_64.AppImage --private-window
Exec=/home/yourusername/Applications/zen-x86_64.AppImage --safe-mode
```

### Step 2 - Move .desktop and .png Files
After editing the zen.desktop file and ensuring the AppImage paths are correct:
Move the .desktop file and the icon file (.png) to the appropriate **/usr/share/applications/** directories.

**Run the following commands:**
'''sh
sudo mv zen.desktop /usr/share/applications/
sudo mv zen-browser.png /usr/share/applications/
'''

### Step 2 - Restart Your Session
After moving the .desktop and .png files to the correct locations:
-  Log out of your current desktop session.
-  Log back in.
