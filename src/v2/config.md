# 配置详情 v2

- 配置信息存储在同级目录的 `InputTip.ini` 文件中，启动软件时自动创建
  - 如果 v1 v2 版本都使用过，不用担心，它们的配置信息是独立的，不会冲突
- 修改方式:
  - 鼠标右键点击任务栏右侧的 `InputTip.exe` 托盘图标，点击 `更改配置`。(推荐方式)
  - 直接打开 `InputTip.ini` 文件，修改对应项的值，保存后重启 `InputTip.exe`。

---

## `changeCursor`

- 默认值: `1`
- 当输入法状态改变时(中英文/大写锁定)，是否改变鼠标指针样式。
- 注意:
  - 当设置为`0`后，`InputTip.exe` 会尝试恢复到原来的鼠标指针样式，但不一定全部成功。
  - 如果有部分鼠标样式没有恢复，那就需要重启电脑。

## `showSymbol`

- 默认值: `1`
- 当输入法状态改变时(中英文/大写锁定)，是否在输入光标附近显示一个方块符号。

### `CN_color`

- 默认值: `red`
- 中文输入状态下方块符号的颜色。
- 可以是常见的颜色英文单词，也可以是十六进制颜色值(带不带 `#` 都可以)。
- 建议除了 `red`、`blue`、`green`等基础颜色单词外，都使用十六进制颜色值。

### `EN_color`

- 默认值: `blue`
- 英文输入状态下方块符号的颜色。
- 可以是常见的颜色英文单词，也可以是十六进制颜色值(带不带 `#` 都可以)。
- 建议除了 `red`、`blue`、`green`等基础颜色单词外，都使用十六进制颜色值。

### `Caps_color`

- 默认值: `green`
- 大写锁定状态下方块符号的颜色。
- 可以是常见的颜色英文单词，也可以是十六进制颜色值(带不带 `#` 都可以)。
- 建议除了 `red`、`blue`、`green`等基础颜色单词外，都使用十六进制颜色值。

### `transparent`

- 默认值: `222`
- 方块符号的透明度。
- 取值范围: `0`~`255`

### `offset_x`

- 默认值: `5`
- 方块符号的水平偏移量。

### `offset_y`

- 默认值: `0`
- 方块符号的垂直偏移量。

### `symbol_height`

- 默认值: `7`
- 方块符号的高度。

### `symbol_width`

- 默认值: `7`
- 方块符号的宽度。

### 其他配置
- 以下配置不应该手动更改，而是从托盘菜单中进行设置，由 `InputTip.exe` 内部更改
- `mode`
  - 鼠标右键点击托盘菜单 -> `设置模式` -> `模式1`,`模式2`,...
- `app_hide_CN_EN`、`app_hide_state`
  - 鼠标右键点击托盘菜单 -> `设置特殊软件` -> `隐藏中英文状态方块符号提示`,`隐藏输入法状态方块符号提示`
- `app_CN`、`app_EN`、`app_Caps`
  - 鼠标右键点击托盘菜单 -> `设置自动切换` -> `自动切换到中文状态`,`自动切换到英文状态`,`自动切换到大写锁定状态`