---
title: "Space Engineers Mods"
layout: page
author: twizzork
pubDate: 2024-11-18T09:00:00
offset: UTC-7
---

# Space Engineers Mods

tldr; steam workshop links:
- [BetterOreDetectors (150m/450m)](https://steamcommunity.com/sharedfiles/filedetails/?id=3356554074)
- [PleaseShutUp (No Breathing Sounds on Realistic Audio)](https://steamcommunity.com/sharedfiles/filedetails/?id=3356553429)

<br/>

if you have any feedback or they break, let me know. i'll probably not play space engineers again until 2 releases 

## explanation of changes to sbc/xml files

if you download the mods, you can see the actual .sbc (its just xml) files that I changed

**ore detectors:**
- i changed the `CubeBlocks\CubeBlocks_Tools.sbc` file for the ore detectors, you can find them by looking for `MyObjectBuilder_OreDetectorDefinition` in the file, or `LargeOreDetector` and `SmallOreDetector`

**breathing:**
- i honestly didn't really test much for this. i used an existing but broken mod for reference, changed what i thought would fix the issue, and it worked out. look for `RealPlayVocBreath1L`, `RealPlayVocBreath2L`, `RealFemPlayVocBreath1L`, `RealFemPlayVocBreath2L`

## how to install single player and multiplayer

### singleplayer

- Subscribe to the mod, may need restart of game.
- On existing save: load game -> edit settings -> mods
- On new save: new game -> customize -> choose mods

### multiplayer

To add to a new dedicated server: Follow instructions for your provider or add the Mod ID to a list in an 'unsignedLong' tag, inside the 'SpaceEngineers-Dedicated.cfg' file:

```xml
<!-- ... -->
<Mods>
  <!-- add any other mod IDs for other mods you want as well -->
  <unsignedLong>3356554074</unsignedLong>
</Mods>
<!-- ... -->
```

To add to an existing dedicated server: Follow instructions for your server provider, or add the following to the 'Sandbox.sbc' file:

```xml
<!-- ... -->
<Mods>
  <ModItem FriendlyName="BetterOreDetectors (150m/450m)">
    <Name>3356554074.sbm</Name>
    <PublishedFileId>3356554074</PublishedFileId>
    <PublishedServiceName>Steam</PublishedServiceName>
    <IsDependency>true</IsDependency>
  </ModItem>
  <!-- other mods -->
</Mods>
<!-- ... -->
```
