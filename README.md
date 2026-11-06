# KeelBar

**给 Mac 加一个真正的任务栏。** 每个打开的窗口一个按钮：点一下前置，再点一下最小化。适合从 Windows 转到 Mac、窗口一多就找不到的人。

[English](#english) · [下载](../../releases/latest) · [更新日志](CHANGELOG.md)

![KeelBar 演示](assets/demo.gif)

哔哩哔哩视频介绍：
https://t.bilibili.com/1267609037079314437?share_source=pc_native

## 功能

- **窗口任务条**：屏幕底部列出所有打开的窗口（不是应用），单击前置，再点最小化。
- **悬停预览**：鼠标停在任务条上，显示窗口缩略图和完整标题。
- **未读提醒**：Teams、Outlook、微信等有未读时，任务条显示数字角标和橙色流光，点击后停止。可在设置里改为转指定圈数或关闭。
- **相同应用合并**：可选，每个应用一个按钮，点开再选窗口。
- **快捷方式**：左侧可固定应用和文件夹，内置“应用程序”“系统设置”“Dock 应用”“最近使用”。
- **窗口避让**：窗口最大化时自动停在任务栏上方，不被遮挡；双击标题栏可最大化和还原。
- **多显示器**：每个显示器一条任务栏，也可以只在主显示器显示。
- **外观**：一行或两行布局，可调背景透明度、字体颜色，可为每个应用单独设置任务条颜色。
- **其他**：最右侧细条一键最小化全部窗口；可隐藏系统 Dock，退出 KeelBar 后自动恢复。
- **语言**：English、中文、日本語、한국어。

## 系统要求

- macOS 14 Sonoma 或更高版本
- Apple 芯片（M1 及以后）。暂不支持 Intel Mac。

## 安装

1. 在 [Releases](../../releases/latest) 下载 `KeelBar-x.x-xxx.zip`，解压。
2. 把 `KeelBar.app` 拖到「应用程序」文件夹。不要在 iCloud、OneDrive 等同步目录里直接运行。
3. 双击打开。KeelBar 还没有经过 Apple 公证，第一次打开会被系统拦截：
   - **macOS 15 及以后**：先双击一次，在提示框里点「完成」；然后打开「系统设置 → 隐私与安全性」，在页面底部找到 KeelBar，点「仍要打开」，输入密码确认。
   - **macOS 14**：按住 Control 点击 `KeelBar.app`，选择「打开」，再点「打开」。
4. 按 KeelBar 弹出的提示授予两项权限（见下文）。授权后会自动生效，一般不需要重启。

> 每次启动时，KeelBar 会先把所有窗口最小化，从任务栏重新开始。窗口不会被关闭，点任务条即可还原。

> 也可以下载后在“终端”里执行 `xattr -dr com.apple.quarantine /Applications/KeelBar.app` 解除隔离，再双击打开。

可以用 Releases 页面里的 `SHA256SUMS.txt` 校验下载文件：

```bash
shasum -a 256 KeelBar-*.zip
```

## 需要的权限，以及为什么

| 权限 | 用途 |
|---|---|
| 辅助功能 | 读取窗口列表和标题，执行前置、最小化、关闭和窗口避让。没有它 KeelBar 无法工作。 |
| 屏幕与系统音频录制 | 只用于生成悬停预览的窗口缩略图。不授权也能用，只是预览没有画面。 |

在「系统设置 → 隐私与安全性」里，请添加 `KeelBar.app` 本身，不要选应用包里面的可执行文件。

## 隐私

- **完全在本机运行，不联网**，没有统计、没有崩溃上报、没有自动更新检查。
- 窗口缩略图只在内存中显示，不保存、不上传。
- 设置保存在本机的 `~/Library/Preferences/com.leowang.keelbar.plist`。

## 价格

**所有功能免费使用。** 如果觉得好用，可以在「设置 → 购买 KeelBar…」里用微信或支付宝买断（9.9 元），获得密钥后会关闭每日一次的购买提醒。不买也不会限制任何功能。

## 常见问题

**任务栏是空的，没有窗口？**
打开「系统设置 → 隐私与安全性 → 辅助功能」，把 KeelBar 关掉再打开，然后退出 KeelBar 重新打开。

**悬停预览只有标题、没有画面？**
在「屏幕与系统音频录制」里允许 KeelBar。

**升级后权限失效？**
在两个权限列表里删除旧的 KeelBar，重新添加新的 `KeelBar.app`。

**系统 Dock 不见了？**
这是「隐藏系统 Dock」选项的效果，可在设置里关掉；退出 KeelBar 后 Dock 也会自动恢复。

**设置菜单在哪里？**
KeelBar 没有 Dock 图标。点菜单栏上的 KeelBar 图标，或任务栏右侧的齿轮。

## 卸载

1. 在设置里关闭「登录时打开」，然后退出 KeelBar（系统 Dock 会自动恢复）。
2. 删除「应用程序」里的 `KeelBar.app`。
3. 在「系统设置 → 隐私与安全性」的「辅助功能」和「屏幕与系统音频录制」里删除 KeelBar。
4. 可选：在“终端”里执行 `defaults delete com.leowang.keelbar` 清除设置。

## 反馈

- 问题和建议：请提交 [Issue](../../issues)，附上 macOS 版本、KeelBar 版本（设置 → 关于）和复现步骤。
- 邮箱：wlbce@126.com

## 版权

© 2026 Leo Wang. All rights reserved. 详见 [LICENSE](LICENSE)。本仓库只提供安装包，不包含源码。

---

<a id="english"></a>

# KeelBar (English)

**A real taskbar for your Mac.** One button per open window: click to bring it forward, click again to minimize. Made for people coming from Windows, or anyone who loses windows once there are too many.

## Features

- **Window taskbar** at the bottom of the screen, one button per window (not per app). Click to bring forward, click again to minimize.
- **Hover preview** with a window thumbnail and the full title.
- **Unread alerts**: when Teams, Outlook, WeChat and others have unread items, the button shows a count badge and an orange glow that keeps circling until you click it. You can switch to a fixed number of laps or turn it off.
- **Combine windows by app** (optional): one button per app; click to pick a window.
- **Shortcuts** on the left for apps and folders, plus built-in Applications, System Settings, Dock Apps and Recents.
- **Window fitting**: maximized windows stop above the taskbar instead of hiding behind it. Double-click a title bar to maximize and restore.
- **Multiple displays**: a bar on every display, or only on the main one.
- **Appearance**: one or two rows, adjustable transparency and text color, per-app button colors.
- **Extras**: the thin strip at the far right minimizes all windows. KeelBar can hide the system Dock and restores it when you quit.
- **Languages**: English, 中文, 日本語, 한국어.

## Requirements

- macOS 14 Sonoma or later
- Apple silicon (M1 or later). Intel Macs are not supported yet.

## Install

1. Download `KeelBar-x.x-xxx.zip` from [Releases](../../releases/latest) and unzip it.
2. Move `KeelBar.app` to the Applications folder. Do not run it from iCloud, OneDrive or another synced folder.
3. Open it. KeelBar is not notarized by Apple yet, so macOS blocks the first launch:
   - **macOS 15 or later**: open it once and click Done. Then go to System Settings → Privacy & Security, scroll down to KeelBar, click **Open Anyway** and confirm.
   - **macOS 14**: Control-click `KeelBar.app`, choose Open, then click Open.
4. Grant the two permissions KeelBar asks for (see below). They take effect automatically, usually without a restart.

> Each time KeelBar starts, it minimizes all windows so you begin from the taskbar. Nothing is closed; click a button to restore a window.

> Alternatively run `xattr -dr com.apple.quarantine /Applications/KeelBar.app` in Terminal, then open the app.

Verify the download against `SHA256SUMS.txt` on the Releases page:

```bash
shasum -a 256 KeelBar-*.zip
```

## Permissions and why

| Permission | Used for |
|---|---|
| Accessibility | Reading the window list and titles; bringing forward, minimizing, closing and fitting windows. KeelBar cannot work without it. |
| Screen & System Audio Recording | Only for hover-preview thumbnails. Optional; without it previews show no image. |

In System Settings → Privacy & Security, add `KeelBar.app` itself, not the executable inside the bundle.

## Privacy

- **Runs entirely on your Mac and never connects to the network.** No analytics, no crash reporting, no update checks.
- Window thumbnails are only shown in memory; they are never saved or uploaded.
- Settings are stored locally in `~/Library/Preferences/com.leowang.keelbar.plist`.

## Price

**Every feature is free to use.** If you like KeelBar, Settings → Buy KeelBar… offers a one-time ¥9.9 license via WeChat Pay or Alipay, which turns off the once-a-day purchase reminder. Nothing is locked without it.

## FAQ

**The bar shows no windows.**
In System Settings → Privacy & Security → Accessibility, turn KeelBar off and on again, then quit and reopen KeelBar.

**Hover previews have no image.**
Allow KeelBar under Screen & System Audio Recording.

**Permissions stopped working after an update.**
Remove the old KeelBar from both permission lists and add the new `KeelBar.app`.

**My Dock disappeared.**
That is the "Hide System Dock" option. Turn it off in Settings; the Dock also comes back when you quit KeelBar.

**Where are the settings?**
KeelBar has no Dock icon. Use the KeelBar icon in the menu bar or the gear at the right end of the taskbar.

## Uninstall

1. Turn off "Open at Login" in Settings, then quit KeelBar (the system Dock comes back).
2. Delete `KeelBar.app` from Applications.
3. Remove KeelBar from Accessibility and Screen & System Audio Recording in System Settings → Privacy & Security.
4. Optional: run `defaults delete com.leowang.keelbar` in Terminal to clear settings.

## Feedback

- Bugs and ideas: open an [issue](../../issues) with your macOS version, KeelBar version (Settings → About) and steps to reproduce.
- Email: wlbce@126.com

## License

© 2026 Leo Wang. All rights reserved. See [LICENSE](LICENSE). This repository distributes the app only; source code is not included.
