# windows10-classic-themes
This is a collection of themes for Windows 10 based on the Classic themes from Windows XP (minus High Contrast).
I chose the GNU AGPL because I realized some systems administrator would install this on a Remote Desktop server at some point. Because the server's filesystem can be locked down for security reasons, I wanted remote users to still be able to access the theme files and modify them directly rather than just use the Personalization settings in Windows. Placing a .ZIP file of the themes in a user-readable directory is a sufficient means of distributing the source.

This is a sister project to my Basic theme for Windows 10, which is still in the works.

As of 4/2/2018, windows10-classic-themes now features its own setup wizard created with Inno Script Studio. Its source code is located at theme-setup.iss, and a compiled version can be found in the Output directory.

# How these themes were built:
Here's a rundown of the basic steps I went through in porting these themes to Windows 10:

## Step 1: Get VirtualBox.
![VirtualBox Manager homepage.](images/step1.PNG)

## Step 2: Create a VM with Windows XP as the guest OS… ![Windows XP (WEPOS 2009) with Luna theme.](images/step2a.PNG) or in my case (due to security concerns), Windows Embedded POSReady 2009, which is one of two editions Microsoft still supports (the other is Embedded Standard 2009).
![Windows XP (WEPOS 2009) with Embedded theme.](images/step2b.PNG)

## Step 3: Create a readily accessible folder in which to store the theme files.
![Created a folder named "Classic Themes" on the desktop.](images/step3.PNG)

## Step 4: Switch to the Classic theme using Display Properties.
![Windows XP Display Properties with Windows Classic theme.](images/step4.PNG)

## Step 5: Click "Save As..." and save the current theme in the folder created previously.
The filename "standard.theme" refers to the Windows Standard color scheme.
!["Save theme" dialog in Display Properties.](images/step5a.PNG)
![The Classic Themes folder, now with standard.theme inside it.](images/step5b.PNG)

## Step 6: Switch to the "Brick" color scheme.
![Appearance tab in Display Properties.](images/step6a.PNG)
![Changed the color scheme to Brick.](images/step6b.PNG)

## Step 7: Save the Brick theme in the Classic Themes folder.
Again, the filename corresponds to the abbreviated name of the color scheme, i.e. brick.theme for "Brick", redwhiteblue.theme for "Red, White, and Blue (VGA)", and plum.theme for "Plum (high color)".
![The Themes tab again.](images/step7a.PNG)
![Saving Brick as brick.theme](images/step7b.PNG)
![So far, we've saved two color schemes.](images/step7c.PNG)

## Step 8: Repeat Steps 6 and 7 for the remaining 16-or-so color schemes.
We're purposefully omitting the 4 High Contrast ones, as those are already present in Windows 10.

## Step 9: Copy/move the folder with our theme files onto a flash drive or network folder.
![We'll be copying the themes over to flash drive E:.](images/step9a.PNG)
![And here's the Classic Themes folder on the flash drive.](images/step9b.PNG)

## Step 10: Switch the flash drive over to the host machine.
![The USB flash drive is now connected to the host.](images/step10a.PNG)
![We can now access the Classic Themes folder on the host machine.](images/step10b.PNG)

## Step 11: Copy the theme files over to a folder on the host.
![Here's all our theme files copied over to the host.](images/step11.PNG)

## Step 12: Using a text editor, modify the theme files to make them compatible with Windows 10.
I recommend Notepad++ for this, as you can open the 18 files in one window. We'll have to add details like the theme name and specify aerolite.msstyles as the visual style, as well as other sections needed for the theme to function properly. You can use the Windows 10 High Contrast theme files as reference points, or just look at the versions I've uploaded.
![Modifying standard.theme in Notepad++.](images/step12.PNG)

## Step 13: Enjoy!
![Screenshot of Windows 10 Pro with Classic theme.](images/step13.PNG)
