# Typora + Github + PicGO 图床最佳实践



## 配置Github

```json
{
  "repo": "", // 仓库名，格式是username/reponame
  "token": "", // github token
  "path": "", // 自定义存储路径，比如img/
  "customUrl": "", // 自定义域名，注意要加http://或者https://
  "branch": "" // 分支名，默认是main
}
```

**1.** 首先你得有一个GitHub账号。注册GitHub就不用我多言。

**2.** 新建一个仓库Public-Pic-Bed

**3.** 生成一个token用于PicGo操作你的仓库：

访问：https://github.com/settings/tokens

然后点击`Generate new token`。

![img](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/generate_new_token.png)

仅仅把repo的勾打上即可。然后翻到页面最底部，点击`Generate token`的绿色按钮生成token。

![img](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/20180508210435.png)

**注意：**这个token生成后只会显示一次！你要把这个token复制一下存到其他地方以备以后要用。

![img](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/copy_token.png)



## 配置PicGo

直接安装下载下来的 EXE 文件即可，整个安装步骤一路 next 。安装后的软件界面如下：

![img](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/25/171aef00951db23b~tplv-t2oaga2asx-zoom-in-crop-mark:1304:0:0:0.awebp)

- 接下来配置 GitHub 作为图床，在左侧找到**图床设置**，找到**GitHub图床**。
- 前边有星号的为必填项，依次填入之前创建的仓库名，注意是：账户名/仓库名；

- 然后填入设定的分支名（创建仓库时如果没有创建其他分支，默认就是 master 分支）；
- 最后填入之前生成的 token 令牌，点击确定。

![image-20220322171449805](https://raw.githubusercontent.com/sunmiao0301/Public-Pic-Bed/main/imgfromPicGO/202203221714895.png)

- 然后找到 PicGo 设置，打开里边的 ***时间戳重命名***，这样可以避免图床在上传文件时，由于文件名相同造成的错误。
- 然后剩下的配置项可以不用管，参考的文章不建议设置为开机自启，因为等会配置好 typora 后，typora 在上传图片时会自动打开 PicGo 软件。
- 设置Server

![img](https://pic3.zhimg.com/80/v2-ae1e793a899aa33595e2d7f93a736b96_720w.jpg)



## Typora 设置

- 偏好设置

![img](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/25/171aef10a36f7831~tplv-t2oaga2asx-zoom-in-crop-mark:1304:0:0:0.awebp)

点击验证图片上传选项，测试是否成功
如看到验证成功，成功上传图片并获得最新的URL则表示成功
也可以直接在文档中插入图片来查看是否上传成功
**如果不出意外的话，到这里就可以成功上传图片并显示啦！**



p.s. 如果出现错误：Failed to fetch，这个错误参考文章经验，一般是由于端口设置错误造成的，此时需要打开 PicGo 设置，点击 **设置 Server**，此时监听的端口号需要与 Typora 中的端口号保持一致，一般默认就是 **36677**，只是需要去查看是否被篡改等等。
