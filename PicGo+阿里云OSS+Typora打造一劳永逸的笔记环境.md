# PicGo+Typora+阿里云OSS,打造一劳永逸的笔记环境

## 1. 前提准备

- PicGo
- Typora
- 域名(已备案,可访问),有最好,没有也可以
- 阿里云OSS

> PS: **上面资源如果没有准备好,可直接翻滚到后面的资源准备,有更详细的准备文档**

## 2. PicGo配置

打开PicGO,依次点击: 图床设置 => 阿里云OSS

![image-20210531230550229](http://oss.emier.cn/images/20210601003543.png)

上面需要填的东西不少,不着急,很简单,向下看!

**返回到阿里云官网,将鼠标放在右上角头像上,点击`访问控制`**

![image-20210531230758736](http://oss.emier.cn/images/20210601004112.png)



点击人员管理下的 `用户` => `创建用户`

![image-20210531231058110](http://oss.emier.cn/images/20210601004124.png)

创建用户需要注意: **访问方式选择编程访问**

![image-20210531231331324](http://oss.emier.cn/images/20210601004210.png)

新建用户完成,拿到`AccessKey ID` 和 `AccessKey Secret`,且只有这一次机会可以拿到,关闭页面后将无法再次获取,所以记得保存好.

![image-20210531231650057](http://oss.emier.cn/images/20210601004222.png)



选中,点击`添加权限`

![image-20210531232106736](http://oss.emier.cn/images/20210601004233.png)

弹出弹框,选择第二个`AliyunOSSFullAccess`的权限就OK了,然后`确定` => `完成`

![image-20210531232416746](http://oss.emier.cn/images/20210601004247.png)

到这,所有的阿里云的配置基本就完成了,然后打开PicGo的阿里云OSS配置界面,先把ID和Key填上,就是刚刚复制的`AccessKey ID`和`AccessKey Secret`

![image-20210531233630589](http://oss.emier.cn/images/20210601004302.png)

> 存储空间名: Bucket名称
>
> 存储区域: 且看下图,比如我,就是: oss-cn-beijing
>
> 注定存储路径: 就是给个文件夹名称,注意后面要加`/` , 比如我的: `images/`

![image-20210531233824173](http://oss.emier.cn/images/20210601004317.png)



PicGo设置到这里的话,点击确定 ,就可以正常使用了,点击上传区,可以上传试试了~

如果**有域名且备案**的同志可以继续向下看一下,给加个域名,如果不加域名的话,就会是: `https://emier-oss.oss-cn-beijing.aliyuncs.com/images/20210531233503.png`,像这样,总感觉不太对~(**没有的话可以跳过,去看Typora的配置了**)

> 下面是域名相关配置

域名购买与备案不说了,很简单,如果想要购买域名的话,可以去阿里云官网购买~

进入资源包概览界面,点击`传输管理` => `域名管理` => `绑定域名`

![image-20210531234950219](http://oss.emier.cn/images/20210601004330.png)



![image-20210531235217434](http://oss.emier.cn/images/20210601004345.png)



填写完成后,点击提交~

然后来到PicGo,在`自定义域名`中填入域名,点击确定

我上传了一张图片试了下,`http://oss.emier.cn/images/20210531235913.png`,完美!

> PS: **到这的话可以去看第3节点Typora的配置了,但还可以再给他加点东西,有兴趣的继续往下看!**

在PicGo中安装两个插件,一个可以上传后将URL复制到剪贴板,一个可以上传前压缩图片的插件

![image-20210601001457854](http://oss.emier.cn/images/20210601004358.png)

然后安装成功之后点击下角的配置按钮可以稍微配置一下,压缩的插件记设置完成之后要在点击小齿轮启用一下~

刚刚试了一下,5.6M的压缩成1.2M的,而且我用的是TinyPng的无损压缩,还不错~Nice~就是时间稍微长了一点,看个人喜好吧,不喜欢等待的可以关掉~

## 3. Typora配置

`文件` => `偏好设置`

![image-20210601003006054](http://oss.emier.cn/images/20210601004411.png)

选择`图像`,配置很简单,看下图:

![image-20210601003316666](http://oss.emier.cn/images/20210601004423.png)

然后点击`验证图片上传选项`验证一下:

![image-20210601003156683](http://oss.emier.cn/images/20210601004435.png)



看! 很稳! 

可以在从Typora中上传图片测试一下,自动将本地图片替换成了网络地址,完美!

还可以对之前本地的图片进行单个上传,或者全部本地图片上传

![image-20210601003657498](http://oss.emier.cn/images/20210601004451.png)

![image-20210601003944658](http://oss.emier.cn/images/20210601003947.png)



> PS: 在Typora设置自动上传的时候,要记得开启PicGo的Server服务,且端口必须为`36677`,这个是默认的,不需要改动,就是怕各位瞎点,所以说一下~
>

![image-20210601061736340](http://oss.emier.cn/images/20210601061738.png)

![image-20210601061815294](http://oss.emier.cn/images/20210601061817.png)



## 资源准备

### PicGo&&Typora安装包

> 链接：https://pan.baidu.com/s/1BbtZx5gphkHjPFrYMWi7uA 
> 提取码：3321 
> 复制这段内容后打开百度网盘手机App，操作更方便哦--来自百度网盘超级会员V4的分享

### 域名及备案

傻瓜式点点点操作,自己解决~

> 域名购买地址: [一键直达](https://wanwang.aliyun.com/domain?source=5176.11533457&userCode=jsnk8fj8)

### 阿里云OSS与域名相关配置及操作

#### 1. 阿里云OSS资源购买

> OSS购买地址:  [购买链接](https://www.aliyun.com/product/oss?source=5176.11533457&userCode=jsnk8fj8)  
>
> PS: 有购买意愿的朋友可以点击下我的购买链接,毕竟确实有优惠~而且最近也618搞活动,力度巨大~[活动地址](https://www.aliyun.com/activity/618/2021?source=5176.11533457&userCode=jsnk8fj8)

![image-20210531222851610](http://oss.emier.cn/images/20210601004509.png)

> 如果是第一次使用OSS不太了解的话,可以按我的购买配置来~
>
> 然后点击立即购买就可以了.

购买成功之后,如下图查看自己的资源包

![image-20210531223308488](http://oss.emier.cn/images/20210601004523.png)

#### 2. Bucket创建

点击按钮,新建Bucket

![image-20210531224331518](http://oss.emier.cn/images/20210601004536.png)

![image-20210531224447545](http://oss.emier.cn/images/20210601004548.png)

确定之后,我们就来到了Bucket的概览界面,资源包购买完成~

前提准备已经完成,可以去看PicGo的配置了!

#### 3.流量包

> 阿里云默认开通的是按量付费,具体可以去官网看下
>
> https://cn.aliyun.com/price/detail/oss

按量付费不知道有没有坑,希望有了解的朋友可以告诉我一下,我之前一直用的是按量付费,好像也没花什么钱,应该是流量太少了~
