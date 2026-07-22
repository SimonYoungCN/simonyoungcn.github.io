
最近踩了许多坑，总结出来与君共勉。由于本人的确是纯小白，每一个坑基本都踩过，文章也应该会有点小儿科，烦请见谅。:smiley:

<!--more-->

{{%admonition type="info" title="配置环境" details="false" %}}
Windows 10 20H2 惠普战66 R5-5625U (HP ZHAN 66 Pro A 14 inch G5 Notebook PC)
{{% /admonition %}}


## Neovim及插件

### init.vim

Neovim插件配置文件即为`init.vim`，安装和配置插件都在这里实现。一般是在`call begin()`和`call end()`之间加入自己需要安装的插件，然后再在最后添加`let g:`等配置信息。说白了Neovim的配置都在这个文件里部署, 例如设置鼠标控制光标等。不知道是系统的原因还是什么，我只能把`init.vim`放在`C:\Users\simon\AppData\Local\nvim`里而把存放插件的地方设置为`C:\Users\simon\.AppData\local\nvim\plugged`里。放在其他地方就会报错。

![看这图看了一天…… ](https://pic.imgdb.cn/item/62b263a809475431298d05d8.png "看这图看了一天……") 

另外, 我似乎还不知道Windows 10 系统下如何打通与Neovim的剪贴板，希望知道的人能够慷慨留言告诉我一下。:wink:

### Usnippets 

这确实是个好东西。但是它需要配合`vim-snippet`使用，否则就只是一具空壳而已。

### MarkdownPreview

由GitHub用户"iamcco"开发，使用十分便利。

只不过在我的环境下，用它打开默认浏览器还需要把`chrome.exe`的路径添加到path里。

## Hugo

### 配置主题 

直接下载对应主题文件，粘贴到`theme`文件夹即可。但是配置文件里主题名称要和主题文件夹名称保持一致。

#### mathjax支持
我的网站上使用的主题是even，由GitHub用户ahonn开发，GitHub用户olOwOlo移植到了hugo上。在此对两位开发者致以崇高的敬意。不过虽然我在`config.toml`里开启了对mathjax的支持，数学公式仍然无法被识别。于是我在GitHub上下载了mathjax的文件，也确实能够识别数学公式（注意此处git clone下来的mathjax文件夹名称应该改为`mathjax`，还要全部小写，并放在`your-site/static/lib/mathjax`的路径里）。但在进行`git push`之后报错：

{{%admonition type="failure" title="build-checkout" details="false" %}}
```bash
Error: fatal: No url found for submodule path 'lib/mathjax' in .gitmodules
Error: The process '/usr/bin/git' failed with exit code 128
```
{{% /admonition %}}

后面上网查了一下，发现是`mathjax`文件夹里还有隐藏的`.git`文件，需要执行如下命令将其删除[1]：

```bash
$ git rm --cached
$ git add .
$ git commit -m "commit messge"
$ git push origin [branch_name]
```

### 部署到GitHub Pages 

目前GitHub已经默认主分支名称为`main`，但大部分教程仍旧是`master`，相关改动可以参考[这里](https://zhuanlan.zhihu.com/p/57361697)的评论区。反正我`push`时`main`分支一直报错，于是我先push到`master`，然后把`main`给删了，简单粗暴。:laughing:

### 评论(Utterances) 

另建一个`repo`，用于存放`issue`形式的评论。

{{%admonition type="warning" title="注意" details="false" %}}
Hugo的配置文档里第一行`baseURL`不能加`www.`的前缀，只能是`https://[YOUR_GITHUB_ID].github.io`。另外, 配置文件里的`repo`只用填写自己的repo名，不用加用户名。
{{% /admonition %}}

为了这一问题我甚至还去Utterances里死皮赖脸提了个issue…… :joy:

## VS Code
Neovim实在用不惯，只用来做笔记算了，积累了小半篇的`markdown.snippet`，做笔记的速度还是蛮快的。:smiley:只不过各方面都没有VSCode好用：中文逗号、冒号等打不出来；不能复制粘贴；功能不强大。
曾经看到过知乎上抖机灵的回答，说(Neo)vim是军刀，IDE是航母。不可否认，vim系列的编辑器优点多多，比如对系统配置要求低，运行速度快，可键盘控制。但个人认为，军刀安装再多插件，装备再丰富，终究不敌航母。写东西是为了方便快捷，而不是去习惯畸形的操作方式。只有自己用起来最顺手的东西才是最好的。

用VSCode其实还挺方便的，就比如复制粘贴，可以大大提高我的效率(doge)。

{{%admonition type="warning" title="注意" details="false" %}}
若要在vscode里为 `markdown`文件创建snippets，除了按照 [官方文档](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_create-your-own-snippets)说的来做之外，还要找到vscode的设置文件 `settings.json`，在下方加一行 `"[markdown]": { "editor.quickSuggestions": true }`。[2]
{{% /admonition %}}

### snippets
换用VSCode后死心不改，仍然不舍放下snippets。于是网上一查，又开始折腾。vscode的snippets是用`json`格式写的。这里分享一个[快速制作json格式snippets的网站](https://snippet-generator.app/)。好不容易做完之后，却发现markdown文件根本无法弹出补全列表。查了一下，需要在`settings.json`里加入如下语句：
```json
"[markdown]": {
        "editor.formatOnSave": true,
        "editor.renderWhitespace": "all",
        "editor.quickSuggestions": {
            "other": true,
            "comments": true,
            "strings": true
        },
     
          "editor.acceptSuggestionOnEnter": "on"
    },
```
但我添加之后，系统一直报错，后来在网上查找发现，依据`json`格式文件规定，在这段代码前还应加上一个逗号。

就先写到这里, 以后随时参考，随时补充。

{{%admonition type="info" title="新配置环境" details="false" %}}
Linux Mint 21 x86_64 linux内核版本 5.15.0-43-generic

惠普战66 R5-5625U
{{% /admonition %}}

## 面部识别软件howdy
正好我的电脑没有指纹识别功能（只有模具），于是看到[这篇文章](https://itsfoss.com/face-unlock-ubuntu/)之后准备大展身手。
但是在下载的时候提示：
{{%admonition type="failure" title="终端" details="false" %}}
```bash
Downloading 3 required data files...
Unpacking...
bzip2: Can't open input file *.bz2: No such file or directory.
Error while running last command
dpkg: 处理软件包 howdy (--configure)时出错：
 已安装 howdy 软件包 post-installation 脚本 子进程返回错误状态 1
正在处理用于 man-db (2.9.1-1) 的触发器 ...
在处理时有错误发生：
 howdy
E: Sub-process /usr/bin/dpkg returned an error code (1)
```
{{% /admonition %}}

当时我是百思不得解，卸了重装还是报错。于是搜索了一下，发现少了三个文件。[CSDN](https://ask.csdn.net/questions/3273360)和[howdy项目的issue里](https://github.com/boltgolt/howdy/issues/307)都有提到这个问题。
结果就是有the Great Firewall，网络环境堪忧，文件下载不下来。要去[这里](https://github.com/davisking/dlib-models)把`dlib_face_recognition_resnet_model_v1.dat.bz2`、`mmod_human_face_detector.dat.bz2`和`shape_predictor_5_face_landmarks.dat.bz2`给手动下载下来。
当然如果网络还是不好，就把整个项目`git clone`下来，再去选对应文件。

把这三个文件下载了之后，首先去新建位于`lib/security/howdy/dlib-data`的文件夹，把那三个压缩包（不要解压）放进去，再执行`sudo apt install howdy`的命令，现在就能顺利下载了。

在Linux上用人脸解锁权限可真舒服，谁用谁知道。

{{%admonition type="quote" title="《孔雀东南飞》" details="false" %}}
多谢后世人, 诫之慎莫忘。
{{% /admonition %}}

## 后记
过了一个多月，我终于等到了Linux Mint 21的镜像，虽说是beta版，但是至少高通的网卡能识别了。想起我刚拿到电脑时兴致勃勃地安装了Linux Mint 20.3以后才发现根本识别不了网卡，然而Windows系统在我全局安装时又被我删了，所以……

现在也在逐步开始适应neovim，花了一天的时间配置，效果还不错，可能之后也会坚持着用吧，毕竟我还是比较喜欢专注于一个软件，自己写的snippets不舍得就此放弃。还好，自己也慢慢地攻克了难关，markdownpreview的附加依赖下载时不会更新进度，就让它安静地下载。
中文符号输入不正确的bug还没有找到，不过大概率是某一个插件引起的，neovim还是空壳的时候，输入中文并没有任何问题，不过我还是利用利用snippets把这个bug尽量弥补了，比如我按中文分号`；`就会跳出来`¼<xCSI>`这玩意儿。所以我直接把那堆乱码设成了中文分号的触发键。后续打算再排查一下，也希望了解这种情况的人能够留言告诉缘由，不尽感激。
还有一个比较奇怪的点，我在Windows上没有遇到，但是在Linux上遇到了的问题是明明好看的主题应用之后变得十分难看，还以为这是Linux系统特点。后面偶然看见讨论说还要`set termguicolors`，之后果然熟悉的配色又回来了。

道阻且长，继续努力吧。:smiley:

贴一张screenshot：

![screenshot](https://pic.imgdb.cn/item/62e7535b8c61dc3b8ea30d72.png "还行吧？")

[1]:(https://www.jianshu.com/p/7cc6ea70e48e)  (简书)
[2]:(https://stackoverflow.com/questions/32703317/how-to-activate-markdown-user-snippets-in-visual-studio-code) (stackoverflow)
