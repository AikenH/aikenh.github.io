---
layout: post
title: Typora PicBed（Github）
​---  
<center>路漫漫其修远兮，吾将上下而求索<br>The road ahead will be long ,Our climb will be steep. </center>

---
初步了解：有待补充<br>Preliminary understanding: to be added
## Typora Pic-upload service setting （github）

​	用markdown记笔记的时候，图片往往是一个麻烦的步骤，想要结合Typora和github云同步的话，笔者在这里使用两种方式解决：

- [使用PicGo-Core（command line）设置github图床，自动转义url](#Pic-Bed)
- [插入自动复制图片，使用git上传github](#Git)


## Pic-Bed
<span id="Pic-Bed">
### 基本部署：

1. 在偏好设置中的图像，进行如下设置👇： 下载或更新PicGo-Cord(command line)

![image-20200512160643588](https://raw.githubusercontent.com/AikenH/md-image/master/img/image-20200512160643588.png)

2. 接着去Github中建立一个Repo：UserName/RepoName，用以存放图片（Public），简单的用readme初始建立即可。

3. 在Github的setting - developer setting-personal access tokens中新建token，指定简单的repo权限，并记录个人的token（只显示一次）
   **Attention：** 忘记记录的话，在token中也是通过update token（好像是这个名，获取新的值的）

4. Typora相应位置打开配置文件，并编写JSON如下：
   记得按照自己的情况修改

   ```json
   {
       "picBed": {
           "github": {
             "repo": "UserName/RepoName",
             "token": "your github token here",
             "path": "img/",
             "customUrl": "https://raw.githubusercontent.com/UserName/RepoName/master",
             "branch": "master"
           },
           "current": "github",
           "uploader": "github"
         },
         "picgoPlugins": {}
   }
   ```

5. 点击验证图片上传选项，进行测试，成功即可

### 存在问题：

用GIthub做图床的话，上传不是十分的稳定（可能需要依赖科学上网技术。请八仙过海，各显神通）。可以用其他的服务器作图床，大体过程应该也差不多，后续个人有更换的话在进行补充。


## Git
<span id="Git">
这里其实没什么说的，就是再上图设置中，将设置改为复制到本地，或者复制到相对文件夹，设置优先使用相对路径，然后后续用git将笔记和图片一起上传github即可。

Have Fun That‘s All！

---

<p align="right">Written by Aiken Hong </p>
<p align="right">2020-05-12</p>  

![8e4808464e922c641fdf084f2247b4698cb50d74](https://raw.githubusercontent.com/AikenH/md-image/master/img/8e4808464e922c641fdf084f2247b4698cb50d74.jpg)