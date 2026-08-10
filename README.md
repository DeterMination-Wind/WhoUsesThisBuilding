# WhoUsesThisBuilding
<h1 align="center">
  <a href="https://github.com/DeterMination-Wind/WhoUsesThisBuilding/releases/latest"><img src="https://img.shields.io/github/v/release/DeterMination-Wind/WhoUsesThisBuilding?display_name=release&label=Latest%20Release&color=green"></a>
  <a href="https://github.com/DeterMination-Wind/WhoUsesThisBuilding/releases"><img src="https://img.shields.io/github/downloads/DeterMination-Wind/WhoUsesThisBuilding/total?label=Downloads&color=blue"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/DeterMination-Wind/WhoUsesThisBuilding?label=License"></a>
  <a href="https://github.com/DeterMination-Wind/WhoUsesThisBuilding"><img src="https://img.shields.io/github/stars/DeterMination-Wind/WhoUsesThisBuilding?style=flat&label=Star%20this%20mod!&color=yellow"></a>
</h1>

WhoUsesThisBuilding is a helper mod for Mindustry logic building workflow.  
It answers one practical question in seconds:

**"Which processors are using this building right now?"**

---

## 中文介绍

WhoUsesThisBuilding 是一个专注于“逻辑排查体验”的辅助模组。  
当你在地图中悬停到某个建筑并按下热键时，它会直接把“正在引用这个建筑”的逻辑处理器高亮出来，并给出简洁标签。

它适合这些场景：

- 逻辑工程太大，不知道某个建筑被谁在用
- 修改/替换建筑前，想先确认影响范围
- 游戏内编辑时，需要快速追踪逻辑引用关系
- 和队友协作排查逻辑问题时，想要一眼看懂结构

这个模组的目标不是改变逻辑玩法，而是让你在复杂逻辑图里定位更快、排错更轻松。

---

## English

WhoUsesThisBuilding is a quality-of-life mod for logic-heavy Mindustry maps.  
Hover a building, hold the hotkey, and it highlights processors that reference that building.

Great for:

- Large logic systems where dependencies are hard to track
- Safe refactoring before replacing/removing a building
- Fast reference tracing during in-game editing
- Team debugging sessions on shared maps

The goal is simple: **less hunting, faster understanding.**

---

## 设置 / Settings

可在游戏内设置界面（设置 → WhoUsesThisBuilding）中调整：

| 设置项 | 默认值 | 说明 |
| --- | --- | --- |
| 启用反向逻辑高亮 (Enable) | 开 | 总开关，关闭后清除所有高亮 |
| 触发热键 (Hotkey) | **Alt**（左 Alt） | 悬停建筑时按住即触发；点击可录制自定义按键 |
| 标签字体大小 (Font size) | 100% | 范围 **50% – 300%**，步进 5% |

- 热键可在设置中点击按钮重新录制，按 Esc 取消；存储与解析同时兼容左右 Alt（默认 `altleft`）。
- 标签格式：`LN(opcode)`，例如 `L20(sensor)`。

## 地图编辑器支持 / Map Editor Support

支持 Mindustry 地图编辑器：在编辑器内悬停建筑并按住热键同样生效，且会检查所有处理器（不限于己方队伍）。游戏内模式默认只分析己方队伍及特权处理器的逻辑。

## 构建与安装 / Build & Install

依赖：JDK 17+（字节码以 Java 8 目标编译），Mindustry `v155.4`（`minGameVersion: 154`），Windows/Linux/macOS 均可。

```bash
./gradlew jar          # 桌面版 → build/libs/WhoUsesThisBuildingDesktop.jar
./gradlew deploy       # 合并桌面+Android → build/libs/WhoUsesThisBuilding.jar，并复制到 dist/ 与 构建/ 目录
./gradlew zipMerged    # 打包 zip 发布产物
```

安装：将 `dist/WhoUsesThisBuilding.jar` 放入 Mindustry 模组目录并重启游戏（Steam 版为 `steamapps/common/Mindustry/mods`，桌面版为 `%appdata%/Mindustry/mods`）。Android 打包需要本机有 Android SDK（d8），否则 `deploy` 会回退为仅桌面产物。
