Head Bleed V2: Gore Framework
Version: 1.0

DESCRIPTION

Gore Framework is an optional add-on for Head Bleed V2 that adds progressive head gore variants and custom head explosions to Red Dead Redemption 2.
Instead of treating every eligible headshot the same way, it uses hit location, weapon, ammunition, and existing damage to select supported gore outcomes. Further hits can progress an existing injury, including after death.
The add-on combines custom head models and internal gore with Head Bleed's blood fountains, particle effects, and blood pools.

Gore Framework requires Head Bleed V2, which provides the gameplay logic, while this package supplies the LML assets and gore zone configuration.

Gore variant design, custom modeling, mesh editing, and in-game integration by iXzellent. These assets may not be reused, redistributed, or included in other mods without my prior permission.

If you enjoy this add-on, don't forget to endorse it on Nexus Mods!

Join the official Head Bleed Discord community for early builds, development updates, technical support, and a place to share your feedback, ideas, and gameplay:
https://discord.gg/Tyx4eJP7X3

REQUIREMENTS

Head Bleed V2
- Install the latest Head Bleed V2 release for the current features and fixes.
https://www.nexusmods.com/reddeadredemption2/mods/9071
- Head Bleed and Gore Framework are versioned separately. Their version numbers do not need to match.
- An older Head Bleed build may not recognize newer variants or features in a newer Gore Framework package. This does not automatically make the entire add-on incompatible.

Lenny's Mod Loader (LML)
- IMPORTANT: Make sure you have installed the latest LML version, including its game-side loader files. Having only the Mod Manager application is not enough.
https://www.rdr2mods.com/downloads/rdr2/tools/76-lennys-mod-loader-rdr/

ScriptHookRDR2 V2 and its Mod Loader
- Head Bleed requires BOTH ScriptHookRDR2 V2 and the Mod Loader (ASI loader) offered on its download page.
- Install ScriptHookRDR2.dll and dinput8.dll next to RDR2.exe.
- The ScriptHook Mod Loader and LML are separate requirements; neither replaces the other.
https://www.nexusmods.com/reddeadredemption2/mods/1472

Optional - you may use Ultimate ASI Loader for a more up to date ASI loader. Download Ultimate-ASI-Loader-NoPDB_x64.zip from:
https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases and use the default filename (dinput8.dll) from the .zip archive.
The Ultimate ASI Loader dinput8.dll will replace the dinput8.dll from the ScriptHookRDR2 V2 archive in your RDR2 install directory should you choose to install Ultimate ASI Loader.

INSTALLATION

1. Install Head Bleed V2 and all requirements above.

2. Close the game, then extract the Gore Framework archive into the Red Dead Redemption 2 game directory, where RDR2.exe is located. Preserve the archive's folder structure.

3. Check these paths:
   lml/HeadBleedV2_GoreFramework/install.xml
   lml/HeadBleedV2_GoreFramework/assets_drawable.ymt
   lml/HeadBleedV2_GoreFramework/gore_entries.xml
   lml/HeadBleedV2_GoreFramework/stream/
   HeadBleedFiles/Config/HeadBleedV2_gore_zones.ini

   The stream folder contains the models, textures, and hb_gore_props.ytyp. Keep the supplied install.xml references intact. Do not create an extra lml/lml folder.
   gore_entries.xml is used by the Head Bleed Asset Patcher to create compatibility patches for other mods that modify assets_drawable.ymt. You do not need to load this file manually in the game. See the COMPATIBILITY section below for details.

4. Make sure HeadBleedV2_GoreFramework is enabled in LML. If another mod replaces assets_drawable.ymt, read COMPATIBILITY before testing.

5. Start the game. Open the Head Bleed menu with F11, or your rebound menu key, and go to Gore > Gore Framework.

6. Allow the installation check to finish after gameplay has loaded. Add-on Status must show Ready before Gore Framework can be enabled. Check that the Gore Framework toggle is On.

Installing or updating streamed assets requires a FULL GAME RESTART. Reloading HeadBleedV2.asi alone does not reload these files.

FIRST TEST

