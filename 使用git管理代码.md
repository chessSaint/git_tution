# 使用git管理代码

## 一、配置git

1. 设置用户名称和登陆邮箱；

   ```bash
   # 用户名称指的是项目斜杠前的那个，比如有个项目为git_tution，在查看项目code的界面，chessSaint/git_tution中的chessSaint就是用户名称
   git config --global user.name '用户名称'
   git config --global user.email '登陆邮箱'
   ```

2. 本地生成密钥

   ```bash
   ssh-keygen -t rsa -C '登陆邮箱'
   ```

   输入上述命令后，连续回车，会在对应目录下生成id_rsa和id_rsa.pub文件，其中：

   - `id_rsa`文件是私钥，要保存好，放在本地，私钥可以生产公钥，反之不行。

   - `id_rsa.pub`文件是公钥，可以用于发送到其他服务器，或者git上。

3. 远端github上配置公钥，打开生成的id_rsa.pub文件并复制全部内容。然后登陆github个人账号中，点击设置---ssh keys---new ssh keys项，将刚刚复制的文件内容粘贴保存，即配置完毕。

## 二、创建新项目/托管本地项目/克隆已有项目

### 1. 没有本地和远程项目

登陆git账户，点击上方导航栏中的`+`按钮，如图所示：

![image-20220513144321529](https://upload-images.jianshu.io/upload_images/9989643-38cf64b03df91fb4.png?imageMogr2/auto-orient/strip|imageView2/2/w/880/format/webp)
