# WxPusher
微信消息实时推送服务[WxPusher]，可以通过API实时给个人微信推送消息.[http://wxpusher.dingliqc.com/](http://wxpusher.dingliqc.com/)

# 使用说明

请直接访问官方说明文档[http://wxpusher.zjiecode.com/docs](http://wxpusher.zjiecode.com/docs)

## Java版本
[ ![version](https://img.shields.io/static/v1.svg?label=version&message=2.0.0&color=brightgreen) ](https://bintray.com/zjiecode/maven/wxpusher-client/1.0.0/link)

### gradle中使用

你需要添加Jcenter库，在“build.grade”中配置：
```groovy
dependencies {
    ......
    compile 'com.zjiecode:wxpusher-client:2.0.0'//使用上面的版本号
    ......
}
```

###  在maven中使用
在*pom.xml*文件中添加：
```xml
<dependency>
  <groupId>com.zjiecode</groupId>
  <artifactId>wxpusher-client</artifactId>
  <version>2.0.0</version>
  <type>pom</type>
</dependency>
```
最后可以在你需要的地方，直接调用方法，即可实时推送消息到微信上了，比如下面这样：
```java
Message message = new Message();
message.setAppToken("AT_qHT0cTQfLwYOlBV9cJj9zDSyEmspsmyM");
message.setContentType(Message.CONTENT_TYPE_TEXT);
message.setContent("不加限制的自由是很可怕的，因为很容易让任何人滑向深渊。");
message.setUid("c1BcpqxEbD8irqlGUh9BhOqR2BvH8yWZ");
message.setUrl("http://wxpuser.zjiecode.com");
Result result = WxPusher.send(message);

```

使用就是这么简单，有需要就看快来试试吧。
