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

填写好项目的各项信息之后，点击create repository按钮，出现类似如下界面，说明项目创建成功。

![image-20220513144321529](https://upload-images.jianshu.io/upload_images/9989643-32e3d2a3f1f51892.png?imageMogr2/auto-orient/strip|imageView2/2/w/1046/format/webp)

https://www.jianshu.com/p/6e1de95828a8#:~:text=Git%E5%9F%BA%E6%9C%AC%E9%85%8D%E7%BD%AE%201%E3%80%81%E9%85%8D%E7%BD%AEgit%EF%BC%9A%20%EF%BC%881%20%EF%BC%89%E8%AE%BE%E7%BD%AE%E7%94%A8%E6%88%B7%E5%90%8D%E7%A7%B0%E5%92%8C%E7%99%BB%E5%BD%95%E9%82%AE%E7%AE%B1%20git%20config%20--global%20user.name,%E6%89%93%E5%BC%80.ssh%E6%96%87%E4%BB%B6%E5%A4%B9%E4%B8%8B%E7%9A%84id-rsa.pub%E6%96%87%E4%BB%B6%E7%9A%84%E5%86%85%E5%AE%B9%EF%BC%8C%E5%85%A8%E9%83%A8%E5%A4%8D%E5%88%B6%E3%80%82%20%E7%84%B6%E5%90%8E%E7%99%BB%E5%BD%95%E4%BD%A0%E7%9A%84git%E6%9C%8D%E5%8A%A1%E5%99%A8%E4%B8%AA%E4%BA%BA%E8%B4%A6%E6%88%B7%E8%AE%BE%E7%BD%AE%E4%B8%AD%EF%BC%8C%E5%AF%BB%E6%89%BEssh%20key%E8%8F%9C%E5%8D%95%E9%A1%B9%EF%BC%8C%E7%84%B6%E5%90%8E%E7%B2%98%E8%B4%B4%E5%8D%B3%E5%8F%AF%E3%80%82%20%E5%A6%82%E4%B8%8B%E5%9B%BE%E6%89%80%E7%A4%BA%EF%BC%9A%20%E9%85%8D%E7%BD%AESSH%20Key%202%E3%80%81%E5%88%9B%E5%BB%BA%E6%96%B0%E9%A1%B9%E7%9B%AE%2F%E6%89%98%E7%AE%A1%E6%9C%AC%E5%9C%B0%E9%A1%B9%E7%9B%AE%2F%E5%85%8B%E9%9A%86%E5%B7%B2%E6%9C%89%E9%A1%B9%E7%9B%AE%EF%BC%9A%20%E5%BD%93%E5%AE%8C%E6%88%90%E7%AC%AC1%E6%AD%A5%E7%9A%84git%E9%85%8D%E7%BD%AE%E5%90%8E%EF%BC%8C%E5%B0%B1%E8%AF%A5%E5%8E%BB%E6%91%86%E5%BC%84%E9%A1%B9%E7%9B%AE%E4%BA%86%E3%80%82
