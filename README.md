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

2. Go into the Payload folder.

3. Copy the "Content" folder.

4. Create a new folder somewhere else called "Resources".

5. Paste the Content folder there.

6. Paste the modimporter executable into the Content folder and create a Mods folder within the Content folder.

7. Place the mod folders into the Mods folder. The folder hierarchy should look like this:
   Resources/
    └── Content/
        ├── Audio/
        ├── ...
        ├── modimporter
        └── Mods/
            ├── ModUtil/
            │   ├── ...
            │   └── modfile.txt
            └── AnotherMod/
                ├── ...
                └── modfile.txt
   If the mod that you got does not have a modfile.txt, it is an old type mod. Follow the instructions on the mod's page to install the mod. It should be the same if it isn't doing anything outside the Content folder. If a mod needs to be placed into a folder called Win/macOS, that is the iOS folder for mobile. You do not need to do this for new type mods, but you may need to rename the iOS folder to Win if any problems arise.

8. Copy the Content folder and then paste it into the Payload folder. Backup and delete the old Content folder beforehand to avoid any issues. You will need to replace that Content folder with the original one if you want to play vanilla.

9. Zip the payload folder and rename it's extension to .ipa
    
11. **EXTRA** Changing the Info.plist file to show the save file in the Files app
    - Open your file in a plist editor.
    - Search up for UIFileSharingEnabled.
    - Under that, paste this string:
      <key>LSSupportsOpeningDocumentsInPlace</key>
      <true/>
    - It should look like this:
      ...
      <key>UIFileSharingEnabled</key>
      <true/>
      <key>LSSupportsOpeningDocumentsInPlace</key>
      <true/>
      ...
    - There you go! Now it should show up in the files app after you have sideloaded it.
   
      
13. Use your preferred way of sideloading.
    - For Altstore(Refresh every 7 days, needs PC to do so but has it's own app to install your own apps), follow this guide: https://faq.altstore.io
      
    - For Sideloadly(Refresh every 7 days, needs PC to do so, everything must be done from pc), follow this guide: https://www.youtube.com/watch?v=vqTsavQc3lQ
   
    - For SideStore(Refresh every 7 days, does not need PC to do so, everything can be done from app after initial install), follow this guide: https://sidestore.io/#get-started
   
14. You're done! Now you can play with mods! You will have to do this all over again if you want to change the mods you have or revert back to vanilla. And if you don't pay for a certificate, you will have to refresh the app every 7 days or it will expire and be unplayable until you manually refresh it! You can probably see why I am going insane!!!!!!! You can probably have vanilla hades from the app store installed but it might not play well with your modded saves(they don't use the same directory it's because of cloud saves)