- Use a fresh, ordinary NPC, not a cutscene character model.
- With Gore Framework enabled, try a close-range headshot using a rifle or a shotgun loaded with regular shells.
- The result depends on the hit zone and your settings; a particular shot is not guaranteed to produce a particular variant.
- Check that both the external head injury and its internal gore render correctly. Ready verifies base assets, not every individual variant or compatibility combination.

FEATURES & SETTINGS

Gore Variants and Progression
- Includes injuries such as Harelip, Cyclops stages, Nose Blown, jaw damage variants, Dental Plan, and Top Off.
- Supported male and female NPCs use the corresponding available assets.
- Variants use defined hit zones and weapon/ammunition rules. Not every weapon can trigger every variant at every location.
- Further eligible hits can progress existing damage rather than selecting an unrelated starting variant.
- Progression also works on corpses. Not every variant can progress into every other variant.

Gore Zone Visuals and Size
- Gore Zone Visuals displays trigger zones while aiming at a ped, useful for checking where a variant can be triggered.
- Gore Zone Size lets you choose the default zones or smaller alternatives. Zones without a smaller alternative retain their default shape.

Shotgun and Sniper Chances
- Shotgun Chance and Sniper Chance control the chance for eligible headshots to trigger a variant instead of a head explosion.
- These settings do not bypass weapon restrictions, hit-zone requirements, or head explosion rules.
- Shotgun Max Distance limits variant triggers and progression from shotgun SHELLS. Its default is 10 meters.
- Shotgun slugs are not affected by that distance limit.
- Shotgun Max Distance is separate from head explosion distances and PDOR distance synchronization.

Custom Head Explosions
- Head Explode Settings provides weapon-specific headshot counts, including separate shotgun shell and slug rules.
- Setting a weapon's hit count to 0 disables that weapon's hit-count rule; it is not a universal switch for every execution or explosive-ammunition outcome.
- Shotgun and sniper distance settings define range brackets and chances after the relevant hit count is reached.
- Small Caliber Head Gore is the same setting exposed in Head Bleed's General menu; the two controls stay synchronized.
- Head explosions handle head components and supported custom headwear replacements as part of the effect.

Executions
- Recognized firearm execution animations use dedicated outcomes based on the move, weapon, and ammunition.
- Known head executions can trigger variants or custom head explosions. Recognized body executions are not treated as headshots simply because an execution occurred.
- Under the Gore Framework execution rules, explosive ammunition overrides the normal variant choice with a head explosion for recognized head executions.
- The Executions setting offers Gore Framework, Mixed, and Vanilla behavior. Mixed adds a 50% vanilla outcome for the other weapon groups while keeping shotgun/sniper behavior unchanged. Vanilla disables the custom execution overrides.
- Recognition covers the animations currently mapped in Head Bleed, not every possible animation added by another mod. The executions enabled by Enhanced Brawling in a non-combat stance should be fully mapped.

Fatal Wounds and Survivor Writhe
- Fatal gore variants and custom head explosions kill immediately and suppress vanilla writhe behavior.
- Survivor Writhe applies to eligible surviving gore wounds, with configurable chance and duration.
- Writhe Duration controls the bleedout time, from 5 to 60 seconds. Additional damage can shorten it.
- Writhe Chance determines how likely an eligible survivor is to enter a writhing state.
- With PDOR compatibility enabled, survivor eligibility is limited to PDOR vanilla headshots.

Blood Effects and General Gore Options
- Blood fountains, bleeding duration, Blood Reserve, extra blood effects, and pool behavior use Head Bleed's settings. See its readme for those controls.
- Meat Chunk Fix, Meat Chunk Lifetime, Full Limb Dismemberment, and Preserve Severed Limbs belong to Head Bleed itself. They do not require the Gore Framework assets, even though they share the Gore menu.

COMPATIBILITY

