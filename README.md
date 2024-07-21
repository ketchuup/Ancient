## Installation

1. Run `forge-1.7.10-10.13.4.1614-1.7.10-installer.jar` to install Forge for Minecraft 1.7.10.

2. Create new empty directory.

3. In Minecraft Lanucher create new installation with version `1.7.10-Forge10.13.4.1614-1.7.10` and select created directory as game directory.

4. Copy `mods`, `config`, `hats` and `resourcepacks` directories to game directory.

5. Run created installation.

6. In `Options` > `Resource Packs` select `Faithful 32x - 1.7.10.zip` and `Aether b.1.7.3 Textures` resouce packs.

7. Create new world using `Biomes O' Plenty` generator.

## Optimizations

### Use dedicated graphics card

#### NVIDIA graphics card

1. Open NVIDIA Control Panel.

2. Go to `3D Settings` > `Manage 3D settings` > `Program Settings`.

3. Click `Add` to add new program and select `javaw.exe` used to run Minecraft.
If you are using bundled Java Runtime, your `javaw.exe` is in `C:\Program Files (x86)\Minecraft Launcher\runtime\jre-legacy\windows-x64\jre-legacy\bin` directory.

4. Select `High-performance NVIDIA processor` as preferred graphics processor.

5. Apply settings.

#### AMD graphics card

¯\\\_(ツ)_/¯

---

### Better garbage collector configuration

Try to use the following JVM arguments ([explanation](https://www.reddit.com/r/feedthebeast/comments/5jhuk9/modded_mc_and_memory_usage_a_history_with_a/)):

```
-XX:+UseG1GC -Xmx4G -Xms4G -Dsun.rmi.dgc.server.gcInterval=2147483646 -XX:+UnlockExperimentalVMOptions -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M
```