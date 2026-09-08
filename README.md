# KeelBar-Smart-Windows-bar-for-Mac
Smart windows bar for Mac. One button per window. 
Topics： macos · taskbar · dock · productivity · windows

# Keelbar：Smart windows bar for Mac

 <img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/42b87a6d-1647-4d12-94a0-646a4285fb49" />


<img width="2706" height="736" alt="image" src="https://github.com/user-attachments/assets/eb7282be-352d-46ca-ba15-1b39d522ba01" />

A window-based taskbar for macOS.  
为 Mac 设计的按窗口工作的底栏。

macOS 14+ · English / 中文 / 日本語 / 한국어  
This repository distributes the packaged app only. Source code is not published.  
本仓库只发布安装包，不公开源代码。

First launch is blocked by macOS until you Control-click → Open (or Privacy & Security → Open Anyway). See the README.
第一次打开会被系统拦截：请 Control-点 → 打开，或到「隐私与安全性」点「仍要打开」。

<img width="1592" height="1080" alt="image" src="https://github.com/user-attachments/assets/9d8649a3-b7e9-443a-92af-242549dbb2d3" />

<img width="1473" height="1080" alt="image" src="https://github.com/user-attachments/assets/e9627d3a-a88a-4a8b-96f7-aca26676cfaf" />

<img width="436" height="720" alt="image" src="https://github.com/user-attachments/assets/d6359026-ddc6-4e5e-8698-660c813c83ad" />

<img width="990" height="994" alt="image" src="https://github.com/user-attachments/assets/74aa8c04-c92d-462d-92d3-80c00ccf570a" />

---

## English

### Why KeelBar

The macOS Dock is built around **apps**. One icon stands for Chrome, Finder, or Word, no matter how many windows you have open. After you minimize a window, it leaves the desktop. Getting back to *that email* or *that folder* means guessing which Dock icon to click, or searching Mission Control.

KeelBar is built around **windows**. Each open window gets its own button, with a readable title. Click to bring it forward. Click again to minimize. The muscle memory is the same as the Windows taskbar.

It is made for people who switched from Windows to Mac, and for anyone who works across many windows every day.

### Dock vs KeelBar

| | Dock | KeelBar |
|---|---|---|
| Unit of work | App | Window |
| Several Chrome or Finder windows | One icon; the system chooses which window to show | One button per window; the title is visible |
| After minimize | The window disappears from the desktop | The button stays on the bar; click to restore |
| Unread mail / chat | A small badge on the Dock icon | The button turns orange; a count appears on the corner |
| Everyday action | Talk to the app | Click to focus, click again to minimize |

The Dock is still good for launching apps. KeelBar is for switching among the windows you already have open.

### Features

- Bottom bar lists every window, not only every app
- Click to focus; click again to minimize
- Optional **Combine Windows by App**: one control per app; multiple windows stack and expand as a list
- Unread state (Dock badge) shown in orange, for apps such as Outlook and Teams
- Pin apps and folders; default shortcuts for Applications, Dock Apps, and Recents
- One or two rows; small or large icons
- Hides the system Dock while running; restores it when you quit
- Runs entirely on your Mac: no network, no data collection
- Menu bar extra (no Dock icon of its own)

### Requirements

- macOS 14 or later
- Accessibility permission (to list windows and bring them forward)

### Install

1. Download **KeelBar.zip** from [Releases](../../releases).
2. Unzip, then move `KeelBar.app` into **Applications**. Do not run it from iCloud Drive or OneDrive.
3. If macOS says the app cannot be opened: Control-click `KeelBar.app` → **Open**.
4. Open **System Settings → Privacy & Security → Accessibility** and add `KeelBar.app` (the app itself, not a file inside the bundle).
5. If the window list is empty: turn KeelBar off and on in Accessibility, then quit and reopen the app.

The current build is ad-hoc signed and not notarized by Apple. The Control-click step is expected on first launch.

### Use

- Click a window button to bring it forward; click again to minimize.
- Right-click for bring to front, minimize or restore, quit, close, or pin.
- The thin strip at the far right minimizes all windows.
- Menu bar icon or the gear on the bar: settings, user guide, and language.
- On first launch, KeelBar minimizes existing windows so the desktop is clear.

A full user guide is inside the app: gear → **User Guide**. It follows the language you select.

### Download

See **Releases** for `KeelBar.zip`. This project does not include source code.


KeelBar is ad-hoc signed and not notarized by Apple. macOS will block it the first time you open a copy downloaded from the internet. This is expected.
**1. Put the app in the right place**

- Unzip `KeelBar.zip`.
- Move `KeelBar.app` into **Applications**.
- Do not run it from the zip, the Downloads folder for long, or iCloud Drive / OneDrive.

**2. Open it the first time (pick one)**

**Way A — Control-click**

1. Open **Applications**.
2. **Control-click** `KeelBar.app` (do not double-click).
3. Choose **Open**.
4. In the dialog, choose **Open** again.

**Way B — Privacy & Security (use this on macOS 15 or later if Way A fails)**

1. Double-click `KeelBar.app` once, so macOS records the block.
2. Open **System Settings → Privacy & Security**.
3. Scroll to the message that KeelBar was blocked.
4. Click **Open Anyway**.
5. Confirm **Open Anyway**, and enter your Mac password if asked.

**3. Allow Accessibility**

1. Open **System Settings → Privacy & Security → Accessibility**.
2. Click **+** and add `KeelBar.app` (the app itself, not a file inside the bundle).
3. Turn the switch **on**.
4. Quit KeelBar fully, then open it again.

