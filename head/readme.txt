HeadBleed V2
Version: 0.9.6-beta

DESCRIPTION

HeadBleed V2 adds dynamic blood fountain effects to headshots in Red Dead Redemption 2.
It expands the original head bleed concept with configurable bleeding time, multiple blood fountain presets, post-mortem bleeding support, extra blood effects, projectile camera support, vehicle support, compatibility options, and an in-game settings menu.
It also includes blood pool controls, adjustable blood decal capacity, and optional improvements to vanilla dismemberment and meat chunk effects.

For progressive gore variants and custom head explosions, the separately released Head Bleed V2: Gore Framework add-on is recommended. See OPTIONAL GORE FRAMEWORK below.

If you enjoy this mod, don't forget to endorse it on Nexus Mods!

Join the official Head Bleed Discord community for early builds, development updates, technical support, and a place to share your feedback, ideas, and gameplay:
https://discord.gg/Tyx4eJP7X3

REQUIREMENTS

IMPORTANT: Head Bleed V2 requires ScriptHookRDR2 V2 AND its Mod Loader (ASI loader).
Download BOTH files from:
https://www.nexusmods.com/reddeadredemption2/mods/1472

Use this V2 setup for Head Bleed V2; the original ScriptHookRDR2 is not the supported setup for this release.
The ScriptHook Mod Loader is not Lenny's Mod Loader (LML). They serve different purposes.
LML is optional for standalone Head Bleed's custom logo, but required for the separate Gore Framework add-on.

Optional - you may use Ultimate ASI Loader for a more up to date ASI loader. Download Ultimate-ASI-Loader-NoPDB_x64.zip from:
https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases and use the default filename (dinput8.dll) from the .zip archive.
The Ultimate ASI Loader dinput8.dll will replace the dinput8.dll from the ScriptHookRDR2 V2 archive in your RDR2 install directory should you choose to install Ultimate ASI Loader.
INSTALLATION

1. Install both ScriptHookRDR2 V2 and its Mod Loader. Place ScriptHookRDR2.dll and dinput8.dll from those downloads next to RDR2.exe.

2. Extract the files from this archive into your Red Dead Redemption 2 game directory.

3. Start the game and press F11 to open the menu. This is the default key and can be changed in the menu.

If startup produces a black screen, see TROUBLESHOOTING below.

LOGO INSTALLATION

The custom logo requires Lenny's Mod Loader (LML):
https://www.rdr2mods.com/downloads/rdr2/tools/76-lennys-mod-loader-rdr/

The Head Bleed archive includes the logo at:
lml/stream/HeadBleedLogo.ytd

Extracting the archive into the game directory places it there automatically.
The logo is optional. Head Bleed's standalone features work without it.

MENU CONTROLS

Open / Close Menu
- F11 by default.
- Select Menu Toggle Key in the main menu, then press the desired key. Press Esc to cancel; reserved keys cannot be assigned.
- The binding is saved in HeadBleedFiles/Config/HeadBleedV2_tuning.ini under [General].
- You can also edit MenuToggleKey=F11 there while the mod is unloaded. Key names such as F10 or F11 can be used instead of numeric key codes.

Navigation
- Numpad 8 or Arrow Up = Up
- Numpad 2 or Arrow Down = Down
- Numpad 4 or Arrow Left = Decrease / Left
- Numpad 6 or Arrow Right = Increase / Right
- Numpad 5 or Enter = Enter / Select
- Numpad 0 or Backspace = Back
- Page Down by default = Open / close the full description of the selected option. Use Arrow Up/Down or Numpad 8/2 to scroll longer descriptions. Back or Esc also closes the description without leaving the current menu.
- Select Info Key in the main menu to rebind it, or edit MenuDescriptionKey=Page Down under [General] in HeadBleedFiles/Config/HeadBleedV2_tuning.ini while the mod is unloaded. Names such as Page Up or End are supported. The menu hints update to match your binding.
- Menu Toggle Key and Info Key must use different keys. If the INI assigns both to the same key, the menu toggle is kept and the description falls back to Page Down (or Page Up if Page Down opens the menu).

