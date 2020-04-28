---
layout: post
title: （Pytorch） Colab Tensorboard 
---  
<center>路漫漫其修远兮，吾将上下而求索<br>The road ahead will be long ,Our climb will be steep. </center>

---
初步了解：有待补充<br>Preliminary understanding: to be added
## How to lunch TensorBoard on Colab

对Tensorboard的编写参数的输入啥的**不需要另外改变**<br>
只是在lunch Tensorboard 的时候输入如下👇的命令：
```
%load_ext tensorboard
%tensorboard --logdir './runs'
```
就能在输出栏中看到代码输出的Tensorboard了<br>

~~当然挂载GoogleDrive后，将Tensorboard的Log下载到本地再执行tensorboard，也没人拦着23333~~

---


<p align="right">Written by Aiken Hong </p>
<p align="right">2020-04-28</p>  

![HitMan2](/images/p3-1.jpg)
