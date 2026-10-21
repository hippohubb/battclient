# MetzClient

Fabric utility client for **Minecraft 1.21.4** (client-side only).

## Modules

| Panel  | Modules |
|--------|---------|
| Combat | Auto Totem, Auto Hit |
| Misc   | Sprint, No Fall, Fast Place, Auto Eat, Anti AFK, Auto Walk, Auto Respawn |
| Render | **Base Finder**, **Sus Chunk**, **Storage ESP**, Player ESP, Mob ESP, Tracers, Fullbright |
| Client | ArrayList, Coords, **Low Res**, Self Destruct |

- **Base Finder** – boxes chunks with lots of chests/barrels/shulkers/furnaces/beds etc. and posts coords in chat.
- **Sus Chunk** – boxes chunks containing blocks that rarely generate naturally (planks, wool, glass, torches, redstone parts).
- **Storage ESP** – through-wall boxes on every storage block (colour-coded by type).
- **Low Res** – compact GUI, small logo, shorter scan radius and slower scans for weak PCs.
- The MetzClient logo is drawn in the **top-right** of the screen. Enabled modules list underneath it.

Open the GUI with **Right Shift** (rebind in Controls). Settings save to `config/metzclient.json`.

## Getting the .jar from GitHub

1. Create a new GitHub repo and push/upload this whole folder (keep the `.github` folder).
2. Open the repo's **Actions** tab → the *Build metzclient* workflow runs automatically.
3. When it finishes, open the run and download the **metzclient-jar** artifact. The jar in it is the mod
   (ignore the `-sources` jar).
4. To publish a downloadable release: `git tag v1.0.0 && git push --tags` – the jar gets attached to the release.

## Installing

1. Install [Fabric Loader](https://fabricmc.net/use/installer/) for 1.21.4.
2. Drop **Fabric API (1.21.4)** and `metzclient-1.0.0.jar` into your `.minecraft/mods` folder.

## Building locally

Needs JDK 21 and Gradle 8.12+:

```
gradle build
```

The jar lands in `build/libs/`. (Run `gradle wrapper` once if you want a `gradlew`.)

## Note

Many servers ban client-side ESP/automation mods. Use it where it's allowed (singleplayer, anarchy servers, your own).