Extra Controls
- Numpad + or + = Save custom blood fountain preset
- Numpad - or - = Delete selected custom preset
- Numpad * or . = Pause / resume soundtrack

SETTINGS OVERVIEW

The settings described in this section belong to Head Bleed V2 itself and do not require the Gore Framework asset add-on.

Bleeding Time & Chance
- Choose how long the bleeding effect should last.
- Supports both fixed and random bleeding time.
- Post-mortem bleeding time can be adjusted separately as a percentage of regular bleeding time.
- Post-mortem bleeding intensity can also be adjusted separately. Fatal first hits retain normal intensity.
- Adjust the chance for head bleeding to trigger.
- Blood Reserve can optionally limit how much blood each ped can lose.
- Max Blood Reserve sets the starting reserve per ped.
- Blood Reserve Drain / s controls how quickly the reserve is drained while a bleeding effect is active.
- Neck Stump Reserve restores a minimum reserve for neck stump bleeding when the head is removed after the ped has already bled out.
- Bleed Lock can keep an active head bleed at its current wound position instead of moving it to new headshot impacts.

Blood Flow
- Natural gradually reduces the bleeding effect throughout its duration.
- Late Fade keeps the effect stronger until the final part of the bleed.
- Mixed randomly selects either behavior with equal chance for each new bleed.

Small Caliber Head Gore
- Optional setting in the General menu.
- When disabled, small caliber headshots no longer cause head explosions.
- Applies to pistols, revolvers, repeaters, and rifles.
- Shotguns and sniper rifles can still cause head gore.

Blood Fountain Presets
- Multiple blood fountain presets are included.
- Presets change the overall fountain behavior, including pressure, pulse, and direction.
- Custom presets can also be created, saved, and added to the dynamic preset pool.

Blood Pools
- Head Bleed adds custom pools for supported bleeding, fatal body shots, and melee kills, including recognized executions.
- Manually placed pools wait for the body and wound position to settle instead of immediately starting where the ped was first hit.
- Blood Pool Speed adjusts the buildup and expansion speed of new normal ped pools, including the shared vanilla/PDOR pool path. Existing pools are unaffected.
- Blood Pool Fix fixes a vanilla bug where arterial blood pools expand too rapidly. These pools will follow your Blood Pool Speed setting. Turning it off does not disable Head Bleed's normal replacement pools.
- Separate Blood Pools allows nearby wounds and severed limbs to form individual pools instead of merging. Changes affect new pools.

Blood Decals
- Increase Blood Decals adjusts blood decal capacity on peds in real time. The default is 400%.
- Lowering the capacity does not immediately erase existing wounds.
- Decal Slot Cleanup frees up blood and dirt decal slots to make room for new bullet wounds. Especially useful at decal capacities below 200%.
- Replace Old Wounds additionally allows new hits to replace older bullet wounds when space is limited. Especially useful at decal capacities below 200%. It requires Decal Slot Cleanup and does not remove bullet wounds while idle.
- IMPORTANT: If another mod also patches decal slots, disable Head Bleed's slot expansion before using them together. See COMPATIBILITY below.

General Gore Settings
- These options are available in the Gore menu independently of the optional Gore Framework add-on.
- Meat Chunk Fix adjusts collision, bounce, damping, rotation, and blood-flake behavior for supported vanilla effects.
- Meat Chunk Lifetime controls how long newly spawned meat chunks and solid bits remain, from 1 to 120 seconds. It works independently of Meat Chunk Fix.
- Full Limb Dismemberment allows gunfire to sever upper arms and thighs instead of restricting those areas to explosions. Turning it off restores that restriction without undoing existing damage.
- Preserve Severed Limbs prevents detached body parts from disappearing when shot. It does not restore parts that have already disappeared.

