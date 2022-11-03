# SWTOR File Changer

Thank you for downloading the SWTOR File Changer! This tool allows you
to edit the asset files of the video game Star Wars: The Old Republic.
You can choose which files you want to replace and customize the game
as you wish.

Please note that this tool is provided under no warranty. You are free
to use this program at your own risk. Editing the asset files can cause
your game to crash or show graphical glitches. When a new patch can be
downloaded, be prepared to restore your game files to the original
version BEFORE you download the patch, otherwise your game may be broken
and you need to redownload it.

If you want to use the automatic backup feature, make sure that you have
at least 5 GB of free memory on your hard drive. Remember that you can
also store this tool on a different hard drive that has more free space.

In case you are having problems running this tool, make sure you have
Microsoft .NET 6.0 installed on your computer. You can download
it at https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-6.0.6-windows-x64-installer


## Editing the Settings.txt file
The Settings.txt file contains the list of files that should be
replaced by the tool. Each file needs to be placed on a separate line
in the following format:

```
replace /resources/path_name.dds replace_file.dds
```

Where the second part is the SWTOR path of the file you wish to
replace, and the last part contains the file that should be used to
replace the file. The three parts are separated by a single space.

If you do not know the file name, you can write the hash instead:

```
replace 0738C4CF_91905309 empty.gr2
```

Also, you can replace nodes in the Game Object Model with the following
command, where the second path is the FQN of the node:

```
replacegom abl.insert.fqn.path.here new_node.node
```

All files that you want to replace need to be put in the "Files"
folder, under the name as specified in the Settings.txt file.

Lines that do not begin with "replace " are ignored, so you can enter
comments starting with # and group the files into sections.

Note that the tool needs to be restarted whenever you make a change
to the Settings.txt file.


Example:
 ```
 replace /resources/art/dynamic/player_character/outfit/all_naked_body/texture/___psd/chest_naked_caucasian_young_a01c01_bfa_h.dds skin_human.dds
 ```

This line replaces a chest texture in the game with the file called
"skin_human.dds" in the "Files" folder.


## How to use the tool
To start the tool, open the SWTOR-File-Changer.exe file. At the top
of the screen, you can select the folder where you have SWTOR
installed. The tool tries to find the path automatically, but if
have SWTOR installed in a different path than the default directory,
press the "Browse..." button and select the installation folder.

In the big list box you will find all the entries from the
Settings.txt file. Here you can check whether the Settings.txt file
was read correctly or if you made a mistake.

With the radio buttons above the list box you can specify which
environment should be edited: the normal game, or the Public Test
Server (PTS). This includes both the Assets folder, as well as the
UI file in the client folder. Note that you need to have the PTS
installed before you can edit it.

With the button "Changing Files" the tool will start searching
through the game files and replace all results from the settings.txt
file it finds.

By default, the tool automatically creates a backup of all game files
that get changed. This way, you can easily go back to the old version
when the game no longer works, or when a new patch has to be downloaded.
You can disable this functionality by unchecking the "Create Backup"
checkbox, but this is NOT recommended.

When you need to restore the backup, press the "Restore Backup" button
in the lower righthand corner. The tool will restore all game files
it can find in the "Backup" folder and copy them to your SWTOR
installation folder. Following that, you can once again start changing
the files.

If you need to extract an original file so that you can create the
replacement file, press the "Extract file" and enter the file you want
to extract. Note that you need to know the name so that you can extract
it. Extracted files can be found in the "Extracted" folder. Go ahead and
change them, copy them to your "Files" folder, edit the Settings.txt
file and you are good to go! Please note that when you have already used
the tool to replace a file, the extract function will extract your edited
file, not the original file. In that case, you need to restore the backup
if you want to get the original file.
