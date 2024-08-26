## About The Project

[Playful Plugins](https://furimanejo.itch.io/playful-plugins) is a collection of plugins and other tools that detect events, usually from games (e.g., getting a kill, receiving damage). These events can then be connected to fun stuff like:
* Sex toys, like those from Lovense (requires [Intiface Central](https://intiface.com/central/?ref=playfulplugins), check the supported devices [here](https://iostindex.com/?filter0ButtplugSupport=4?ref=playfulplugins)).
* Shock devices, like the Pishock shock collar or DG-LAB Coyote (requires an [XToys](https://xtoys.app/) account, check the supported devices [here](https://iostindex.com/?filter0Availability=Available,DIY&filter1Connection=Digital&filter2XToysSupport=1&filter3Features=OutputsEstim)).
* Vtuber models, through Vtube Studio hotkeys.

Consider joining my [Discord Server](https://discord.gg/HswJa4tDMf) if:
* You need help setting up the app or are experiencing problems with it.
* You're a game dev interested in adding.
* You're a streamer or content creator using this app, I'd be happy to watch you and share your work.
* You're looking for like-minded people to hang out with.

If you liked this project and want to contribute, please consider subscribing or donating at:
* [Itch](https://furimanejo.itch.io/playful-plugins),
* [Subscribestar](https://subscribestar.adult/furimanejo),
* [Liberapay](https://liberapay.com/Furimanejo/),
* [Stripe](https://donate.stripe.com/7sI3eZcExdGrc5WeUU).

## Games And Events
### [Overwatch 2](https://store.steampowered.com/app/2357570)
Events detected through computer vision (no code injection or game file modifications): 
* Eliminations, assists, saves, being eliminated, receiving and applying Mercy's beams, Zenyatta's orbs, immortality field, hack, or "prompt" effects (e.g., Stunned, Sleep, Hacked).

### [League of Legends](https://www.leagueoflegends.com/)
Events detected through the official game client API: 
* Kill, death, assist, destroy turret or inhibitor, win or lose match, creep score and ward score, "Minions Have Spawned".

### [Helldivers 2](https://store.steampowered.com/app/553850)
Events detected through computer vision (no code injection or game file modifications): 
* Receiving damage or healing, being low on health.

### [Peggle Deluxe](https://store.steampowered.com/app/3480)
Events detected through computer vision (no code injection or game file modifications): 
* BALL-O-TRON and FEVERMETER bars.

### [Kinky Dungeon](https://ada18980.itch.io/kinky-dungeon)
Events detected through an external utility mod "KD_events.zip" (to be loaded into the game's main menu): 
* Deal Damage, take Damage, apply/remove restraint/armor, struggle, leash tug, play with yourself, edge, orgasm, orgasm denied, trigger a trap, open a chest, consume shrine, get spell orb, get perk, use stairs.

### [Elden Ring](https://store.steampowered.com/app/1245620)
Events detected through computer vision (no code injection or game file modifications, disabling EAC not necessary): 
* Taking damage, using FP or stamina, dying.

### [PowerWash Simulator](https://store.steampowered.com/app/1290000)
A demo for user-made modules, event detected: 
* Part cleaned.

### [Ero Dungeons](https://erodungeons.itch.io/ero-dungeons)
Events detected through official in-game support (make sure to enable it in the game's settings): 
* "Deal Damage", "Take Damage", "Take Lust Damage", "Get Grappled", "Take Grapple Damage", "Equipment Breaks", "Faltered", "Afflicted", "Kidnapped", "Cursed Item Equipped", "Item Uncursed".

## Connecting Toys And The Score/Pattern System
To connect your toys, run [Intiface Central](https://intiface.com/central/?ref=playfulplugins) and make sure its server is running and waiting for client, then in Playful Plugins' "Intiface" tab click connect. If your toy is powered it should soon be detected and appear on the device list. Make sure your toy is not connected elsewhere (like to the lovense app) and that it's also not paired to windows (intiface does not require pairing your devices).

Playful Plugins uses a combination (simple sum) of points and patterns to trigger the connected toys, according to the values set for each device (defaults to 0% intensity at 0 points and 100% intensity at 100 points).

Events can award points. Points can be additive, adding to a score that decay over time, or non-additive (or instant), only existing while the respective event happens. Event points can also be proportional to a multiplicative value within the event (for some events it makes sense to ask "how much" of the event was triggered for example for a "Take Damage" event we can ask "how much damage was taken").

Events can also trigger patterns, each pattern is defined as a series of values between 0 and 100 (custom patterns may be added by editing the config_main.json file). Pattern triggers consist of an intensity value that scales the respective pattern between 0% and 100%, and a disable delay value that dictate for how long the pattern should play after the event ends. Triggering an event multiple times or continuously refreshes the disable delay.

## How To Capture The Overlay In OBS
* In Playful Plugins' main tab set "Hide Overlay From Taskbar" to false.
* In OBS create a new window capture targeting the "Playful Plugins (Overlay)" window and set it's capture method from "Automatic" to "Windows 10" (otherwise the overlay's background won't be transparent). 
* Place the overlay window capture on top of the other windows in the sources hierarchy, so it correctly draws above the other windows.

## User-made Modules
WIP
## Windowed Mode Border Fix
WIP