PDOR Compatibility
- A collaborative effort has been put forth between PDO Reloaded and Head Bleed V2 to achieve a high level of compatibility.
- To use Head Bleed V2 with PDO Reloaded ensure that the 'PDO Reloaded' compatibility option is enabled inside of the Head Bleed V2 'Compatibility' menu.
- When PDO Reloaded compatibility is enabled in Head Bleed V2:
	- PDO Reloaded determines whether a head shot will be an 'Enhanced Head Shot' (EHS) or a 'Vanilla' head shot based upon your configuration of the 'Enhanced Head Shot' chance in the PDO Reloaded settings.
	- Head Bleed V2 detects whether PDO Reloaded selects an 'Enhanced Head Shot (EHS)' or a 'Vanilla' head shot. Head Bleed V2 only activates in all scenarios for 'Vanilla' head shots. 
	- Inside of the PDO Reloaded 'Enhanced Systems' menu you can set the percentage chance PDO Reloaded will consider a head shot 'Enhanced' or 'Vanilla'. If you want Head Bleed V2 to activate on all head shots then set PDO Reloaded for 100% 'Vanilla' head shots.
	- If you remove or disable PDO Reloaded be sure to disable the PDO Reloaded compatibility option inside of Head Bleed V2. 
- Find the dedicated settings under Compatibility > PDO Reloaded. Enable PDOR compatibility when using Ped Damage Overhaul Reloaded, and disable it otherwise.
- When enabled, Head Bleed V2 stays out of living headshot handling and lets PDOR use its own dying states, except for peds in vehicles where Head Bleed V2 handles the headshot fallback.
- PDOR Vanilla Head Bleed can be enabled to add Head Bleed V2 effects to PDOR's vanilla headshot detection. Post-mortem hits can still trigger Head Bleed's post-mortem effects regardless of this setting.
- PDOR vanilla headshots use the global Bleeding Chance setting; there is no separate PDOR bleeding chance setting.
- PDOR Vanilla Force Kill controls whether PDOR vanilla headshot peds should be killed instantly. Available modes are Always, Bleeding Only, and Off.
- Decapitations and head explosions are supported with neck stump bleeding.

Extra Blood
- Optional extra blood decals and blood splatter effects.
- Includes selectable decal behavior and blood splatter intensity settings.

Projectile Cam
- Optional cinematic projectile camera for arrows, tomahawks, and throwing knives.
- Projectile Cam modes:
  Off, Hit Chance, and Always.
- Hit Chance starts the camera only when the mod predicts a likely hit.
- Always starts the camera for supported projectile launches and can use Target Only, No Target Timeout, or Cinematic Flight behavior.
- Supports projectile killcams with Headshots or All Kills modes.
- Killcam Trigger can be set to Always or Projectile Cam only.
- Optional HUD hiding and temporary player invincibility can be enabled during projectile camera playback.
- Arrow Cam Min Distance and Arrow Cam Max Distance control the target distance range for arrow Projectile Cam activation.
- Thrown Cam Min Distance and Thrown Cam Max Distance control the target distance range for tomahawk and throwing knife Projectile Cam activation.
- A max distance value of 0 disables the upper distance limit.

Soundtrack
- Optional background soundtrack support for the menu and in-game use.
- Volume can be adjusted in the menu.
- The soundtrack can be paused or resumed with the assigned hotkey.

Slow Motion
- Optional slow motion support.
- Can be set to activate while aiming or stay active at all times.

OPTIONAL GORE FRAMEWORK

Head Bleed V2: Gore Framework is a separately distributed, optional add-on that expands Head Bleed's blood effects with progressive gore variants and custom head explosions.

Head Bleed V2 provides the gameplay logic; Gore Framework adds the required LML assets and gore zone configuration. No additional ASI is needed.

The two packages are versioned and updated separately. See the add-on's readme for installation instructions, Head Bleed version requirements, variant settings, and Enhanced Brawling decapitation compatibility.

You can find Gore Framework under Gore in the Head Bleed menu. Its Add-on Status must show Ready before you can enable it. Head Bleed's standalone features remain available without the add-on.

Download Gore Framework:
https://www.nexusmods.com/reddeadredemption2/mods/11240

RECOMMENDED MODS

For an even bloodier experience, I highly recommend checking out these mods:

