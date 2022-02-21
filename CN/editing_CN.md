[<< 返回中文主页](README_CN.md)
# 编辑代码 (Editing code)

> 摘自官方Wiki
有两种主要的方法来编写Mindustry逻辑: 可视化编辑和手动编辑. 每种都有各自的优点, 哪个适合你就选哪个.

## 可视化编辑 (The Visual Editor)

可视化编辑是处理器中的'编辑'界面 (当你点击'铅笔'图标后). 可视化编辑推荐初学者使用, 因为它易于理解与使用.

与手动编辑相比, 这种编辑方式的优点如下:

- 一个长条状, 有颜色编码, 可拖放的界面
- 简易参数选择器, 显示所有需要的参数
- 可视, 易于设置跳转关系
- 对手机端友好

![image](https://mindustrygame.github.io/wiki/images/misc/logic-editing-visualEditor-overview.png)

你还可以在文本表单中导出和导入代码

## 手动编辑 (Manual Editing)

手动编辑涉及使用例如Notepad++, Vim或Visual Studio Code这样的文本编辑器来编辑你的代码. 对于更高级的用户或更长的代码, 更推荐手动编辑.

与可视化编辑相比, 这种编辑方式的优点如下:

- 代码比可视化编辑更紧凑; 一次可以看到更多代码
- 打字比在长长的代码墙上拖拽要更快
- 无需打开Mindustry即可快速生成代码进行演示
- 在某些文本编辑器中有语法高亮, 例如VS Code (插件), Emacs (包), Vim (插件) 和Sublime Text (包)
- 文本块不会阻止部分参数文本
- 能够在Mindustry之外保存和访问代码
- 注释, 缩进和跳转标签, 有助于跟踪较长代码中的循环和函数

然而对于初学者或不习惯编辑代码的人来说, 这可能有点困难.

### 注释 (Comments)

注释可以用来解释代码的功能, 并帮助跟踪代码. 注释不会被保留, 也无法在可视化编辑器中查看.
```
# Set a = 1, b = 2, c = 4
set a 1
set b 2 # On this line, b is set to 2
set c 4
#这是一条注释, 开头带上'#'即可
jump jumpHere equal a 1 # 如果a等于1, 则跳转
    set d 0
    end
jumpHere:
set d 3
```

### 跳转标签 (Jump labels)

手动编辑时, 跳转标签可用于'跳转'指令.
它们可以像注释一样帮助表示函数和循环.
```
set a 0
loop:
    op add a a 1
jump loop lessThan a 5 # 继续使a做加法直到其数值为5, 然后将a重置为0
```

### 缩进和间隔 (Indentation and spacing)

手动编辑代码时, 你可以在指令之间使用缩进和间隔来帮助美化代码或使代码更具可读性.
当你把这些间隔粘贴进可视化编辑中时, 它们会消失.
```
set a 1
# 哇, 这是指令之间的间隔!
set b 2
# 和更多间隔!
set c 4
set d 0
loop:
            print "你还可以添加任意数量的缩进"
                                print "\n尽管我建议你不要滥用它 :)"
    op add d d 1
jump loop lessThan d 3
# 现在我们将其打印刷新到信息板中
    printflush message1
```
