# hexo-blog-backup

#### 注意点：
- 1、准备

``` 
安装brew
安装node.js
安装git
安装npm
安装hexo
sudo npm install hexo-cli -g
安装自动化部署工具
npm install hexo-deployer-git --save （需要在博客目录执行）
发布
hexo clean && hexo g && hexo d
```
- 2、创建blog目录 如： hexo init blog
- 3、clone下来后取hexo-blog-backup目录中的工程配置文件，和主题目录替换刚创建的blog中的相应的文件
- 4、然后在blog目录执行npm install hexo-deployer-git  --save安装发布git
