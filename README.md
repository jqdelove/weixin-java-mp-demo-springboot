# weixin-java-mp-demo-springboot

# 概述

微信公众号后台demo，引用微信开发者联盟的微信开发 Java SDK，进行简单的改造，用于测试公众号接口是否可用。主要测试了主动发送消息(客服消息)，使用了WxMpKefuMessage类创建客服消息，并且添加了用户发送消息的规则，发送内容为：接收消息用户的id+空格+发送的消息内容。

# 服务器启动后台

将项目打包成可执行jar包，上传到服务器，执行如下命令：

```shell
java -jar jar包名
```

该执行方式为实时查看后台输出日志，并且推出当前shell窗口即退出项目运行。使用nohup命令让项目在后台执行，并且执行日志输出目录：

```shel
nohup java -jar 项目名称.jar >/路径名称/输出的日志名称.log>&1&
```

# 配置微信URL

需要在该网址<https://mp.weixin.qq.com/debug/cgi-bin/sandboxinfo?action=showinfo&t=sandbox/index>配置接口的url，并且填写的token需要和项目中配置的token相同，微信才能正确请求该url，具体该url的用处请查看微信公众号开发文档。

