# EBook Workshop
 ![Logo 4 EbookWorkshop](https://avatars.githubusercontent.com/u/132744849)    
这是一个用于采集文章并整理成电子书的工具。采集的来源可以是在线网页、Txt文件、pdf文件[^1]。可以输出Pdf格式、Txt格式文件。并支持发送到邮箱（比如 Kindle 邮件同步）。    

做这个的初衷是为了方便将Txt文件打包成Pdf发到 Kindle —— 有一段时间Kindle直接看 Txt 文件会出现吞行的现象。    
后来是为了方便将在线阅读的章节整本盘下来在 Kindle 看 —— Kindle 上看网页那体验实在不好，而且也不一定一直能联网。    
到目前，整个项目该有的功能应该都有了。    

## 程序结构
本工具含前端项目：前端项目（ https://github.com/EbookWorkshop/Front-end ）、服务器项目（ https://github.com/EbookWorkshop/Api ），需要同时运行才能正常工作。

## Release  
最新版下载
[EbookWorkshop-FrontEnd@lasest](https://github.com/EbookWorkshop/Front-end/releases/latest)    
[EbookWorkshop-Api@lasest](https://github.com/EbookWorkshop/Api/releases/latest)

## 如何使用
要跑起本项目，需要掌握一点命令行操作知识，node运行知识，npm包安装知识。    
若想使用项目，还需要掌握一点相关知识：CSS采集器规则[^2]，正则表达式[^3]等。    

### 运行[^4]
1. 拉取或下载前端项目（ https://github.com/EbookWorkshop/Front-end ）、服务器项目（ https://github.com/EbookWorkshop/Api ）到本地。
1. 初始化运行环境 —— 分别进入上述项目，执行安装命令： `npm install --registry=http://registry.npmmirror.com` 直至没有错误提示为止。实际情况可能出现各种错误。部分可以通过重试安装命令解决。
1. 运行项目——进入前端项目，执行命令`npm run dev`；在服务器项目执行命令`node app`
    
若一切顺利，则会在浏览器自动打开项目首页。
    
当然，不顺利的情况就多种多样了，总的来说是npm包安装不上。这个不方便一一展开说，不同的环境有不同的现象。    

[^1]:pdf 的只能按源文件存储，不能采集分析内容    
[^2]:用于采集网页内容。CSS规则用于描述需要采集的内容在网页中的元素位置
[^3]:正则表达式描述的是查找匹配规则的文本，如：设置分割Txt文件章节规则（通过命中章节标题分割章节）、设置自动校阅规则（将命中的内容自动改为想要的结果）    
[^4]:需要本地已安装Node（ https://nodejs.org/ version >= v22.0.0）