Other Mods Replacing assets_drawable.ymt
- Gore Framework adds custom entries to assets_drawable.ymt. Another replacement of the same file can hide those entries, or lose the other mod's entries if Gore Framework wins instead.
- Changing load order alone does not merge both files. Use a matching compatibility patch when needed.
- The Head Bleed Asset Patcher can merge the supplied gore_entries.xml into a target mod's XML assets_drawable.ymt. It does not accept binary target YMTs or convert them automatically.
- Select the Gore Framework LML folder containing gore_entries.xml, the target mod folder, and a new or empty output folder outside both input folders. Preview the merge and review any conflicts before creating a patch.
- Install the generated patch in lml and load it after both source mods. Restart the game.
- The patcher leaves the input mods unchanged. It does not automatically resolve conflicts between multiple unrelated mods; use an existing combined compatibility mod as the target when appropriate.
- Keep gore_entries.xml matched to your installed Gore Framework package. Recheck or regenerate compatibility patches after asset updates.

PDO Reloaded
- Configure this under Compatibility > PDO Reloaded in the Head Bleed menu.
- With Gore Framework Priority Off, initial gore is limited to PDOR 'Vanilla' headshots and executions. Turning Gore Framework Priority On permits eligible variants to trigger for PDOR 'Enhanced Head Shots' allowing a ped to enter a PDOR 'Dying State' with a Gore Framework variant applied.
- When PDO Reloaded compatibility is enabled in Head Bleed V2:
	- PDO Reloaded determines whether a head shot will be an 'Enhanced Head Shot' (EHS) or a 'Vanilla' head shot based upon your configuration of the 'Enhanced Head Shot' chance in the PDO Reloaded settings.
	- Head Bleed V2 detects whether PDO Reloaded selects an 'Enhanced Head Shot (EHS)' or a 'Vanilla' head shot. Gore Framework only activates in all scenarios for 'Vanilla' head shots.
	- Inside of the PDO Reloaded 'Enhanced Systems' menu you can set the percentage chance PDO Reloaded will consider a head shot 'Enhanced' or 'Vanilla'. If you want Gore Framework to activate for all gore zone shots on living peds then set PDO Reloaded for 100% 'Vanilla' head shots.
- Post-mortem hits remain eligible regardless of that priority setting. Weapon and progression rules still apply.
- The PDOR distance synchronization option uses PDOR's shotgun/sniper head explosion distance and chance settings instead of Head Bleed's values. It does not replace Shotgun Max Distance for variants.

Enhanced Brawling
- Configure this under Compatibility > Enhanced Brawling.
- Enable the compatibility switch to route EB's supported decapitation move to the custom Gore Framework head explosion while retaining the vanilla-gore suppression.
- The optional jaw-variant setting replaces that outcome with a 50/50 choice of Jaw Drop Left or Dental Plan. Existing gore variants are preserved.
- This integration requires a supported EB build. It is not a general switch for firearm executions: recognized firearm execution rules work independently of it, including when those moves occur in vanilla combat.

Decal Slot Mods
- Gore Framework does not need a second decal slot patch.
- If another mod modifies decal slots, disable Head Bleed's expansion by setting EnableDecalSlotExpansion=false under [General] in HeadBleedFiles/Config/HeadBleedV2_tuning.ini, then fully restart the game.
- See the Head Bleed readme for the complete decal settings and compatibility notes.

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

These are optional recommendations, not requirements for Gore Framework.

LIMITATIONS

- Known cutscene ped models are temporarily excluded from gore variants and custom head explosions. Their rigs need additional work.
- Custom character models and modified head components are not guaranteed to fit the supplied assets.
- Some execution animations may not yet be supported. If an execution doesn't trigger the expected gore effect, please report it with a diagnostic log. A short video can also help, but isn't required.
- The installation check verifies representative assets and the gore zone configuration, not the entire package. A Ready status does not guarantee that every optional asset or external compatibility patch is correct.

TROUBLESHOOTING

Add-on Status: Waiting or Checking
- Let gameplay finish loading and allow the check to complete. It may retry for around 30 seconds of active checking before reporting Unconfirmed.

Add-on Status: Check INI
- Verify HeadBleedFiles/Config/HeadBleedV2_gore_zones.ini is installed from this package.
- This status can mean the file is missing, unreadable, or contains no zones recognized by the installed Head Bleed build.

