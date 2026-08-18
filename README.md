# WhoUsesThisBuilding / 谁在用这个建筑

> 从一个建筑反查依赖它的逻辑处理器，少找一会儿，多理解一点。

WhoUsesThisBuilding 是面向 Mindustry 逻辑创作的排错工具。当某个建筑被改动、替换或出现异常时，你可以直接从建筑反查哪些处理器正在使用它，而不必在整张地图里逐个打开处理器猜测依赖关系。

它适合大型逻辑图、多人地图维护和需要快速定位引用关系的创作者。显示结果只帮助你理解现有逻辑，不会自动修改程序。

## 使用

在游戏或地图编辑器中悬停建筑，按住模组热键即可查看引用它的处理器。热键和显示大小可在设置中调整。

## 构建与安装

需要 JDK 17+。将 Release 或 dist/ 中的模组 JAR 放入 Mindustry 的 mods 目录并重启游戏。

~~~powershell
.\gradlew.bat jar
.\gradlew.bat deploy
.\gradlew.bat zipMerged
~~~

## English

> Trace a building back to the processors that depend on it.

WhoUsesThisBuilding is a troubleshooting tool for Mindustry logic work. When a building changes or behaves unexpectedly, it shows which processors use that building so you can find the relevant logic without opening every processor on the map.

It is useful for large logic graphs, multiplayer map maintenance, and creators who need to understand dependencies quickly. The mod only explains the existing logic; it does not rewrite programs automatically.

## Usage

Hover a building in-game or in the map editor and hold the mod hotkey to inspect the processors that reference it. The hotkey and label size can be changed in the settings.

## Build and install

JDK 17+ is required. Put the release or dist/ JAR in Mindustry's mods directory and restart the game.

~~~powershell
.\gradlew.bat jar
.\gradlew.bat deploy
.\gradlew.bat zipMerged
~~~
