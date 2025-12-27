---
title : 'RPG Maker'
---

# RPG Maker

[RPG Maker](https://www.rpgmakerweb.com/) is a series of programs for the development of role-playing video games.

## Windows

Some Japanese games are compatible with [Locale Emulator](https://xupefei.github.io/Locale-Emulator/) but [enabling JP Locale](/all-platforms/jp-locale) may be required.

## Linux

### Native

Many games can be played natively on Linux using EasyRPG Player and mkxp. RPG Maker MV/MZ games can be run through a [local web server](https://rpgmakerofficial.com/product/MV_Help/page/01_11_08.html) and a browser or [NW.js](https://itch.io/blog/484532/how-to-update-nwjs-in-rpg-maker-mv-for-rpg-devs).

### Lutris

> [!info] Information
> Requires to have [JP Locale enabled](/all-platforms/jp-locale).

1. Create a vanilla Wine prefix, install [English](https://www.rpgmakerweb.com/run-time-package) and/or [Japanese](https://rpgmakerofficial.com/support/rtp/) RTPs.
2. Install [Japanese fonts](/linux/wineprefixes).
3. Download [RPG Maker 2003 fonts](https://web.archive.org/web/20201206133232/https://rpgmaker.net/users/kentona/locker/Fonts.rar) and copy them to `drive_c/windows/Fonts`.
4. Set the `LANG="ja_JP.UTF-8"` or `LC_ALL="ja_JP.UTF-8` environment variable if your game is in Japanese and run it through Lutris.
5. (Optional) For RPG Maker MV, you can run `winetricks d3dcompiler_43 corefonts` if you have trouble running some games.

## Known issues

- Try different RTP installers if you get any errors.
- You might have to change Wine "Compatibility mode" using `winecfg` to run some games.
- Some Wine versions may require to [delete "libEGL.dll"](https://github.com/ValveSoftware/Proton/issues/3694#issuecomment-968034842) from the game directory, [disable "libglesv2.dll"](https://www.reddit.com/r/linux_gaming/comments/p7t05w/comment/j64kvt8/) using `winecfg` or [install "quartz" and "devenum"](https://blog.easyrpg.org/2017/10/running-rpg-maker-games-in-wine/) through Winetricks to run a game.
- Editing "Game.ini" to change the DLL used by a game [might prevent missing DLL errors](https://forums.rpgmakerweb.com/index.php?threads/question-around-rgss102e-dll.107608/#post-958495)
- Use `iconv` and `unzip` commands to fix files with encoding issues in their name or content as they can crash the game.
- For MIDI playback support, run `winetricks directmusic` , install and configure `timidity` or just convert MIDI files to MP3.

## Game translations

1. Extract resources from "Game.rgss" using [RGSS Decryptor](https://github.com/usagirei/RGSS-Decryptor).
2. Copy them to the game directory.
3. Extract the patch archive to the same location.
4. Delete "Game.rgss".

Some projects might recommend [RPGMaker Trans](https://rpgmakertrans.bitbucket.io/index.html) instead.

## Controls

- [RPG Maker forums thread](https://forums.rpgmakerweb.com/index.php?threads/rpg-maker-pc-game-controls-mv-vx-ace-vx-xp-2003-2000.140758/)

## Links

- [NW.js Documentation - "Package and Distribute"](https://docs.nwjs.io/For%20Users/Package%20and%20Distribute/)
- [NW.js Documentation - "Command Line Options"](https://docs.nwjs.io/References/Command%20Line%20Options/)
- [NW.js website](https://nwjs.io/)
- [NW.js download](https://dl.nwjs.io/v0.96.0/)
- [kakurasan's Linux blog](https://kakurasan.blogspot.com/)
