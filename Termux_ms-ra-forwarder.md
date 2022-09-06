ZeroTermux: [https://od.ixcmstudio.cn/repository/main/ZeroTermux/ZeroTermux-0.118.22.apk](https://od.ixcmstudio.cn/repository/main/ZeroTermux/ZeroTermux-0.118.22.apk)

## 安装依赖
(出现选择Y/n之类的提示就直接回车)

`pkg install python`

`pkg install nodejs`

`pkg install git`

## 克隆项目
`git clone https://github.com/wxxxcxx/ms-ra-forwarder`

(如因网络问题导致失败可换成这条命令`git clone https://ghproxy.com/https://github.com/wxxxcxx/ms-ra-forwarder`）

## 进入目录
`cd ms-ra-forwarder`

## 安装项目依赖并运行
`npm install`

`npm run start`

## 最后
Web访问地址: [http://localhost:3000](http://localhost:3000)

#### 下次打开Termux用以下命令运行项目:

*~~cd ms-ra-forwarder~~*

*~~npm run start~~*

***~~或者合并为一条命令:~~***
*~~cd ms-ra-forwarder && npm run start~~*

### 推荐使用别名方式:

执行这条命令设置永久别名:

`echo 'alias tts="npm start -prefix ~/ms-ra-forwarder"'>>$PREFIX/etc/bash.bashrc`

下次打开Termux使用命令

`tts`

即可一键运行。

