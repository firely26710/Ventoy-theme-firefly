# Firefly · 流萤 — Ventoy 主题 | A Ventoy Theme

> 崩坏：星穹铁道 × Ventoy ｜ Honkai: Star Rail × Ventoy


**语言 | Languages:** [中文](#中文) | [English](#English)

---

<a id="中文"></a>

# 中文

## 简介

以《崩坏：星穹铁道》中的角色「流萤（Firefly）」为主题设计的 Ventoy 启动菜单主题。整体采用靛紫夜幕色调的背景，搭配流萤标志性的荧光绿渐变选中条，菜单字体使用霞鹜文楷。

## 特性

- **流萤主题背景**：1920×1080 靛紫夜幕背景，适配任意分辨率（GRUB 自动缩放）
- **荧光绿选中条**：流萤标志性的荧光绿渐变，选中项字体放大并高亮为白色
- **文楷字体**：内置 12 / 14 / 16 / 18 四个字号，终端界面使用 14 号
- **Ventoy 功能提示**：热键提示（`@VTOY_HOTKEY_TIP@`）与内存模式状态（`@VTOY_MEM_DISK@`）显示
- **丰富图标**：`icons/` 目录内置 80 个发行版与功能图标
- **全屏终端**：终端界面使用文楷字体全屏显示，与整体风格统一

## 文件结构

```
firefly/
├── theme.txt          # 主题配置
├── background.png     # 背景图（1920×1080）
├── select_c.png       # 选中条中间段（456×45）
├── select_w.png       # 选中条左端
├── select_e.png       # 选中条右端
├── wenkai-12.pf2      # 文楷 12 号
├── wenkai-14.pf2      # 文楷 14 号（终端）
├── wenkai-16.pf2      # 文楷 16 号（菜单项）
├── wenkai-18.pf2      # 文楷 18 号（选中项 / 倒计时）
└── icons/             # 系统与功能图标
```

## 安装

三步点亮流萤 ✨

1. 把整个 `firefly` 文件夹复制到 Ventoy U 盘第一分区（就是平时放 ISO 的那个分区）：

   ```
   ventoy/theme/firefly/
   ```

2. 接下来二选一，告诉 Ventoy 换上这套主题：

   **方案 A：VentoyPlugson（官方推荐，点点就完事）**
   - 打开 Ventoy 自带的 `VentoyPlugson.exe`，选中你的 U 盘
   - 进入「Theme（主题）」插件
   - 主题文件填 `/ventoy/theme/firefly/theme.txt`
   - 分辨率填 `1920x1080`（背景图原生 1080p），显示模式保持 `GUI`
   - 保存更新，收工！

   **方案 B：手动改 `ventoy.json`（极客向）**
   - 打开 U 盘第一分区 `ventoy/ventoy.json`，加入：

   ```json
   {
       "theme": {
           "file": "/ventoy/theme/firefly/theme.txt",
           "gfxmode": "1920x1080",
           "display_mode": "GUI"
       }
   }
   ```

3. 重启，从 U 盘启动——流萤在等你 🌌

   想解锁更多姿势（多主题随机切换、按屏幕自动匹配分辨率等）？官方文档请戳：[Ventoy 主题插件说明](https://www.ventoy.net/cn/plugin_theme.html)

## 自定义

想给流萤换个造型？改改 `theme.txt` 就行，保存即生效，全程无痛 🎨

- **换背景**：直接替换 `background.png`（建议 1920×1080），或者改 `theme.txt` 里的 `desktop-image` 路径
- **改选中条**：替换 `select_c.png` / `select_w.png` / `select_e.png` 三段图片
- **改配色**：动 `theme.txt` 里的颜色值——菜单文字 `item_color`、选中文字 `selected_item_color`、倒计时文字 `color`（默认天蓝 `#4fc3f7`）
- **换字体**：把新字体用 `grub-mkfont` 转成 `.pf2` 丢进来，再同步改 `theme.txt` 里的字体引用
- **更多参数**：`gfxmode`、`display_mode`、多主题随机切换等完整说明见官方文档：[Ventoy 主题插件说明](https://www.ventoy.net/cn/plugin_theme.html)

## 背景分享

欢迎各位同好分享自己制作的流萤主题背景图！如果你有一张心仪的流萤背景并愿意与大家分享，可以通过以下方式投稿：

1. Fork 本仓库，将背景图放入 `DIY-backgrounds/` 目录（命名建议：`你的昵称-简短描述.png`）
2. 提交 Pull Request
3. 不方便使用 Git 的话，也可以在 Issues 中直接附上图片

**投稿小贴士：**
- 推荐分辨率 1920×1080，PNG 格式
- 人物主体尽量避开屏幕右侧 30% 区域（启动菜单所在位置），避免遮挡菜单
- 请注明图片来源（官方壁纸 / 授权画师作品 / 自绘等）

**使用分享的背景：** 下载后重命名为 `background.png` 替换主题目录中的原文件即可（或修改 `theme.txt` 中的 `desktop-image` 路径）。

投稿一经采纳，会展示在下方「同好投稿」列表中：

### 同好投稿

| 预览 | 作者 | 说明 |
| --- | --- | --- |
| 虚位以待～ |  |  |

## 致谢

- 《崩坏：星穹铁道》— 角色「流萤」© 米哈游 / HoYoverse
- 霞鹜文楷 [LXGW WenKai](https://github.com/lxgw/LxgwWenKai) — 主题字体
- [Ventoy](https://www.ventoy.net/) — 新一代多系统启动 U 盘解决方案

## 免责声明

本主题为个人制作的同人作品，与米哈游 / HoYoverse 无任何关联。角色「流萤」及相关元素版权归米哈游所有。本主题仅供个人学习与使用，请勿用于商业用途。

---

<a id="English"></a>

# English

## Introduction

A Ventoy boot menu theme inspired by **Firefly (流萤)**, the beloved character from **Honkai: Star Rail**. It features an indigo night-sky background and a selection bar in Firefly's signature glowing green. 
## Features

- **Firefly-themed background**: 1920×1080 indigo night tones; scales to any resolution
- **Firefly-green selection bar**: gradient in her signature glowing green; selected item enlarged and highlighted in white
- **WenKai fonts**: four sizes (12 / 14 / 16 / 18); terminal uses size 14
- **Ventoy info**: hotkey tips (`@VTOY_HOTKEY_TIP@`) and memdisk status (`@VTOY_MEM_DISK@`)
- **Rich icon set**: 80 distro and function icons in `icons/`
- **Full-screen terminal**: terminal themed with the WenKai font for a consistent look

## File Structure

```
firefly/
├── theme.txt          # theme configuration
├── background.png     # background image (1920×1080)
├── select_c.png       # selection bar center (456×45)
├── select_w.png       # selection bar left edge
├── select_e.png       # selection bar right edge
├── wenkai-12.pf2      # WenKai size 12
├── wenkai-14.pf2      # WenKai size 14 (terminal)
├── wenkai-16.pf2      # WenKai size 16 (menu items)
├── wenkai-18.pf2      # WenKai size 18 (selected item / countdown)
└── icons/             # system and function icons
```

## Installation

Three steps to light up Firefly on your boot screen ✨

1. Copy the entire `firefly` folder to the first partition of your Ventoy USB drive (the one where your ISO files live):

   ```
   ventoy/theme/firefly/
   ```

2. Pick your flavor to enable the theme:

   **Option A: VentoyPlugson (official, all point-and-click)**
   - Run `VentoyPlugson.exe` (ships with Ventoy) and select your USB drive
   - Open the **Theme** plugin
   - Set the theme file to `/ventoy/theme/firefly/theme.txt`
   - Set resolution to `1920x1080` (native size of the background), keep display mode as `GUI`
   - Save and update — you're done!

   **Option B: Edit `ventoy.json` by hand (for the tinkerers)**
   - Open `ventoy/ventoy.json` on the first partition and add:

   ```json
   {
       "theme": {
           "file": "/ventoy/theme/firefly/theme.txt",
           "gfxmode": "1920x1080",
           "display_mode": "GUI"
       }
   }
   ```

3. Reboot and boot from the USB drive — Firefly is waiting 🌌

   Want more (multiple themes with random pick, auto resolution matching, etc.)? See the official docs: [Ventoy Theme Plugin](https://www.ventoy.net/en/plugin_theme.html)

## Customization

Want to give Firefly a new look? It's all in `theme.txt` — edit, save, done 🎨

- **Change the background**: replace `background.png` (1920×1080 recommended), or edit the `desktop-image` path in `theme.txt`
- **Change the selection bar**: swap the three pieces `select_c.png` / `select_w.png` / `select_e.png`
- **Change colors**: edit the color values in `theme.txt` — `item_color` for menu text, `selected_item_color` for the highlighted item, `color` for the countdown (default sky-blue `#4fc3f7`)
- **Change fonts**: convert a new font to `.pf2` with `grub-mkfont`, drop it in, and update the font references in `theme.txt`
- **More parameters**: full details on `gfxmode`, `display_mode`, multi-theme random pick, etc. in the official docs: [Ventoy Theme Plugin](https://www.ventoy.net/en/plugin_theme.html)

## Background Sharing

Fellow Firefly fans are welcome to share their own custom backgrounds! If you have a favorite Firefly wallpaper you'd like to contribute:

1. Fork this repo and put your background into the `DIY-backgrounds/` directory (suggested naming: `your-name-short-description.png`)
2. Submit a Pull Request
3. Not comfortable with Git? You can also attach the image directly in an Issue

**Submission tips:**
- 1920×1080 recommended, PNG format
- Keep the main subject away from the right 30% of the screen (where the boot menu sits) to avoid overlapping the menu
- Please credit the image source (official wallpaper / artist-licensed work / your own art, etc.)

**To use a shared background:** download it, rename it to `background.png`, and replace the original file in the theme folder (or edit the `desktop-image` path in `theme.txt`).

Accepted submissions will be listed in the "Community Submissions" table below:

### Community Submissions

| Preview | Author | Notes |
| --- | --- | --- |
| Waiting for the first one~ |  |  |

## Credits

- *Honkai: Star Rail* — Character "Firefly" © miHoYo / HoYoverse
- [LXGW WenKai](https://github.com/lxgw/LxgwWenKai) — theme font
- [Ventoy](https://www.ventoy.net/) — the next-generation multi-boot USB solution

## Disclaimer

This is a fan-made theme and is not affiliated with or endorsed by miHoYo / HoYoverse. The character "Firefly" and related elements are the property of miHoYo. This theme is for personal use only and not for commercial purposes.
