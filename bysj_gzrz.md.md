# 毕业设计工作日志

现在是2023/2/27，wafer首次尝试markdown的方式进行笔记的记录。

~~以下为本人弱的要死但是还是坚持要写的工作日志~~

# 1.基础部分

本部分内容是参考b站某个大佬，~~已经忘了是谁了哈哈哈。大佬对不起！~~

## 1.1Python

Python学习用的是Python编程从入门到实践这本书。目前是把第一部分给刷完了，但是感觉还是有点囫囵吞枣的感觉。

~~后期这次毕业设计水完了之后感觉得对着菜鸟网站一个个学。~~

[Python](https://www.runoob.com/python3/python3-tutorial.html)

## 1.2数学基础

~~这一部分彻底摆烂哈哈哈。但是还是把需要的书列出来把！~~

1. 高等数学
2. 线性代数
3. 概率论
4. 最优化方法

## 1.3两个packgae

~~这一部分也摆烂了。我超我到底干了什么东西？后续有机会学的话我还是再来吧！~~

[NumPy](https://www.runoob.com/numpy/numpy-tutorial.html)

[Pandas](https://www.runoob.com/pandas/pandas-tutorial.html)

## 1.4Pytorch

终于终于，开始算是做了点什么了。

### 1.4.1Anaconda3

这一部分似乎没有出任何问题~

但是还是把官网给码一下，~~防止以后脑抽会回来看~~~

[Anaconda3](https://www.anaconda.com/)

### 1.4.2Pytorch安装

要安装Pytorch是要在anaconda里面配置环境，大概是这几个很关键的代码：

`conda create -n pytorch python=3.9`

`conda activate pytorch`

再然后就是安装了。按照官网的方法安装显然是不行的，官网的神秘代码如下：

`conda install pytorch torchvision torchaudio pytorch-cuda=11.6 -c pytorch -c nvidia`

---

因此我开始寻找方法，我找到了两类方法，一个是conda，一个是pip，前者我没办法实现但是还是把他给码出来吧：

[conda法](https://blog.csdn.net/zzq060143/article/details/88042075?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167750769916800213057471%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167750769916800213057471&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-88042075-null-null.142^v73^control_1,201^v4^add_ask,239^v2^insert_chatgpt&utm_term=%E6%B8%85%E5%8D%8E%E6%BA%90%E5%AE%89%E8%A3%85pytorch&spm=1018.2226.3001.4187)

```
#conda法
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes
conda install pytorch torchvision torchaudio pytorch-cuda=11.6
```

对于conda法，需要注意下面几个东西

1. cuda的等级
2. 官网代码后面那些强制定位到国外网站的东西要杀掉

---

下面是我是用成功的方法~

[pip法](https://blog.csdn.net/weixin_44864260/article/details/127770525?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167724188316800215060588%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=167724188316800215060588&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~times_rank-2-127770525-null-null.142%5ev73%5econtrol_1,201%5ev4%5eadd_ask,239%5ev2%5einsert_chatgpt&utm_term=pytorch%E7%8E%AF%E5%A2%83%E6%90%AD%E5%BB%BA&spm=1018.2226.3001.418)

大意是在下面网站处下载，请注意版本对应。torch和torchvision都需要下载，我下载的版本分别是

`torch-1.12.0+cu116-cp39-cp39-win_amd64.whl`

`torchvision-0.13.0+cu116-cp39-cp39-win_amd64.whl`

[下载链接](https://download.pytorch.org/whl/torch_stable.html)

[版本对应](https://pypi.org/project/torchvision/)

完成上述内容后就可以进行安装，建议先安装torch，再安装torchvision

`pip install torchvision`

`pip install torch`

对于pip法，需要注意下面几个东西

1. 要注意房子里面python的版本
2. 要注意cuda的版本
3. 要注意torch和torchvision版本对应

### 1.4.3Pytorch练习

这部分内容按照B站小土堆视频进行学习。

[视频链接](https://www.bilibili.com/video/BV1hE411t7RN/?spm_id_from=333.337.search-card.all.click)

---

验证pytorch的可行性

```
import torch
print(torch.__version__)
print('gpu', torch.cuda.is_available())
```

出来的结果是下面内容就是没问题啦

```
1.12.0+cu116
gpu True
```

---
