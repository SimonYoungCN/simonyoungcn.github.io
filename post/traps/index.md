
最近踩了许多坑，总结出来与君共勉。由于本人的确是纯小白，每一个坑基本都踩过，文章也应该会有点小儿科，烦请见谅。:smiley: 

{{%admonition type="info" title="配置环境" details="false" %}}
Windows 10 20H2 惠普战66 R5-5625U
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

{{%admonition type="quote" title="《孔雀东南飞》" details="false" %}}
多谢后世人, 诫之慎莫忘。
{{% /admonition %}}

[1]:(https://www.jianshu.com/p/7cc6ea70e48e)  (简书)
[2]:(https://stackoverflow.com/questions/32703317/how-to-activate-markdown-user-snippets-in-visual-studio-code) (stackoverflow)