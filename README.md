有时候，我们处于某些目的，要获取到淘宝、天猫、京东、拼多多、苏宁这些商城的服务器时间。

这个时间在抢购等情况下是非有用的，但很多人又不知道怎么正确的获取到这个时间，所以这里整理了一下获取方法，以供参考。

淘宝/天猫 http://api.m.taobao.com/rest/api3.do?api=mtop.common.getTimestamp

访问以上地址，会获得一下数据：

{"api":"mtop.common.getTimestamp","v":"*","ret":["SUCCESS::接口调用成功"],"data":{"t":"1605017462556"}} 这其中的

"data":{"t":"1605017462556"} 就是淘宝的服务器时间，通过时间戳转换，即可得到常规的时间，比如上面的1605017462556通过转换，就能得到2020-11-10 22:11:22。

京东 https://a.jd.com//ajax/queryServerData.html

同样的，访问上方的地址，得到以下数据：

{"serverTime":1605017683549} 转换后得到：2020-11-10 22:15:56。

2021年4月20日 更新

京东服务器时间请访问这个新的地址：https://api.m.jd.com/client.action?functionId=queryMaterialProducts&client=wh5

苏宁 http://quan.suning.com/getSysTime.do

访问上方地址，可以得到：

{"sysTime2":"2020-11-10 22:16:34","sysTime1":"20201110221634"} 不用转换时间戳，已经提供了两种数据形式。

原创文章，作者：蓝洛水深，如若转载，请注明出处：https://blog.lanluo.cn/9787
