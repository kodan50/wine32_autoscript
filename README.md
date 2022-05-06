# wine32_autoscript
Helps to automate running apps in wine32 without a lot of complicated script edits and such

 I read somewhere that switching between a 64-bit and 32-bit flavor of Wine is annoying and you have to use scripts everywhere and whatever. I don't like this solution, so if you need a simpler way to handle a 32-bit and a 64-bit version of Wine, this script will allow you to call a 32-bit flavor right away. In theory, you should be able to use this for any version of Wine that isn't your main. I also have no idea what I am doing, so I won't be held liable if this wipes your computer. Have fun!

Preperation:
Create a 32-bit wine prefix called wine32 and just use the script as is. If you want to use this with any other wine prefix, you can change wine32 to whatever other wine prefix you want.

Installation:
Copy this file into any of the folders that your path refers to, or create a new folder and add it to your path in bashrc.
you may also need to chmod +x to make it executable.

Usage:
If you want to run a general command (winetricks, winecfg, or whatever) just type wine32 (command), and it will launch the command you ask in that prefix.
If you want to run an application, navigate to the folder that contains the file and type wine32 (file.exe), and it will add the current directory to the file path and execute wine with that file.

How it works:
We will search for the name of the file in the directory you are in, and if it exists, it will add the path to a variable so it can properly call wine32 with whatever file you want. If the file does not exist, it is assumed you are not running an app or game, and instead will issue whatever request to wine32.
