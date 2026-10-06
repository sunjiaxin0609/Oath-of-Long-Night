# 长夜誓约 / Oath of Long Night

2D 等距视角动作 RPG。一次性买断，无抽卡，无内购。
目标平台：Windows（GOG + Steam），中文 / 英文。

## 项目状态

**设计阶段** — 见 `docs/核心设计文档.md`

当前进度：
- ✅ 核心设计文档 v0.1
- ⬜ Godot 项目骨架
- ⬜ P0 技术验证（手感）
- ⬜ GOG / Steam 商店页

## 目录结构

```
project.godot          Godot 项目配置
design/                主游戏工程
  scenes/              场景文件
  scripts/             GDScript
  data/                数值配置（Resource 格式）
  assets/
    sprites/           角色与敌人精灵
    fx/                特效
    audio/             音乐与音效
    fonts/             字体（中文字体需注意授权）
prototype/             手感原型，可随时丢弃
docs/                  设计文档
tools/                 工具脚本
```

## 开发环境

- **引擎**：Godot 4.3 或更高（[官网下载](https://godotengine.org/download)）
- **渲染后端**：GL Compatibility（兼容性最好，2D 足够用）
- **目标分辨率**：1280×720，stretch mode = canvas_items

### 首次运行

1. 安装 Godot 4.3+
2. 用 Godot 打开 `project.godot`
3. 首次打开时会提示缺少主场景，在 P0 原型完成后设置

### 导出 Windows 构建（GOG 上架需要）

1. `编辑器 → 管理导出模板` 下载 4.3 导出模板
2. `项目 → 导出` 添加 Windows Desktop 预设
3. 关闭 `binary_format/embed_pck`（GOG 偏好独立 pck，便于更新）
4. 输出目录用 `build/`

## 核心设计

一句话：**在一场吞没世界的长夜里，你与六个互不信任的誓约者签订有代价的契约，借他们的力量走到黎明。**

### 三个设计原则

1. **驱动力来自"代价"，不是"运气"** — 强力角色必须通过永久牺牲获得
2. **所有系统都能被看懂** — 无隐藏数值、无随机词条，Build 乐趣来自组合发现
3. **可通关，不逼氪，不逼肝** — 主线 15–20 小时，全收集约 40 小时

详细设计见 [docs/核心设计文档.md](docs/核心设计文档.md)

## 待决事项

- [ ] 主角是谁？是否可自定义外观？
- [ ] 是否需要城镇/据点地图，还是全程关卡内？
- [ ] 同时上场多角色，还是单角色切换？
- [ ] 是否支持手柄？
- [ ] 美术外包预算？
- [ ] 是否做免费 Demo 先行？