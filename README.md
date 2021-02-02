<!--
 * @Description: 
 * @Date: 2021-01-24 10:09:37
 * @LastEditors: CK.Zh
 * @LastEditTime: 2021-01-24 13:48:12
 * @FilePath: \undefinede:\source\virtualkvm_doc\README.md
-->
# VirtualKVM User's Guide
VirtualKVM 用户指南

## 快速开始

1. 使用USB线连接`HOST`口到`主控机`
2. 使用USB线连接`SLVAE`口到`被控机`，使用HDMI线连接`HDMI`口到`被控机`视频输出口
3. 在主控机上打开`VirtualKVM`客户端软件

## 客户端下载

[Virtual KVM Releases→](https://github.com/autolaborcenter/virtualkvm_doc/releases/)


## 客户端功能

| 菜单  | 功能                          | 备注 |
|-------|-------------------------------|--------|
| `输入`  | 选择视频流输入设备 | 默认选择为VirtualKVM硬件 |
| `画质` | 选择客户端内画面的尺寸、帧率及比例 | 默认选择为 1280*720(16:9)@60FPS <br/> 建议设置为与被控机相同的分辨率或画面比例 |
| `声音`  | `输入` <br/> `输出`   | 选择或禁用主控机的声音来源  <br/>  选择或禁用主控机的声音输出 |
| `捕获`  | `截屏` <br/>  ~~`开始录像`~~ <br/> `更改文件夹` <br/>  `打开...`| 截取被控机当前画面为图片 <br/>  ~~录制被控机当前画面为视频~~（该功能暂不可用） <br/> 选择截屏/录像文件保存位置 <br/>  打开截屏/录像文件的存储目录 |
| `输出` | 选择键鼠数据流输出设备                  | 默认选择为VirtualKVM硬件 |
| `模式`  | `默认` <br/> `类Unix` | 被控机为`Windows`平台时选择  <br/>  被控机为`Linux`、`Android`、`macOS`等类Unix平台时选择 |
| `关于`  | `帮助` <br/> `关于` | 查看帮助文档及软件更新  <br/>客户端软件的构建信息 |
| `显示`  | `光标` <br/> `全屏` | 设置是否显示主控机本身的光标   <br/>  设置客户端软件进入/退出全屏 |

## 硬件接口及指示灯

| 接口  | 功能                          | 连接至 |
|-------|-------------------------------|--------|
| `HOST`  | 视频数据流输出 <br/> 键鼠数据流输入 | 主控机 |
| `SLAVE` | 键鼠数据输出                  | 被控机 |
| `HDMI`  | HDMI视频数据输入              | 被控机 |

******

| 指示灯| 功能             | 常亮●               | 熄灭○               | 闪烁◐                   |
|------|------------------|--------------------|--------------------|------------------------|
| `STA1` | 视频采集（硬件） | 工作中             | 未工作             | N/A                    |
| `STA2` | 键鼠模拟（硬件） | 工作中             | 未工作             | N/A                    |
| `STA3` | 预览画面（软件） | 主控机正在预览画面 | 主控机未在预览画面 | N/A                    |
| `ENUM` | 键鼠枚举（软件） | 被控机已识别键鼠   | 被控机未识别键鼠   | N/A                    |
| `UP`   | 键鼠通信（软件） | N/A                | N/A                | 键鼠数据发送至被控机 |


## 常见问题

* “`ENUM`灯已点亮，为什么主控机无法控制被控机？”

    如果被控机是`Windows`平台，请在客户端软件的`模式`选项中点选`默认`
    如果被控机是`Linux`、`Android`、`macOS`等类Unix平台，请在客户端软件的`模式`选项中点选`类Unix`

* “为什么在客户端看到的画面模糊/有畸变？”

    请将客户端的`画质`设置为与`被控机`输出分辨率相同
    或设置两者的画面比例为相同

* “被控机是笔记本或已经连接了显示器，该如何使用VirtualKVM？”

    请将`被控机`的显示输出设置为`镜像模式`

* “如何使被控机的声音通过主控机输出？”

    * 设置`被控机`的音频输出为`HDMI`
    * 确保所用HDMI线支持音频传输
    * 取消`主控机`麦克风静音（部分笔记本可能具有类似功能），麦克风权限对VirtualKVM开放


* “哪些设备可以作为被控机？”

    树莓派、JetsonNANO、笔记本电脑、台式电脑、电视盒子、Nintendo Switch、Smartisan TNT、三星手机PC模式、华为手机PC模式.....
    
    理论上任何支持HDMI输出和键鼠输入的设备都可使用
    
## 反馈

> 欢迎通过下方链接向我们发送任何使用问题或反馈意见

[ISSUES→](https://github.com/autolaborcenter/virtualkvm_doc/issues/)
