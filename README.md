# Code Poster

生成代码明信片。支持代码压缩，图片缩放，自动居中。

![](http://ok2pw0x6d.bkt.clouddn.com/Fuo-iJqj2LSeIgLV8Cm_vcWAGCBO.png)

## 安装

### 下载

[二进制程序](http://github.com/fate-lovely/codeposter/releases)

### Go

```bash
go git -u github.com/fate-lovely/codeposter
```

## 参数

```bash
$ codeposter -h
usage: codeposter [<flags>] <source> <image>

Flags:
  -h, --help                Show context-sensitive help (also try --help-long
                            and --help-man).
      --font="Hack"         font family, please use monospace font,
      --fontsize="11.65px"  font size, valid css font size, must corresponding
                            to char width and char height
      --charwidth=7         single character width in pixels
      --charheight=14       single character height in pixels
      --width=800           output poster width in pixels
      --height=760          output poster height in pixels
      --bgcolor="#eee"      background color, valid css color
      --output=canvas       specify output format, [canvas | dom]
      --version             Show application version.

Args:
  <source>  source code path
  <image>   image path
```

- `font`：字体，默认使用`Hack`，务必选择一款等宽字体
- `fontsize`：字体大小，选个一个合适的字体大小，保证对应的字符的宽度和高度是一个整数
- `charwidth`：单个字符宽度，这个需要在浏览器中手动测量
- `charheight`：单个字符高度，这个也需要在浏览器中手动测量
- `width`：最终明信片的宽度，单位是像素，整数
- `height`：最终明星片的高度，单位是像素，整数
- `bgcolor`：背景颜色
- `output`：输出格式，目前支持`dom`和`canvas`。注意，dom格式将每个字符渲染为一个div，十分消耗性能，默认格式为canvas。

## 示例

进入`example`文件夹。

### Gopher

```bash
codeposer jquery.min.js go.png > go.html
```

![](http://ok2pw0x6d.bkt.clouddn.com/Fs-kAGAGyrsTVZG7wzsv_DpyVWm-.png)

### Heart

```bash
codeposter jquery.min.js heart.png > heart.html
```

![](http://ok2pw0x6d.bkt.clouddn.com/FqAgqcFdvvrQ-gcUrNfi1VwLXBtP.png)

### Diamond

```bash
codeposter jquery.min.js diamond.png > diamond.html
```

![](http://ok2pw0x6d.bkt.clouddn.com/FjlOnvZSWkEoOlPFRJT1bFNZV6qz.png)
