
# SoH Mod Organizer

Ultimately, this is just a fancy renaming tool. It will keep track of your files original names for ease of use, and revert them for when you wish to add more. It's written in python, and uses numerical order (with the proper padding), to ensure that SoH loads the mods in your desired order. I've limited it to 999 mods at maximum, which frankly is an absurd amount already, and see no reason to increase this further.

If you wish to do so, you're more than welcome to do so yourself.

# Usage

Follow the setup for the mods folder [here](https://github.com/HarbourMasters/Shipwright) in the Custom Assets section

## Note for Ubuntu LTS users
You'll need to run

`sudo apt install libsdl2-2.0-0`

for it to work

## Sorting mods

+ Open the program
+ Select browse
+ Navigate to the mods folder
+ Sort the list as desired with your keyboards arrow keys, or the arrow buttons within the GUI
+ Select the sort buttons
+ Enoy the game!

## Adding mods

At the moment due to the limitations of the current code, resorting isn't possible

+ Open the program
+ Select browse
+ Navigate to the mods folder
+ Select revert
+ Sort the list as desired with your keyboards arrow keys, or the arrow buttons within the GUI
+ Select the sort buttons
+ Enoy the game!

# Technical details
This python script, which you can just run directly rather than using the binaries, renames the files in a %03d format, writes the original names to a file, and uses this to retain both the order they were in, so that you can see what file corelates to what.

The original version of this mod organizer did a lot more, to try and provide ease of use, but a number of bugs and edge cases that I simply could not resolve, and anyone is more than welcome to fix that code, as I have provided it within this repository.

The icons are loaded in through base64 byte streaming to allow for both the script, and the executables, to have their icons regardless of how it's run. The binary is created using pyinstaller and feeding that in through github actions, which unfortunately causes extreme bloating for the linux binary.

This code requires wxPython and setproctitle to run correctly, you can usually install them in pip. For the Arch users, and I think Nix users (IIRC), can get these from their package managers.

`$ pip install wxpython setproctitle`

# Known issues
At the moment, if you're in KDE with wayland, the icon won't show up, there's no fix for this, hope KDE fixes it in 6, I tried about a dozen different methods to work around this limitation, and nothing practical seems to be possible at the moment. Gtk desktops should have no such issue.
