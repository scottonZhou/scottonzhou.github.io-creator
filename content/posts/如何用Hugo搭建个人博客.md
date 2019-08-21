---
title: "如何用Hugo搭建个人博客(Windows 10)"
date: 2019-08-21T23:45:19+08:00
draft: false
---

![](/images/img1.png)

具体操作步骤如下：

1. 前往Hugo官网(gohugo.io)下载安装程序，并完成本地安装；


2. 选定用于存放创建博客的目录(没有可自行创建)，并通过命令行操作进入该目录；


3. 命令行操作：'hugo new site xxxxxx.github.io-creator' (xxxxxx均为小写，并与github的ID保持一致)；


4. 通过命令行进入上一步操作后生成的目录；


5. 命令行操作：'git init'，创建本地仓库；


6. 命令行操作: 'git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke','echo 'theme = "ananke"' >> config.toml' 完成主题添加；


7. 命令行操作:'hugo new posts\文章标题.md' 创建新文章;


8. 通过vscode编辑文章内容（markdown）；


9. 命令行操作: 'hugo server -D' 开启本地服务，以便访问'http://localhost:1313/'，若通过'ctrl+c'关闭服务，则无法访问；


10. 配置主题 config.toml;


11. 命令行操作：'hugo'(此时可新建终端执行命令)，生成public目录；


12. 在外层目录下新建gitignore目录，添加内容'//public//'，避免后续创建的.git本地仓库发生冲突；


13. 命令行操作进入public目录，执行'git init'，生成本地仓库；


14. 分别执行'git add .' ， 'git commit -v' ;


15. 前往Github新建仓库，名为xxxxxx.github.io(xxxxxx均为小写，并与github的ID保持一致);


16. 通过命令行将public的本地仓库'push'上传至远程仓库；


17. setting >> Github pages 进行相应配置和自定义域名等操作；


18. HTTPS不开启，便于测试；


19. 在Github创建新的仓库(名称xxxxxx.github.io-creator)，并将xxxxxx.github.io-creator的本地仓库上传至该仓库，完成备份。

Hugo官方教程参考：https://gohugo.io/getting-started/quick-start/
![](/images/img2.png)