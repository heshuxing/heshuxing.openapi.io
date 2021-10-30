## 常见问题<!-- {docsify-ignore-all} -->

***

* API 访问域名应该用哪个？

  如果和BLing公有云对接，应该采用 [https://bling-openapi.percent.cn](https://bling-openapi.percent.cn)；如果客户购买的是私有云服务，应该采用私有云地址进行对接；

* API 不满足需求怎么办？

  如果用户需要开放更多能力，可以联系<a href="mailto:bling-dev@percent.cn">bling-dev@percent.cn</a>，提出自己的场景以及需求。

* 客户端如何获取个人信息？

  客户端必须调用免登接口才可以获取自身信息。

* 如果用户不进行免登，服务端接口能获取到凭证（`accessToken`）吗？

  答案是：不需要。

  1）对于企业内部应用，服务端通过`appId`和`appSecret`可以获取`accessToken`，不需要组织信息。

  2）对于第三方应用，用户可以在首页URL中采用占位符的形式做到，使用**$ORGID$**做为参数占位符，BLing容器会将**$ORGID$**替换为当前访问用户的企业**$ORGID$**。

* 前端JSAPI鉴权需要注意什么？

  JSAPI鉴权需要注意按照示例代码逻辑严格执行，否则可能出现鉴权失败的风险。

* 如何测试应用？
  当用户需要对应用进行测试，可以将应用共享给其它组织使用。需要注意，共享给其它组织使用时，相当于是一个第三方应用。因此可以在首页URL中使用占位符**$ORGID$**。
