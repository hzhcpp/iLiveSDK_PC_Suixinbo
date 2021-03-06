## PC_iLiveSDK_ChangeList

###### V1.4.1(2017-07-11)
* 修正1.4.0的bug;
* 增加系统声音采集功能;

###### V1.4.0(2017-07-03)
iLiveSDK接口重构,大大降低了sdk的接入难度，主要以下几方面优化,
* 支持VS的各个版本接入;
* 所有接口在主线程中进行回调;
* 用户不再需要手动请求画面,sdk可以自动请求画面;
* 美颜功能优化，大大提升美颜质量;

###### V1.3.1(2017-03-13)
* 增加自定义采集功能;
* 增加麦克风和扬声器音量控制接口;
* 内部优化;

###### V1.3.0(2017-03-06)
* 错误码优化;
* 命名空间优化;
* bug修正: 异常退出房间后，再次登录，会收到之前所在房间的消息;为修正此bug，对接口进行了如下修改: <br/>
	(1) SetConnCallBack()接口去掉;<br/>
	(2) SetForceOfflineCallback()接口移动到iLiveLoginMgr类里;<br/>
	(3) SetMessageCallBack()分解为setGroupMessageCallBack()、setC2CMessageCallBack()、setSysemMessageCallback()三个接口，并放到iLiveRoomMgr里面;

###### V1.2.2(2017-02-27)
* 代码注释修正;
* 内部实现优化;

###### V1.2.1(2017-02-20)
* iLiveSDK日志文件规范化;
* iLiveSDK自动清理日志文件(7天前);
* 增加屏幕分享指定窗口句柄的接口;
* iLiveRoomOption结构修改:<br/>
	(1) 增加m_autoRecvScreenListener成员;<br/>
	(2) 增加m_autoRecvMediaFileListener成员;<br/>
	(3) m_autoRecvListener成员改名为m_autoRecvCameraListener;<br/>

###### V1.2.0(2017-02-13)
* 更新avsdk1.8.5;
* 增加美白、美颜、屏幕分享过程中动态修改分享区域大小接口;
* 接口变动:<br/>
	(1) iLiveRoomOption.h: iLiveRoomDisconnectListener 函数指针添加errorinfo字段;<br/>
	(2) iLiveRoomOption.h: iLiveRoomOption结构体添加字段screen_recv_mode;<br/>
	(3) iLiveRoomMgr.h: requestViewList、cancelViewList、cancelAllView 接口返回值由int改为void;<br/>
	(4) iLiveRoomMgr.h: 增加changeScreenShareSize接口;<br/>
	(5) iLiveRoomMgr.h: openScreenShare接口参数改为引用方式;<br/>

###### V1.0.0(2017-01-16)
* iLiveSDK第一个版本，实现互动直播主线流程以及主要接口的封装,并与已有的Android、IOS平台实现互通;
* 主线流程：包括注册，登录，创建房间，加入房间，退出房间，推流、录制;
* 主要接口：请求/取消画面，相机，麦克风，扬声器相关操作，角色、权限修改，群组消息、C2C消息收发，推流、录制相关操作;
