# v2 版本更新日志

- 注意: 如果你的网络环境无法访问 [官网](https://inputtip.pages.dev)，`InputTip.exe` 也将无法检测到版本更新，你可能需要额外关注项目仓库中是否有版本更新

- 没有特别说明的版本都是修复问题


## 2.10.0

- 在托盘菜单中添加 `设置自动切换`，现在可以设置指定应用自动切换到英文/中文/大写锁定状态
- 其他的修复和优化

## 2.9.0

- 在托盘菜单中添加 `设置特殊偏移量`，用于解决在缩放大于 `125%` 的副屏上可能导致的显示位置误差
- 其他的修复和优化

## 2.8.0

- 添加配置修改校验，避免错误配置导致程序报错
  - 你不应该手动修改 `InputTip.ini` 配置文件
- 其他的修复和优化

## 2.7.2

- 将 `模式2` 作为默认模式
  - 一些 `模式1` 无法识别的窗口，`模式2` 可以识别
- 不是一开始就使用 `2.7.2` 及以上版本的，也可以切换到 `模式2` 尝试一下
  - 如果切换到 `模式2` 有效，就推荐一直使用 `模式2`

## 2.7.1

- 由于不是所有的输入法都无法在记事本和 everything 中获取到中英文状态
- 直接把 `notepad.exe,everything.exe` 赋值给 `app_hide_CN_EN` 配置是不合理的
- 应该由用于自己去设置 `app_hide_CN_EN` 配置项
  - 通过底部任务栏右侧的 `InputTip` 托盘图标，鼠标右键点击它，选择 `设置特殊软件`
- 所以现在将 `app_hide_CN_EN` 配置的默认值更改为空
- 不是一开始就使用 `2.7.1` 及以上版本的，你可以先去除掉 `notepad.exe,everything.exe`这个值，检查一下是否可以正常工作

## 2.7.0

- 更改了配置项
  - `window_no_display` => `app_hide_CN_EN`
  - `window_no_display` 的值会复制给 `app_hide_CN_EN`
- 添加了一个配置项:
  - `app_hide_state`
- 在任务栏底部右侧的软件托盘菜单中添加了一个子菜单 `设置特殊软件`
  - 可以在它的子项中，快速的设置 `app_hide_CN_EN` 和 `app_hide_state`
- 提高了处理逻辑的阈值时间，解决有时状态更新不及时的问题
- 其他的修复和优化

## 2.6.0

- 添加 `模式4` 以兼容手心输入法

## 2.5.0

- 提高了处理逻辑的阈值时间，解决有时状态更新不及时、方块卡在原地的问题
- 修改两个默认配置的值
  - `offset_x`: `15` => `5`
  - `offset_y`: `-15` => `0`
  - 正常来说，这样的默认值可能更合理一些
  - 你甚至可以将 `symbol_height` 高度设置为光标的高度，将 `symbol_width` 调小，你就可以获得一个光标形状的符号，而不是方块。
- 修改了模式切换的菜单显示
- 其他的修复和优化

## 2.4.0

- 通过模式切换兼容更多输入法，包括百度、小狼毫(rime)、谷歌等输入法
- 修改了菜单文字显示的效果，减少了字重，减少了字体显示问题
- 由于不同的网络环境，可能无法访问到 [官网](https://inputtip.pages.dev)，所以给一些可能访问不到的地址，添加 `Github` 和 `Gitee` 地址
- 其他的修复和优化

## 2.3.0

- 添加了一个方块符号，在输入光标处根据输入法状态改变颜色，作为除了鼠标以外的另一个提示方式
- 添加了许多的配置项
  - 关于配置项的详细说明，请查看 [配置项说明](./config.md)
- 添加了自动更新机制
  - 当启动 `InputTip.exe` 时，会异步的检查更新，如果有新版本，会提示确认更新
  - 如果确认更新就会自动下载新版本替代旧版本并重启
- 其他的修复和优化

## 2.2.0

- 当开始大写锁定时，鼠标样式将会切换为绿色(默认)
  - 你也可以自定义它
- 此版本没有考虑到版本迁移的问题
  - 如果直接将 2.2.0 的 exe 文件覆盖 2.1.0 的 exe 文件，可能会导致应用无效
  - 因为 InputTipCursor 需要新添加两个目录 Caps 和 Caps_Default
  - 建议先将 InputTipCursor 目录移动到别处，让 InputTip.exe 重新创建此目录
- 其他的修复和优化

## 2.1.0

- 添加鼠标样式的设置
- 延长了轮询间隔
- 添加了一个可选的鼠标样式文件 Pen
- 改进和修复了一些其他问题

## 2.0.0

- v1 版本中通过显示内容的方式来提示当前输入法的中英文状态，这在某些时候会觉得有些碍眼
- v2 版本中不再使用此方式，而是通过两套光标样式，切换输入法状态时，光标样式会随之切换