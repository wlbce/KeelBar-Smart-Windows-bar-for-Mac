# 更新日志 / Changelog

## 4.1 (120)

### 新增 / Added
- 拖动排序：按住任务条左右拖动即可调整顺序，同一应用的窗口会一起移动；顺序会被记住，重启后仍然有效。
  Drag to reorder: hold a task button and drag it left or right. Windows of the same app move together, and the order is remembered across restarts.
- 预览上的关闭按钮：鼠标移进悬停预览，右上角出现 ✕，点击即可关闭该窗口；点缩略图其他位置切换到该窗口。多窗口预览卡片同样支持。
  Close from the preview: move into a hover preview and click the ✕ in its corner to close that window, or click the thumbnail to switch to it. Works on multi-window preview cards too.
- 自动隐藏任务栏：在设置里打开后，鼠标离开任务栏会自动收起，碰到屏幕底边再弹出；打开预览、菜单或正在拖动时不会收起。
  Auto-hide: when enabled in Settings, the bar slides away once the pointer leaves and returns when you touch the bottom edge of the screen. It stays up while previews or menus are open, or while you are dragging.
- 拖文件切换窗口：把文件拖到任务条上停留约半秒，对应窗口会自动前置，可以直接拖放进去，和 Windows 一样。
  Drag-and-hover to switch: hold dragged files over a task button for about half a second and its window comes forward, ready for the drop, just like on Windows.
- 新增「任务条随图标着色」开关，打开后恢复按应用图标颜色着色的彩色任务条。
  New "Tint Tasks by App Icon" switch that brings back fully colored task buttons.

### 改进 / Improved
- 任务条默认改为统一的半透明底色，只保留一点应用颜色，整体更清爽；单独设置过颜色的应用不受影响。
  Task buttons now share one translucent color with only a hint of the app's color, for a calmer bar. Apps with a custom color keep it.
- 当前窗口的标题加粗、底色略亮，最小化的窗口图标和文字变淡，状态一眼可辨。
  The active window gets a bold title and a slightly brighter button, and minimized windows are dimmed, so each state is easy to tell apart.
- 空间足够时任务条更宽，长标题显示得更完整；图标与文字的间距重新调整。
  Task buttons grow wider when there is room, so long titles are cut off less often. Icon and title spacing has been refined.
- 左侧快捷图标排列更紧凑，文件夹图标与应用图标大小一致，分隔线更清晰。
  Shortcuts on the left are packed more tightly, folder icons match app icons in size, and the divider is clearer.
- 任务栏顶部增加一道细高光，边缘更有层次。
  A fine highlight along the top edge gives the bar more depth.
- 单击任务条改为松开鼠标时生效，以便区分点击和拖动。
  A click on a task button now takes effect when you release the mouse, so clicks and drags can be told apart.
- 使用手册按当前功能重写，去掉已删除的选项说明。
  The in-app User Guide has been rewritten for the current features, and removed options are no longer described.

### 修复 / Fixed
- 计算器等窗口较小的应用不出现在任务栏上（包括最小化之后）。
  Apps with small windows, such as Calculator, did not appear on the bar, including after being minimized.

## 4.0 (111) — 首个公开版本 / First public release

### 新增 / Added
- 未读通知流光：应用有新未读时，任务条显示橙色流光，默认一直转，点击任务条停止；可在「设置 → 流光转圈通知」改为 1 / 3 / 5 / 10 圈或关闭。
  Unread glow: an orange light circles a task button when its app gets new unread items. By default it keeps going until you click the button; choose 1, 3, 5 or 10 laps, or turn it off, in Settings → Notification Glow.
- 点击任务条和左侧快捷图标时有轻微的按压反馈。
  Subtle press feedback when clicking task buttons and shortcuts.

### 改进 / Improved
- 当前窗口的指示线改为白色、两端渐隐，在蓝色等彩色任务条上也清晰可见；选中时从中间展开。
  The active-window indicator is now a white line with soft ends that stays visible on blue and other tinted buttons, and grows from the center when selected.
- 去掉了选中任务条时的流光动画，切换窗口更安静。
  Removed the light sweep on the selected button for calmer window switching.
- 设置子菜单显示在对应菜单项旁边，开关改为系统风格。
  Settings submenus open beside their row, and toggles use the system switch style.
- 窗口最大化、避让任务栏和双击标题栏缩放的逻辑重新整理，更稳定；点击标题栏上的按钮、标签页和滚动条不会再误触发缩放。
  Reworked maximize, taskbar fitting and title-bar double-click zoom. Clicking buttons, tabs or scroll bars in a title bar no longer zooms the window.

### 修复 / Fixed
- 鼠标从窗口下边缘移到任务栏时，光标有时停留在上下调整的形状。
  The pointer could stay as a resize cursor after moving from a window edge onto the taskbar.
- Outlook 的两个任务条有时会互换位置。
  Outlook's two task buttons could swap places.
- 打开设置菜单的瞬间移动鼠标，会误弹出子菜单。
  Moving the mouse while the settings menu was opening could pop up a submenu.
- 购买提醒没有按每天一次出现。
  The purchase reminder did not appear once a day as intended.
