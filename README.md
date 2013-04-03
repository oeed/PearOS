PearOS
======

PearOS - OS X Inspired OS for ComputerCraft

Over the past few weeks I have been rather busy, I've managed to fix a good majority of the bugs but I haven't really added many new features, as many people have been asking for the new version I've decided to post a bug fix preview.

In short, PearOS is a graphical 'OS' for ComputerCraft. It completely (will, at this stage there are a few things that need to be added) removes the need to use the console. Why? Most of the people who play FTB with me have no idea how to use the computers and end up just playing 'adventure' on them. So, this is my answer to that problem.

For more information look here and here.

Screenshots
===========
PearOS's (and obviously OS X's) menus are at the top of the screen instead of on the window. The menus are specific to the current application.
![Imgur](http://i.imgur.com/evS8mpg.png)

System Preferences, the OS X version of 'Control Panel'
![Imgur](http://i.imgur.com/UyWjAZt.png)

PearOS supports multiple windows and applications open at once.
![Imgur](http://i.imgur.com/2FrkEAm.png)

Download
========

Enter the following in to the shell:
[quote]pastebin get LRFsvuN3 PearOS.pkg[/quote]
(It will take some time [20+ seconds], just be patient.)

Then run 'PearOS.pkg'.

If you're interested, PearOS uses my packaging utility, Package Maker, to squash all of its ~70 files in to one automatically installing file. Rather than spending hours making some pointless web installer or having to use Dropbox, I simply entered a single shell command. Anyway, enough plugging, on with the post.

New Features/Tweaks
===================
(Compared to Preview 1)

As mentioned earlier, I haven't had the time to add many new features, however I've added some minor new features/tweaks (some of them aren't really changes that the end user will notice, however)
You can now open 'txt' files from Finder, support for registering an extension is there, but buggy.
Modularised much of the code (each object/group of functions has its own file). Essentially, the main system has changed from one ~2300 line file to a ~550 line file and 40 files that are included at run time.
Cleaned up the code (indentation was broken because of Sublime Text).
Added 'About' window framework, this should prevent the many errors occurring.
Windows now start in the middle of the screen.

Bugs Fixed
==========
(Compared to Preview 1)
Thanks to everyone who submitted bugs and/or posted fixes!

- First run is resizeable
- Windows don't start centered
- Applications windows don't get focus
- Browsing Finder Crash: PearOS.lua:1782:vm error:(Java out of bounds exception)
- About Finder crashes,  Finder:203: index expected, got nil
- Crash when clicking on an 'About' window
- TextEdit wrapping cuts off during a word (thanks Kingdaro!)
- Menus stay open when dock icon is clicked (app open)
- Prevent the whole screen from being redrawn every second. I have implimented this, but I've turned it off because it causes some problems when buttons are click (they will stay blue until the screen is redrawn). You can turn it on by commenting out line 419 in PearOS.lua. I will change this in future.
- Added buffering to drawing framework (no more flickering! )
- A number of TextEdit crashes and glitches
- Resizing TextEdit doesn't work
- PearOS logo isn't center on boot (Thanks Leonardoas26)
- 'Starting PearOS in verbose mode...' poorley placed (ditto)
- 'Finder:203: index expected but got nil' when resizing 'About this Pear'
- Changing the desktop background doesn't do anything.
- A few minor bugs that I've found, and possible some I've forgotten.

What's Coming/In the Works
========
- Wireless peripherals (similar to AirPlay, you can use remote printers, monitors and disk drives [disk drives are causing me some hassle, however]). This is essentially done, apart from the ability to access files from disk drives.
- Running non-PearOS programs. This will be released very soon, I know it is vital for the OS. One question, should the programs be their own app/dock icon or should they run within another application. (Mac users, think X11. Not sure of any similar applications)
- A help mode (hold 'H' at boot). To be honest, I don't think I need to add this. Thoughts?
- A guide on how to make an application. I could do this tomorrow, however, I want to make sure I'm not going to make any large changes to how applications are made/run first.
- Fullscreen mode (Suggested by theoriginalbit)
- Project moving to GitHub
- Known Issues
- Arrow keys (vertical) missing from TextEdit.
- Scrolling missing from TextEdit.
- Selection is incorrect in TextEdit due to text wrapping.

Boot Modifiers
=====
One feature that was present very early on (way before the first preview) was boot modifier keys, and I simply forgot to tell you .
Essentially, when the computer is turning on and the screen is white, before the PearOS logo appears, you can hold one of the following keys to change what will happen (you have about one second to do so).

       C - This will boot you strait in to CraftOS mode incase you want to use it. (You can also click on 'Restore CraftOS' from the 'P' menu)
       V - This will boot you in verbose mode. Essentially it is designed to prevent the 'Oh noes!' crash screen and will do the regular red crash text (some times two errors are thrown and you can't see the both). It will also list any peripherals connected and tell you whats happening at boot. You can enter shell commands from here too.
       M - This will prevent PearOS from using any attached monitor. By default it will use any attached monitor.

Keyboard Shortcuts
======
I have been asked what the '#' means on the menus. The hash ('#') is the closest thing to the command symbol on OS X. See the below screenshot. Whenever you see one you can use the Command or Control  key + the letter listed to do that menu action instead. (Note: Due to the fact the Command + Q is captured the by OS [or Java, I'm not sure] on OS X you will have to use Control + Q) 
![Imgur](http://i.imgur.com/1FuhZo6.png)

I want to help, what can I do?
==============================
I've had a number of people request to help with PearOS. In terms of the actual core OS, no sorry. This is a personal project, also if other people get involved it will get hard to maintain constancy. However, I will soon be posting a tutorial on how to make an application for PearOS. Once you've made it, send it to me and I might include it with the OS or on an App Store/thread for applications. (Also, TextEdit (more specifically, OSTextView) is giving headaches. Any assistance would be appreciated)

If you have bugs or suggestions please let me know below.

Licence

PearOS is released under Creative Commons Attribution-NonCommercial-NoDerivs 3.0 Unported (CC BY-NC-ND 3.0) License

In simple terms this means that...

You are free to:
- Share, copy, distribute and transmit the work.

Under the following conditions:
- Attribution - You must attribute the work in the manner specified by the author or licensor (but not in any way that suggests that they endorse you or your use of the work).
- Noncommercial - You may not use this work for commercial purposes.
- No Derivative Works - You may not alter, transform, or build upon this work. (With out permission from myself)

With the understanding that:
- Waiver - Any of the above conditions can be waived if you get permission from the copyright holder.
- Public Domain - Where the work or any of its elements is in the public domain under applicable law, that status is in no way affected by the license.
- Other Rights - In no way are any of the following rights affected by the license:
- Your fair dealing or fair use rights, or other applicable copyright exceptions and limitations;
- The author's moral rights;
- Rights other persons may have either in the work itself or in how the work is used, such as publicity or privacy rights.
- Notice - For any reuse or distribution, you must make clear to others the license terms of this work.

See http://creativecommo...s/by-nc-nd/3.0/ for more information.
