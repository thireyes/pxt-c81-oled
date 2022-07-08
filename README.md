
> 在 [https://thireyes.github.io/pxt-c81-oled/](https://thireyes.github.io/pxt-c81-oled/) 打开此页面

## 用作扩展

此仓库可以作为 **插件** 添加到 MakeCode 中。

* 打开 [https://makecode.microbit.org/](https://makecode.microbit.org/)
* 点击 **新项目**
* 点击齿轮图标菜单下的 **扩展**
* 搜索 **https://github.com/thireyes/pxt-c81-oled** 并导入

## 编辑此项目 ![构建状态标志](https://github.com/thireyes/pxt-c81-oled/workflows/MakeCode/badge.svg)

在 MakeCode 中编辑此仓库。

* 打开 [https://makecode.microbit.org/](https://makecode.microbit.org/)
* 点击 **导入**，然后点击 **导入 URL**
* 粘贴 **https://github.com/thireyes/pxt-c81-oled** 并点击导入

## 积木块预览

此图像显示主分支中最后一次提交的块代码。
此图像可能需要几分钟才能刷新。

![块的渲染视图](https://github.com/thireyes/pxt-c81-oled/raw/master/.github/makecode/blocks.png)

#### 元数据（用于搜索、渲染）

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>

# C81 OLED MakeCode Package [![Build Status](https://travis-ci.org/Tinkertanker/pxt-oled-ssd1306.svg?branch=master)](https://travis-ci.org/Tinkertanker/pxt-oled-ssd1306)

![avatar](https://raw.githubusercontent.com/thireyes/pxt-c81-oled-ssd1306/master/icon.png)

This is the MakeCode Package for SSD1306 OLED controller, based on the Adafruit Arduino library available [here](https://github.com/adafruit/Adafruit_SSD1306).

## Hardware Setup
1. Insert the OLED display into the I2C ports on the break out board.

## Blocks
### Initialize OLED Display
Initializes the OLED display.

Sets up the OLED display and prepares it for use by the micro:bit.

```sig
OLED.init(64, 128);
```

This block must be placed before any of the ``show`` blocks.

### Show String Without Newline
Displays a string on the OLED module without a newline.

```sig
OLED.showString1("hello, micro:bit!")
```

The ``init`` block must be placed before this.

### Show String With Newline
Displays a string on the OLED module with a newline.

```sig
OLED.showString2("hello, micro:bit!")
```

The ``init`` block must be placed before this.


### Show Number Without newline
Displays a number on the OLED module without a newline.

```sig
OLED.showNumber1(123)
```

The ``init`` block must be placed before this.


### Show Number With Newline
Displays a number on the OLED module with a newline.

```sig
OLED.showNumber2(123)
```

The ``init`` block must be placed before this.


### Clear Display
Clears the display.

```sig
OLED.clear()
```

The ``init`` block must be placed before this.

### Draw Outlined Rectangle
Displays an outline of a rectangle.

```sig
OLED.drawRectangle(x,y,w,h)
```

The ``init`` block must be placed before this.


### Draw Outlined Circle
Displays an outline of a circle.

```sig
OLED.drawCircle(x,y,r)
```

The ``init`` block must be placed before this.


### Draw Line
Displays a line.

```sig
OLED.drawLine(x1,y1,x2,y2)
```

The ``init`` block must be placed before this.


### Progress bar
Displays a progress bar with a specified percentage of progress.

```sig
OLED.drawLoadingBar(percent)
```

The ``init`` block must be placed before this.


## Example: Counter
The following code is a simple counter that displays an increasing number every second.

```blocks
OLED.init(64, 128)
let item = 0
basic.forever(() => {
    basic.pause(1000)
    item += 1
    OLED.showNumber(item)
})
```

## Supported targets

* for PXT/microbit

## Footnotes

1.  Datasheet https://cdn-shop.adafruit.com/datasheets/SSD1306.pdf
