# iLiveSDK 1.4.0 更新说明

1.4.0版本修改了一些接口和命名空间，老版本用户更新到新版需要一定的工作量。对于不需要新功能的老用户来说，继续使用老版本SDK是一个不错的选择。所以我们仍然保留了[老版本的下载](http://dldir1.qq.com/hudongzhibo/git/iLiveSDK_PC_Suixinbo/iLiveSDK_1.3.1.0.zip)。

## 为什么改动了接口
为了能够支持各个VS版本（和其他编译器），我们替换了原有的std::string和std::vector等stl的内容；修改了一些类的实现，防止跨dll申请和释放资源；所有功能用抽象接口方式提供。另外，我们将各功能放入一个头文件中，方便调用和查阅。

## 老版本用户如何更新，成本多高
我们修改了个接口的参数类型，头文件位置，命名空间，原有的各接口的名称和功能没有改变。所以老用户将上述三者修改即可，不需要修改调用接口的逻辑。预计开发时间为1天。

## 老版本SDK是否还维护
我们会继续维护老版本，有任何使用问题欢迎反馈。

## 我应该使用哪个版本的SDK
新用户建议使用新版本（1.4.0及以上），老版本用户可以继续使用老版本。





腾讯云互动直播团队

