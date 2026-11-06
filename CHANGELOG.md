# 更新日志 / Changelog

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
