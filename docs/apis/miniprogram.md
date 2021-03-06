# 设备

## 振动

## vibrateLong(Object object)

使手机发生较长时间的振动（400 ms)


**参数**
Object object

| 属性         | 类型     | 默认值 | 是否必须 | 说明                 |
| ------------ | -------- | ------ | -------- | ------------------------------------------------------------------------------------------- | -------- |
| success      | function |        | 否       | 接口调用成功的回调函数                                                                                                                      |
| fail         | function |        | 否       | 接口调用失败的回调函数                                                                                                                      |
| complete     | function |        | 否       | 接口调用结束的回调函数（调用成功、失败都会执行）                                                                                            |
## vibrateShort(Object object)

**参数**
Object object

| 属性         | 类型     | 默认值 | 是否必须 | 说明                 |
| ------------ | -------- | ------ | -------- | ------------------------------------------------------------------------------------------- | -------- |
| success      | function |        | 否       | 接口调用成功的回调函数                                                                                                                      |
| fail         | function |        | 否       | 接口调用失败的回调函数                                                                                                                      |
| complete     | function |        | 否       | 接口调用结束的回调函数（调用成功、失败都会执行）                                                                                            |

## 电话

## makePhoneCall(Object object)

**参数**
Object object

| 属性         | 类型     | 默认值 | 是否必须 | 说明                 |支持平台|
| ------------ | -------- | ------ | -------- | ------------------------------------------------------------------------------------------- | -------- |
|phoneNumber      | string|        | 否       |需要拨打的电话号码                                                                                                                     |
| success      | function |        | 否       | 接口调用成功的回调函数       |微信                                                                                                               |
| fail         | function |        | 否       | 接口调用失败的回调函数                                                                                                                      |
| complete     | function |        | 否       | 接口调用结束的回调函数（调用成功、失败都会执行）                                                                                            |


## 网络

## getNetworkType(Object object)

获取网络类型

**参数**
Object object

| 属性         | 类型     | 默认值 | 是否必须 | 说明                 |
| ------------ | -------- | ------ | -------- | ------------------------------------------------------------------------------------------- | -------- |
| success      | function |        | 否       | 接口调用成功的回调函数                                                                                                                      |
| fail         | function |        | 否       | 接口调用失败的回调函数                                                                                                                      |
| complete     | function |        | 否       | 接口调用结束的回调函数（调用成功、失败都会执行）                                                                                            |


**object.success 回调函数**

Object res

| 属性       | 类型   | 描述                                       |支持平台|
| ---------- | ------ | ------------------------|------------------ |
| networkType       | string | 网络类型值 UNKNOWN / NOTREACHABLE / WIFI / 3G / 2G / 4G / WWAN |都支持|
| networkAvailable | Number |网络是否可用           |支付宝|



## onNetworkStatusChange(function callback)

监听网络状态变化事件

**参数**

function callback
网络状态变化事件的回调函数

**object.success 回调函数**

Object res

| 属性       | 类型   | 描述                                       |支持平台|
| ---------- | ------ | ------------------------|------------------ |
| networkType       | string | 网络类型值 UNKNOWN / NOTREACHABLE / WIFI / 3G / 2G / 4G / WWAN |都支持|
| isConnected | boolean |当前是否有网络链接           |都支持|

## 剪切板

##  getClipboardData(Object object)

获取系统剪贴板的内容

**参数**
Object object

| 属性         | 类型     | 默认值 | 是否必须 | 说明                 |
| ------------ | -------- | ------ | -------- | ------------------------------------------------------------------------------------------- | -------- |
| success      | function |        | 否       | 接口调用成功的回调函数                                                                                                                      |
| fail         | function |        | 否       | 接口调用失败的回调函数                                                                                                                      |
| complete     | function |        | 否       | 接口调用结束的回调函数（调用成功、失败都会执行）                                                                                            |

**object.success 回调函数**

Object res

| 属性       | 类型   | 描述                                       |
| ---------- | ------ | ------------------------|------------------ |
| data       | string | 剪贴板的内容

##  setClipboardData(Object object)

设置系统剪贴板的内容

**参数**
Object object

| 属性         | 类型     | 默认值 | 是否必须 | 说明                 |
| ------------ | -------- | ------ | -------- | ------------------------------------------------------------------------------------------- | -------- |
| data      | string |        | 是      | 剪贴板的内容                                                                                                                     |
| success      | function |        | 否       | 接口调用成功的回调函数                                                                                                                      |
| fail         | function |        | 否       | 接口调用失败的回调函数                                                                                                                      |
| complete     | function |        | 否       | 接口调用结束的回调函数（调用成功、失败都会执行）                                                                                            |

## 屏幕

## setKeepScreenOn(Object object)

设置是否保持屏幕长亮状态。仅在当前小程序生效，离开小程序后失效。

**参数**
Object object

| 参数         | 类型     | 默认值 | 是否必须 | 说明                 |
| ------------ | -------- | ------ | -------- | ------------------------------------------------------------------------------------------- | -------- |
| keepScreenOn      | string |        | 是      |是否保持屏幕长亮状态                                                                                                                    |
| success      | function |        | 否       | 接口调用成功的回调函数                                                                                                                      |
| fail         | function |        | 否       | 接口调用失败的回调函数                                                                                                                      |
| complete     | function |        | 否       | 接口调用结束的回调函数（调用成功、失败都会执行）                                                                                            |


## getScreenBrightness(Object object)

获取屏幕亮度

**参数**
Object object

| 参数         | 类型     | 默认值 | 是否必须 | 说明                 |
| ------------ | -------- | ------ | -------- | ------------------------------------------------------------------------------------------- | -------- |
| success      | function |        | 否       | 接口调用成功的回调函数                                                                                                                      |
| fail         | function |        | 否       | 接口调用失败的回调函数                                                                                                                      |
| complete     | function |        | 否       | 接口调用结束的回调函数（调用成功、失败都会执行）                                                                                            |

## setScreenBrightness(OBJECT)

设置屏幕亮度

**参数**
Object object

| 参数         | 类型     | 默认值 | 是否必须 | 说明                 |
| ------------ | -------- | ------ | -------- | ------------------------------------------------------------------------------------------- | -------- |
| value      | Number |        | 是       | 屏幕亮度值，范围 0 ~ 1。0 最暗，1 最亮                                                                                                                      |
| success      | function |        | 否       | 接口调用成功的回调函数                                                                                                                      |
| fail         | function |        | 否       | 接口调用失败的回调函数                                                                                                                      |
| complete     | function |        | 否       | 接口调用结束的回调函数（调用成功、失败都会执行）                                                                                            |

## boolean canIUse(string schema)

判断小程序的API，回调，参数，组件等是否在当前版本可用。


**参数**
string schema


使用 ${API}.${method}.${param}.${options} 或者 ${component}.${attribute}.${option} 方式来调用

**返回值**

boolean
当前版本是否可用

参数说明
* ${API} 代表 API 名字
* ${method} 代表调用方式，有效值为return, success, object, callback
* ${param} 代表参数或者返回值
* ${options} 代表参数的可选值
* ${component} 代表组件名字
* ${attribute} 代表组件属性
* ${option} 代表组件属性的可选值


代码示例：

```javascript
React.api.canIUse('getFileInfo')
React.api.canIUse('closeSocket.object.code')
React.api.canIUse('getLocation.object.type')
React.api.canIUse('getSystemInfo.return.brand')
React.api.canIUse('lifestyle')
React.api.canIUse('button.open-type.share')
```