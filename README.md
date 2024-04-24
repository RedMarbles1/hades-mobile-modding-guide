# Hades Mobile Modding Guide(the unreasonable effectiveness of kludging data files)
A guide on how to mod the mobile version of Hades. Please read the warning before proceeding because this is not something a normal person should attempt. [INCOMPLETE]

# Warning
Please only do this if you know what you are doing and can debug issues by yourself. I'm not the dev of anything mentioned here, and can't really help you if any issue arises. Backup your save files before proceeding(I have a guide for that [here!](https://github.com/RedMarbles1/hades-save-transfer-guide)). 

# What do you need

- A decrypted .ipa package of the game. This file is where all the game files are located and what you'll mod. Due to the nature of iOS/iPadOS, we need the game package as we can't access the game files after it has been loaded onto your device. You can get this file from external sites, or extract it from your phone using a variety of tools which I do not want to talk about here. Be cautious while downloading ipa files from sources outside App Store though, as there is a risk of malware being present. **DO YOUR RESEARCH WELL AND ONLY USE WEBSITES TRUSTED BY EVERYONE BEFORE DOWNLOADING FROM THERE. I'M NOT RESPONSIBLE IF YOUR NETFLIX ACCOUNT IS STOLEN**

- [Modimporter](https://github.com/SGG-Modding/ModImporter). This is important as it is what you will use to import the mods. Old type mods can also work, but this is just easier.

- Mods that you want to play with. Mods that require a keybind to be used CANNOT be used properly in the mobile version because of the lack of keys. If youre going to connect a keyboard and then try it, please do. I need someone else to contribute to my insanity that is mobile modding.

- A way to open info.plist files. This is only relevant if you want to use the files app on your phone to modify your save files. I'd recommend it to minimize the amount of meddling you'll have to do in the game files. [ProperTree](https://github.com/corpnewt/ProperTree) is a free way to open plist files which should be enough here.

- A way to sideload apps to your iDevice. You can use AltStore, SideStore or Sideloadly. I'd recommend SideStore as it is the least maintenance one after the initial install, requiring no PC.

# How to do this(why)

1. Rename the extension of your .ipa file to .zip and then extract it. There should be a "Payload" folder extracted.

2. Go into the payload folder.


