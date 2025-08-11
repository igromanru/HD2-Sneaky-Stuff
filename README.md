# Helldivers 2 Sneaky Stuff by Igromanru

![Preview](https://i.imgur.com/tURMm9h.png)

### Description
Helldivers 2 Sneaky Stuff is an advancement of [Helldivers 2 Undetected Features](https://github.com/igromanru/HD2-Undetected-Features). I overcome many issues from "Undetected Features" tool by going internal.  
It's a dll, that has to be injected into the game and all features are controlled by hotkeys.  
It contains two type of features, **Undetected** and **Sneaky**.  "Undetected" features can be active all the time, while the "Sneaky" features will disable themselves to avoid being caught by GameGuard. (Read the AntiCheat section for details)  
I've left out Medals and Requisition Slips in Resupply Drop, since it's much faster to instant finish missions to get them.

## Features
### Undetected
- Infinite Stratagems
- Super Credits in Resupply Pod

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
Before you start, you have to unzip the files from the zip archive.
Both **HD2-Sneaky-Stuff-Injector.exe** and **Helldivers-2-Sneaky-Stuff.dll** has to be in the same directory!
If your AntiVirus doesn’t like it, disable it and add the directory where you unzipped the files to the exclusions list. It’s common for AV software to detect injectors.

### Inject Automatically

1. Load the game until you're in your ship
2. Execute the **HD2-Sneaky-Stuff-Injector.exe** (you must have administrator rights on the Windows account)
3. If the injection was successful, and you see the console window of Sneaky Stuff, you can close the window of the injector.
4. Use hotkeys to enable features while the game or the Sneaky Stuff console is in the foreground.
5. "Undetected" features can be disabled manually by pressing CTRL+[their assigned hotkey]. "Sneaky" disable themselves automatically. (See "*Sneaky" features and how to use them* section)
6. (optional) Move the "HD2 Sneaky Stuff" console window to a second monitor to see what happens there while you're playing.


### Inject Manually (alternative)
You can use any DLL injector that works for you to inject the **Helldivers-2-Sneaky-Stuff.dll**.
If you want to be extra sneaky, use a manual map injector or a driver based manual map injector.

## "Undetected" features description
"Undetected" features are like the name says, undetected. They can be activated and deactivated/restored at any time.

### Infinite Stratagems
Prevents Stratagems to go into cooldown and decrease in quantity. Works only for your Stratagems. All others are visual only.
For server sided stratagems like Resupply or SEAF Artillery, it works only if you're the host.

### Super Credits in Resupply Pod
Replaces one of the slot in the Resupply Pod with a stack of Super Credits.
See the "Resupply Drops Information" section for more details.

## "Sneaky" features and how to use them (Important information!)
GameGuard runs an integrity check in a random interval, I don't know exact timing, but it happens like once in a minute.
The whole idea behind the "Sneaky" features is to patch code for a short period of time to reduce the chance of being caught to minimum.
As long you don't spam the features none stop, the chance that GG catches a code change and closes your game are very small.

### Pseudo Infinite Health
Pseudo Infinite Health will change your health to 9999 (maximum what the game allows), **if your health value changes while the feature is active**.
As long the damage won't one shot you, you can take any amount of damage or heal yourself (if you're not full HP).  
With Ctrl+(hotkey) health can be "restored" to 200. Same rules apply, you have to take damage while it's active.

### Pseudo Infinite Stamina
Pseudo Infinite Stamina changes Stamina value to 9999 and consumption multiplier to a fraction, which will make you consume a very little Stamina after the feature has unpatched itself. The effect should last until you die, but I can't remember all the nuances.
It also affects Stamina regeneration, so you might need to use Stims and reactivate at some point.

### Speedhack
Sets your movement speed to 3x. Works on the ship as well.  
You have to start moving while the hook is active.

### Collect X Samples
Collect X Samples is currently set to 98, in the time while the feature is active, you've to pick up any sample, and you will receive 98 of it.
**Important:** Sample limit per game is 99! (100 but you don't see it)
If the team together has over 99 during the extraction, none will count.
All type of samples count to the same limit! While farming, only farm one type of sample per mission! Take 99 of one type and extract.

### Instant Complete Mission (host only)
Works only, if you're the host! Does exactly what it says.
It will mark all primary missions as completed and will allow you to extract.
Other players will see the mission as "failed", but they will still get the rewards.

### Instant Shuttle (host only)
Will skip the wait time for the Pelican-1 to arrive.
The feature has to be active while you finish typing the code into the extraction beacon. You can simply pretype the code until the last arrow, activate the feature and press the last arrow to finish.

## Farming section
### Resupply Drops Information
- In each mission, there is a **random** pick-up limit that applies to each player, 0-15. After the limit is reached, the server will stop adding picked up resources to players.
- The limit is somehow related to the map size, mission type and terrain. The ideal map size is reached on difficulty 3, and overall difficulty 3 was the best for getting the most drops on average in the past (no idea how it's now).
- Picked up resources are added to each player in the squad. It allows farming faster with more players, since each can pickup the same amount of stacks per mission.
- Super Credits, Medals and Requisition Slips count to the same limit. Therefore, you might want to focus on one resource at a time.
- Don't use any Boosters that upgrade/change the Resupply Pod, it might prevent it from dropping resources.
- Sometimes the Super Credits model isn't loaded into the game and will appear as ? (question mark). Just leave the mission and try another one.



### Medals, Requisitions and XP
Getting all three is pretty easy by just starting level 10 Super Helldive difficulty and instant finishing the mission.

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



### SC farming
Read "Resupply Drops Information" above to understand the process.
Farming Super Credits with features from this tool is fastest with a full party.
I can't give you step-by-step instructions here since I don't know exactly which planets, mission types and difficulties are currently the best.
But overall, what you have to do it:

- Enable "Infinite Stratagems" and "Super Credits in Resupply Pod"
- Go into difficulty 3 missions that are not in Mega Cities
- Drop as fast you can 13 resupply pods for each player
- Count how many stacks SC a player can pick up before it stops appearing on the UI
- Let every player pick the exact amount of drops, while you finish dropping as many Resupply Pod as needed
- Abort the missions
- Repeat


Find out for yourself which mission types and planet have highest drop rates.
If somebody makes a guide on what’s best, I can add it here.

### Don't drop SC in public lobbies!
**Don't drop Super Credits, Medals or Requisition Slips with randoms in a mission.
You're not only risking your account, but also drawing attention to the exploit!**

---

### Log file
In case something happens to the console window or the game closes/crashes, you can find the log file, "Sneaky-Stuff.log" in the game's root directory.
For Steam it's in: *C:\Program Files (x86)\Steam\steamapps\common\Helldivers 2\*

### AntiCheat Details
**nProtect GameGuard in Helldivers 2** serves solely as anti-tamper software. Despite what it can do in other games, in HD2 it only attempts to preserve the integrity of the original code and prevent external software from accessing the process. It doesn't even check for foreign DLLs in the process.
If GameGuard detects ".text" code changes or one of the blacklisted programs like Cheat Engine, it will only close the game, usually with a message.
There are no (GameGuard) bans. And until today, no bans for cheaters were reported in any of HD2 related cheating communities.

### Disclaimer
1. The tool doesn't bypass the nProtect GameGaurd AntiCheat protection! It relies on the incompetence of the anti-cheat to protect the process and on the fact that, in the worst-case scenario, it will just close the game if it detects something.
2. I take no reposibility for any damage to your game or account. By using my tools, you accept the risk that even after all this time since release, the developers might change their approach at any moment and start applying penalties to accounts.
3. Infinite Stratagems with Resupply Pod drops is a very slow way to farm Super Credits. There are much better and faster ways to farm with a bypass and cheats from closed/premium communities. Just do your own research and don't ask me about it.