- Improvements in Blood by Cazanu
  url=https://www.nexusmods.com/reddeadredemption2/mods/2371
- Dynamic Blood V1 by robindubronx
  https://www.nexusmods.com/reddeadredemption2/mods/10672
- Ped Damage Overhaul Reloaded by MikeStarkweather
  https://www.nexusmods.com/reddeadredemption2/mods/6635
- Enhanced Brawling by 14N001st
  https://www.nexusmods.com/reddeadredemption2/mods/1662

These are optional recommendations, not requirements. Follow each mod's own installation and compatibility instructions.

COMPATIBILITY

Other Decal Slot Mods
- If you use another mod that modifies decal slots, such as Blood & Wounds, open:
  HeadBleedFiles/Config/HeadBleedV2_tuning.ini
- Under the existing [General] section, set:
  EnableDecalSlotExpansion=false
- A FULL GAME RESTART is required. Reloading the ASI or lowering Increase Blood Decals is not a substitute for disabling this startup patch.
- This switch disables Head Bleed's decal slot expansion, not the entire mod.

TROUBLESHOOTING

Black Screen
- Verify that both ScriptHookRDR2 V2 and its Mod Loader are installed.
- If you encounter a black screen, try setting [Interface] Enable = false in the ScriptHookConfig configuration INI, then restart the game.
- This is a ScriptHook setting, not a Head Bleed tuning option. It is a workaround to try, not a fix for every possible black screen.

SCRIPT HOOK RDR2 ERROR
- Verify you only have the required ScriptHookRDR2 V2 (ScriptHookRDR2.dll) and its mod loader (dinput8.dll) or the optional Ultimate ASI Loader (dinput8.dll). 
- Having multiple Script Hooks and ASI loaders will typically cause issues unless you have explicitly made accommodations for having multiple Script Hooks. Multiple ASI loaders are not supported.
- ScriptHookRDR2 V2 (ScriptHookRDR2.dll) is approximately 4.45MB at the time of this writing. If your ScriptHookRDR2.dll file is a different size you most likely have an out of date file.

Unreadable Menu Text
- If your game language does not render the custom menu font correctly, open HeadBleedFiles/Config/HeadBleedV2_tuning.ini and set PlainMenuText=1 under [General].

Menu Does Not Open
- F11 is only the default. Check MenuToggleKey under [General] if you have changed the binding.
- To reset it, unload the mod or close the game, set MenuToggleKey=F11, then load the mod again.

Gore Framework Shows Unconfirmed
- Check the add-on installation and make sure the mod is enabled in LML.
- Restart the game after installing or changing streamed assets; an ASI reload alone is not sufficient.
- For further diagnosis, provide HeadBleedV2.log, vfs.log, and ModManager.log from the same game session.

SUPPORT

For support, feedback, bug reports, and update news, join the official Head Bleed Discord server:
https://discord.gg/Tyx4eJP7X3

When reporting a bug, include your Head Bleed version, whether Gore Framework is installed, relevant settings, other mods, and steps to reproduce it. A short video is helpful for hit detection or execution issues.
Enable Debug Log before reproducing an issue when a diagnostic log is needed, then include HeadBleedV2.log from that session.

CREDITS

Head Bleed V2 design and development by iXzellent.

You may not copy, reuse, modify, redistribute, or incorporate my code into other projects without my prior permission. This includes code extracted or reconstructed from the ASI through decompilation, disassembly, or other reverse-engineering methods.

Absolutely no thanks at all, none whatsoever, to episiotomy <3

And thanks to everyone in the community who tried the early builds, reported bugs, and shared suggestions. Your feedback is always appreciated.

DEVELOPMENT NOTE

Head Bleed V2 is developed by iXzellent with AI assistance for coding, debugging, and technical research. I direct the project, evaluate proposed changes, and test the mod in-game alongside community testers. Design decisions and responsibility for releases remain mine.

SUPPORT DEVELOPMENT

If you'd like to support the ongoing development of Head Bleed, you can do so on Patreon. Your support is appreciated, but never required:
https://www.patreon.com/c/iXzellent