Add-on Status: Unconfirmed
- Make sure the latest LML game-side files are installed and the Gore Framework mod is enabled.
- Check the folder structure, stream files, and install.xml references. Keep hb_gore_props.ytyp in the supplied stream layout and retain its DLC_ITYP_REQUEST entry.
- Check for another mod overriding assets_drawable.ymt and install a suitable compatibility patch if needed.
- Fully restart after correcting asset installation. Files appearing in ModManager.log or being queued in vfs.log do not alone prove that the game registered and loaded them.
- Unconfirmed means the base-asset check did not succeed; it does not identify the exact cause by itself.

Missing Internal Gore or Incorrect Components
- Check that the complete stream folder is installed, including YDR props, textures, and the YTYP.
- Avoid mixing files from different releases or leaving old test copies active in another LML folder.
- Confirm that any generated compatibility patch uses the gore_entries.xml supplied with your installed version.

Missing Menu Logo
- If the Head Bleed menu opens but its logo is missing, check that HeadBleedLogo.ytd is present in lml/stream and that LML is installed and working.
- If the logo is missing and Gore Framework also remains Unconfirmed, LML may not be loading the custom assets correctly. See the installation checks above.
- Alternatively, you can move HeadBleedLogo.ytd into the Gore Framework mod's stream folder. Keep only one copy and restart the game after moving it. The logo will then only load while the Gore Framework mod is enabled in LML.

Crash When Loading a Save
- Make sure both ScriptHookRDR2 V2 and its Mod Loader are installed.

Black Screen
- Try setting Interface=False in the ScriptHook configuration INI, then restart the game. This may resolve black screens caused by the ScriptHook interface.

UPDATING & REMOVAL

- Close the game before replacing streamed assets. Back up any settings you want to retain.
- Update the Gore Framework mod folder. Replace HeadBleedV2_gore_zones.ini when the update adds new variants or includes changes to the gore zones. Avoid leaving multiple releases enabled in LML.
- Check compatibility patches after an update; a patch generated from older entries can override the new metadata.
- Head Bleed and Gore Framework updates are separate. New asset variants may require a newer Head Bleed build to use them, without invalidating the variants an older build already recognizes.
- To remove the add-on, turn Gore Framework Off in the HB menu, close the game, and disable/remove its LML folder and GF-specific compatibility patches. Leave Head Bleed's own ASI and settings in place if you want to keep using standalone HB.
- If you moved the HB logo into the GF folder, move it back to lml/stream before removing that folder.

SUPPORT

For technical support, feedback, bug reports, and development news, join the official Head Bleed Discord server:
https://discord.gg/Tyx4eJP7X3

Include your Head Bleed and Gore Framework versions, relevant settings, other mods, and steps to reproduce the issue. For execution problems, include the weapon, ammunition, visible hit location, and ideally a short video.
Enable Debug Log in Head Bleed before reproducing the issue. For installation problems, provide HeadBleedV2.log, vfs.log, and ModManager.log from the SAME game session.

CREDITS

Gore variant design, custom modeling, mesh editing, and in-game integration by iXzellent. These assets may not be reused, redistributed, or included in other mods without my prior permission.

I emphatically do not give any special thanks to: episiotomy.
Seriously though, a huge thank you to episiotomy, who has been there throughout development: testing countless builds, helping track down bugs, verifying fixes, and suggesting features and improvements that helped shape Gore Framework. Thanks for sticking with me through all the “one more test” moments. You’re a true pard.

And thanks to everyone in the community who tried the early builds, reported bugs, and shared suggestions. Your feedback is always appreciated.

SUPPORT DEVELOPMENT

If you'd like to support the ongoing development of Head Bleed and Gore Framework, you can do so on Patreon. Your support is appreciated, but never required:
https://www.patreon.com/c/iXzellent

DEVELOPMENT NOTE

Head Bleed V2 and Gore Framework are developed by iXzellent with AI assistance for coding, debugging, and technical research. I direct the project, evaluate proposed changes, and test the mod in-game alongside community testers. Design decisions and responsibility for releases remain mine.
I especially do not thank episiotomy.
