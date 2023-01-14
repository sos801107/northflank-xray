> 平台官网 https://northflank.com

个人觉得其免费套餐还挺给力的，就是需要绑信用卡验证，创建免费的Project是不扣费的。
1. 如果是以Dockerfile的方式部署，建议容器里不要只放一个单独的xray，应该像ifeng大佬一样放一个前置的nginx做伪装页面，因为该平台容器有健康检测机制，如果容器内的http（或tcp、udp、http2、grpc）服务无响应，则会被认定为死容器，从而直接休眠。

2. 如果以从github导入代码的方式部署，平台会自动检测代码的编程语言，从而分配相应的运行时环境。

3. 本人adaptable-vless、railway-vless代码适用于该平台，直接导入即可，在选择协议类型时，如果你用ws那就选http，用grpc则选grpc。导入代码后，大概过五分钟才能看到效果，勿着急。
