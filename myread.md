Node-Webkit是一个基于Chromium和Node.js运行平台。它能让你把HTML5应用打包成本地桌面应用或游戏安装到Windows、Linux或Mac系统中。Node-Webkit项目是由英特尔开源技术中心开发，发起人是王文睿。

为什么Node-WebKit是开发HTML5本地桌面应用的最佳选择
Node-WebKit能把你的HTML5应用打包成本地桌面应用，在Windows、Linux或Mac平台上，你不需要其它依赖就可以独立运行你的HTML5应用。
它支持Node.js。你可以使用Node.js的所有模块来开发你喜欢的app或游戏。不仅你可以使用Node.js原生的模块，而且可以使用第三方的node.js模块。
如何使用Node-Webkit开发HTML5本地桌面应用
这非常简单，像传统的开发你的HTML5应用一样开发它们，完成之后用Node-Webkit打包它。打包的方法是
```
1.先下载Node-Webkit
2.然后创建一个包文件命名为package.json, 写入下面的代码：
{
  "name": "nw-demo",
  "main": "index.html"
}
这里的“name”是你应用的名称，“main”是你的应用的启动文件，也就是应用启动是第一加载的文件。

3.将你的HTML5应用文件和package.json一起打包成zip
4.重命名zip文件，将其后缀变成 .nw ，比如app.nw
5.现在你就可以用node-webkit runtime来运行你的app了在Linux上的运行命令是
./nw app.nw
在Windows平台上你可以直接把你的app.nw拖拽到 nw.exe 程序上就行了。

6.想让你的应用更容易传播和发布，可以将它和node-webkit封装到一起，也就是将你的HTML5应用 app.nw 和 nw.exe 合成一个可执行文件。在Linux上的做法是
cat /usr/bin/nw app.nw > app && chmod +x app
在Window上的做法是

copy /b nw.exe+app.nw app.exe
```
