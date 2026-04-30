# Helldivers 2 Sneaky Stuff by Igromanru
![Preview](https://i.imgur.com/z6e9XpH.png)

## Index
- [Description](#description)
- [Features](#features)
  - [Undetected](#undetected)
  - [Sneaky](#sneaky)
  - [Video showcase](#video-showcase)
- [How to use](#how-to-use)
  - [Inject Automatically](#inject-automatically)
  - [Inject Manually (alternative)](#inject-manually-alternative)
  - [Configuration file](#configuration-file)
- ["Undetected" features description](#undetected-features-description)
  - [Infinite Stratagems (Default Hotkey: Numpad 7)](#infinite-stratagems-default-hotkey-numpad-7)
  - [Super Credits in Resupply Pod (Default Hotkey: F3)](#super-credits-in-resupply-pod-default-hotkey-f3)
  - [Medals in Resupply Pod (Default Hotkey: F4)](#medals-in-resupply-pod-default-hotkey-f4)
- ["Sneaky" features and how to use them (Important information!)](#sneaky-features-and-how-to-use-them-important-information)
  - [Pseudo Infinite Health (Default Hotkey: Numpad 1)](#pseudo-infinite-health-default-hotkey-numpad-1)
  - [Pseudo Infinite Stamina (Default Hotkey: Numpad 2)](#pseudo-infinite-stamina-default-hotkey-numpad-2)
  - [Speedhack (Default Hotkey: Numpad 3)](#speedhack-default-hotkey-numpad-3)
  - [Collect X Samples (Default Hotkey: Numpad 4)](#collect-x-samples-default-hotkey-numpad-4)
  - [Instant Complete Mission (host only) (Default Hotkey: Numpad 8)](#instant-complete-mission-host-only-default-hotkey-numpad-8)
  - [Instant Shuttle (host only) (Default Hotkey: Numpad 9)](#instant-shuttle-host-only-default-hotkey-numpad-9)
- [Farming section](#farming-section)
  - [Resupply Drops Information](#resupply-drops-information)
  - [Medals, Requisitions and XP](#medals-requisitions-and-xp)
  - [Samples](#samples)
  - [[Patched] SC farming](#patched-sc-farming)
  - [Don't drop SC in public lobbies!](#dont-drop-sc-in-public-lobbies)
- [Log file](#log-file)
- [AntiCheat Details](#anticheat-details)
- [Disclaimer](#disclaimer)
- [Detections History](#detections-history)
- [My other work](#my-other-work)

### Description
Helldivers 2 Sneaky Stuff is an advancement of [Helldivers 2 Undetected Features](https://github.com/igromanru/HD2-Undetected-Features). I overcome many issues from "Undetected Features" tool by going internal.  
It's a dll, that has to be injected into the game and all features are controlled by hotkeys.  
It contains two type of features, **Undetected** and **Sneaky**.  "Undetected" features can be active all the time, while the "Sneaky" features will disable themselves to avoid being caught by GameGuard. (Read the AntiCheat section for details)  

## Features
### Undetected
- Infinite Stratagems
- Super Credits in Resupply Pod
- Medals in Resupply Pod

### Sneaky
- Pseudo Infinite Health
- Pseudo Infinite Stamina
- Speedhack
- Collect X Samples
- Instant Complete Mission (host only)
- Instant Shuttle (host only)

### Video showcase
[![Showcase](https://img.youtube.com/vi/YSuHrW66k4E/0.jpg)](https://www.youtube.com/watch?v=YSuHrW66k4E)

## How to use
Before you start, disable your antivirus first. All public DLL injectors are flagged as potentially dangerous software and will be removed by many antivirus programs.  
Unzip **HD2-Sneaky-Stuff-Injector.exe** and **Helldivers-2-Sneaky-Stuff.dll** into the same directory.  
Add that entire directory to your antivirus exclusions, then you can re-enable it. (Use google to find out how it works for your AntiVirus)

### Inject Automatically
1. Load the game until you're in your ship
2. Execute the **HD2-Sneaky-Stuff-Injector.exe** (you must have administrator rights on the Windows account)
3. If the injection was successful, and you'll see the console window of Sneaky Stuff
4. Use hotkeys to enable features while the game or the Sneaky Stuff console is in the foreground.
5. "Undetected" features can be disabled manually by pressing CTRL+[their assigned hotkey]. "Sneaky" disable themselves automatically. (See "*Sneaky" features and how to use them* section)
6. (optional) Move the "HD2 Sneaky Stuff" console window to a second monitor to see what happens there while you're playing.

### Inject Manually (alternative)
You can use any DLL injector to inject **Helldivers-2-Sneaky-Stuff.dll** into the `helldivers2.exe`.  
If you want to be extra sneaky, use a manual map injector or a driver based manual map injector.

### Configuration file
The `Settings.toml` file will be created in the `/Helldivers 2/bin/` directory if it doesn’t already exist, and it will be read from there.  
In the **Settings.toml** configuration file, you can change the single-key hotkeys assigned to each feature. To disable certain features, you still need to use the hard-coded modifier CTRL + (hotkey).  
Hotkey values are [Virtual-Key Codes](https://learn.microsoft.com/en-us/windows/win32/inputdev/virtual-key-codes), and can be assigned as either decimal or hex-decimal.  
e.g.: `InfiniteHealthKey = 0x61` is the **Numpad 1** key.  
If you have a non-US keyboard layout (e.g. Russian, German, Chinese), just use google to find corresponding Virtual-Key Codes.  

Some features like "Collect X Samples" or "Speedhack" have also modifieable values.  

You can also change the unhook delay times for certain features in the settings file.  
Values are in milliseconds (1 sec = 1000 ms).  
Increase them at your own risk. You can play around with them, since the worst thing that can happen is that GG closes your game, but anything over 6 sec increases the chance of getting caught exponentially.

## "Undetected" features description
"Undetected" features are like the name says, undetected. They can be activated and deactivated/restored at any time.

### Infinite Stratagems (Default Hotkey: Numpad 7)
Prevents Stratagems to go into cooldown and decrease in quantity. Works only for your Stratagems. All others are visual only.  
For server sided stratagems like Resupply or SEAF Artillery, it works only if you're the host.

### Super Credits in Resupply Pod (Default Hotkey: F3)
Replaces second slot in the Resupply Pod with a stack of Super Credits.  
Don't even ask, replacing all 4 slots with Super Credits doesn't work.  
See the "Resupply Drops Information" section for more details.

### Medals in Resupply Pod (Default Hotkey: F4)
Same as **Super Credits in Resupply Pod** but replaces third slot with Medals.

## "Sneaky" features and how to use them (Important information!)
GameGuard runs an integrity check in a random interval, I don't know exact timing, but it happens like once in a minute.
The whole idea behind the "Sneaky" features is to patch code for a short period of time to reduce the chance of being caught to minimum.
As long you don't spam the features none stop, the chance that GG catches a code change and closes your game are very small.

### Pseudo Infinite Health (Default Hotkey: Numpad 1)
Pseudo Infinite Health will change your health to 9999 (maximum what the game allows), **if your health value changes while the feature is active**.
As long the damage won't one shot you, you can take any amount of damage or heal yourself (if you're not full HP).  
With Ctrl+(hotkey) health can be "restored" to 200. Same rules apply, you have to take damage while it's active.

### Pseudo Infinite Stamina (Default Hotkey: Numpad 2)
Pseudo Infinite Stamina changes Stamina value to 9999 and consumption multiplier to a fraction, which will make you consume a very little Stamina after the feature has unpatched itself. The effect should last until you die, but I can't remember all the nuances.
It also affects Stamina regeneration, so you might need to use Stims and reactivate at some point.

### Speedhack (Default Hotkey: Numpad 3)
Sets your movement speed multiplier. (Default set to 3x) Works on the ship as well.  
You have to start moving while the hook is active.  
If you're the host, it affects enemies as well, if they move while the hook is active.

### Collect X Samples (Default Hotkey: Numpad 4)
Collect X Samples is default set to 98, in the time while the feature is active, you've to pick up any sample, and you will receive 98 of it.  
**Important:** Sample limit per game is 99! (100 but you don't see it)  
If the team together has over 99 during the extraction, none will count.
All type of samples count to the same limit!  
You can also set the value to 33 in the settings and pick up one of each sample type, if you want.  

### Instant Complete Mission (host only) (Default Hotkey: Numpad 8)
Works only, if you're the host! Does exactly what it says.
It will mark all primary missions as completed and will allow you to extract.
Other players will see the mission as "failed", but they will still get the rewards.

### Instant Shuttle (host only) (Default Hotkey: Numpad 9)
Will skip the wait time for the Pelican-1 to arrive.
The feature has to be active while you finish typing the code into the extraction beacon. You can simply pretype the code until the last arrow, activate the feature and press the last arrow to finish.

## Farming section
### Resupply Drops Information
Super Credits pick-up was patched with v6.2.2 (28.04.2026).  
To my current knowledge it's not longer possible to pick-up Super Credits that weren't part of the mission.

### Medals, Requisitions and XP
Getting all three is pretty easy by just starting level 10 Super Helldiver difficulty and instant finishing the mission.

1. Drop directly into the extraction zone
2. Activate "Instant Complete Mission" feature
3. On the extraction beacon, type in the arrows code until one arrow is left
4. Activate "Instant Shuttle"
5. Finish the code

### Samples
Pretty much the same as with Medals, Requisitions and XP.

1. Drop into any mission that has samples that you need
2. Find the sample type you need
3. Activate "Collect X Samples" feature
4. Pick up the sample
5. Before extracting, make sure that the whole party doesn't have more than 99 samples (you can see it in the HUB)
6. Use "Instant Complete Mission" and "Instant Shuttle" like described under "Medals, Requisitions and XP" section above to extract fast

### [Patched] SC farming
Super Credits pick-up was patched with v6.2.2 (28.04.2026).  
To my current knowledge it's not longer possible to pick-up Super Credits that weren't part of the mission.

---

## Log file
The `Sneaky-Stuff.log` file will be created and written in the `/Helldivers 2/bin/` directory.
If something happens to the console window, or the game closes or crashes, you can find what was printed to the console in the log file.  
If you want to report a bug or error, include the content of the latest log file.  

## AntiCheat Details
**nProtect GameGuard in Helldivers 2** serves solely as anti-tamper software. Despite what it can do in other games, in HD2 it only attempts to preserve the integrity of the original code and prevent external software from accessing the process. It doesn't even check for foreign DLLs in the process.
If GameGuard detects ".text" code changes or one of the blacklisted programs like Cheat Engine, it will only close the game, usually with a message.  
There are no (GameGuard) bans. And until today, no bans for cheating were reported in any of HD2 related cheating communities.

## Disclaimer
1. The tool doesn't bypass the nProtect GameGaurd AntiCheat protection! It relies on the incompetence of the anti-cheat to protect the process and on the fact that, in the worst-case scenario, it will just close the game if it detects something.
2. I take no reposibility for any damage to your game or account. By using my tools, you accept the risk that even after all this time since release, the developers might change their approach at any moment and start applying penalties to accounts.
3. Infinite Stratagems with Resupply Pod drops is a very slow way to farm Super Credits. There are much better and faster ways to farm with a bypass and better features. Just do your own research and don't ask me about it.

## Detections History
On 03.09.2025 GameGuard added all versions of Sneaky Stuff and [Helldivers 2 Undetected Features](https://github.com/igromanru/HD2-Undetected-Features) that were released on unknowncheats.me to their detection list.  
Detections appears to be AOB pattern-based and affects versions 1.0 to 1.3, together with the injector.  
To test if they will keep up, I released a new undetected version of Sneaky Stuff, v1.4.0 on UC, which become detected on 16.09.2025.  
I moved away from UC to distribute the tool privately on Discord, and since v1.4.1 the DLL has been undetected.   
On 02 December 2025, I started to do releases again on GitHub (here), but it's still undetected. It looks like they only care about UC.    
The injector itself remains detected, but unless there are errors, it injects the DLL into the game and closes itself, which happens too fast for GG to notice.  

## My other work
[Helldivers 2 Farming Guide](https://github.com/igromanru/HD2-Farming-Guide)

## Archived Discord Server
The server is by now archived and I moved one from maintaining it, but there are still useful stuff there.
<a href="https://discord.gg/SKbHMw5Npf"><img src='https://discordapp.com/api/guilds/1417474730906095626/widget.png?style=shield'></a>  