﻿获取access_token
==================

.. Note::

    获取access_token之前，请先申请client_Id、client_secret、subscriptionKey。:doc:`issues`


- 调用各接口时都需使用access_token。开发者需要进行妥善保存。
- access_token的有效期目前为24个小时。

平台的API调用所需的access_token使用及生成方式说明：

1、建议开发者使用中控服务器统一获取和刷新Access_token，其他业务逻辑服务器所使用的access_token均来自于该中控服务器，不应该各自去刷新，否则容易造成冲突，导致access_token覆盖而影响业务；

2、目前Access_token的有效期通过返回的expire_in来传达，目前是7200秒之内的值。中控服务器需要根据这个有效时间提前去刷新新access_token；

3、Access_token的有效时间可能会在未来有调整，所以中控服务器不仅需要内部定时主动刷新，还需要提供被动刷新access_token的接口，这样便于业务服务器在API调用获知access_token已超时的情况下，可以触发access_token的刷新流程。


接口地址
__________

https请求方式: POST

地址：https://ids.shingsou.com/connect/token

参数说明
__________

grant_type	是	填写client_credential

client_Id	是	第三方用户唯一凭证

client_secret	是	第三方用户唯一凭证密钥

返回说明
__________

正常情况下，会返回下述JSON数据包：

{"access_token":"ACCESS_TOKEN","expires_in":7200}