**4. If the bar is empty**

- In Accessibility, turn KeelBar **off**, then **on**.
- Quit KeelBar and reopen it.
- Confirm you added `KeelBar.app` from **Applications**, not a second copy in Downloads.

**Still blocked?**

- Delete other copies. Keep only `/Applications/KeelBar.app`.
- In Terminal: `xattr -dr com.apple.quarantine /Applications/KeelBar.app`  
  Then try Control-click → Open again.
---

## 中文

### 为什么做 KeelBar

macOS 的 Dock 管的是 **应用**。Chrome、Finder、Word 各一个图标，开了多少窗口都挤在同一个图标里。窗口最小化后会离开桌面，要回到「那封邮件」或「那个文件夹」，只能再点 Dock，或在调度中心里找。

KeelBar 管的是 **窗口**。每个窗口一条，标题看得见。单击前置，再点最小化。手感和 Windows 任务栏一致。

适合从 Windows 转到 Mac 的人，也适合每天要在很多窗口之间切换的人。

### Dock 和 KeelBar

| | 系统 Dock | KeelBar |
|---|---|---|
| 工作单位 | 应用 | 窗口 |
| 多个 Chrome / Finder 窗口 | 一个图标，点下去由系统选择 | 每个窗口一条，标题可见 |
| 最小化之后 | 窗口从桌面消失 | 底栏按钮还在，再点即可还原 |
| 未读邮件 / 消息 | Dock 图标上的小角标 | 任务条变橙，角标显示数量 |
| 日常操作 | 和应用打交道 | 单击前置，再点最小化 |

Dock 适合打开应用。已经打开的窗口之间切换，用 KeelBar 更直接。

### 功能

- 底栏按窗口列出，而不是只按应用
- 单击前置，再点最小化
- 可选 **相同应用合并**：每个应用一个入口；多窗口呈叠片，点开后上下列出
- 未读状态（Dock 角标）显示为橙色，如 Outlook、Teams
- 可固定应用和文件夹；默认提供「应用程序」「Dock 应用」「最近使用」
- 单行或两行；小图标或大图标
- 运行时隐藏系统 Dock，退出后恢复
- 仅在本机运行：不联网，不收集数据
- 菜单栏常驻（自身不占用 Dock）

### 系统要求

- macOS 14 或更高版本
- 需要「辅助功能」权限（用于列出窗口并前置）

### 安装

1. 从 [Releases](../../releases) 下载 **KeelBar.zip**。
2. 解压后把 `KeelBar.app` 放到 **应用程序**。不要从 iCloud / OneDrive 同步目录里直接运行。
3. 若系统提示无法打开：按住 Control 点图标 → **打开**。
4. 打开 **系统设置 → 隐私与安全性 → 辅助功能**，添加 `KeelBar.app`（整个应用，不要选包内的可执行文件）。
5. 若窗口列表是空的：在辅助功能里关掉再打开 KeelBar，然后退出软件再开一次。

当前构建为本地签名，未经 Apple 公证。第一次打开时，用 Control-点打开是正常步骤。

### 使用

- 单击窗口按钮前置，再点一次最小化。
- 右键可前置、最小化或还原、退出程序、关闭、固定。
- 最右端细条会最小化全部窗口。
- 菜单栏图标或底栏齿轮：设置、使用手册、语言。
- 启动时会将已有窗口最小化，桌面先留空。

完整说明在软件内：齿轮 → **使用手册**。手册语言随界面语言切换。

### 下载

请到 **Releases** 下载 `KeelBar.zip`。本仓库不提供源代码。



KeelBar 为本地签名，未经 Apple 公证。从网上下载后，系统第一次会拦截，这是正常现象。


**1. 先放到正确位置**

- 解压 `KeelBar.zip`。
- 把 `KeelBar.app` 拖进 **应用程序**。
- 不要在压缩包里直接开，也不要从「下载」、iCloud / OneDrive 同步目录里长期运行。

**2. 第一次打开（任选一种）**

**方法 A — Control-点打开**

1. 打开 **应用程序**。
2. **按住 Control 再点** `KeelBar.app`（不要双击）。
3. 选 **打开**。
4. 弹出确认时，再点一次 **打开**。

**方法 B — 隐私与安全性（macOS 15 及以上若方法 A 无效，用这个）**

1. 先双击一次 `KeelBar.app`，让系统记下「已拦截」。
2. 打开 **系统设置 → 隐私与安全性**。
3. 往下滚，看到 KeelBar 被拦截的说明。
4. 点 **仍要打开**。
5. 再次确认 **仍要打开**；若要求输入本机密码，请输入。

**3. 打开辅助功能权限**

1. 打开 **系统设置 → 隐私与安全性 → 辅助功能**。
2. 点 **+**，添加 `KeelBar.app`（整个应用，不要选包里面的可执行文件）。
3. 把开关打开。
4. 完全退出 KeelBar，再打开一次。

**4. 底栏是空的、看不到窗口**

- 在辅助功能里把 KeelBar **关掉再打开**。
- 退出 KeelBar，再启动一次。
- 确认添加的是 **应用程序** 里的那一份，不是「下载」里的另一份。

**仍然打不开？**

- 删掉多余的副本，只保留 `/应用程序/KeelBar.app`。
- 打开「终端」，执行：  
  `xattr -dr com.apple.quarantine /Applications/KeelBar.app`  
  然后再用 Control-点 → 打开。
---



© 2026 Leo Wang. All rights reserved.
