<!--
 * @Description: 
 * @Date: 2021-01-24 10:09:37
 * @LastEditors: CK.Zh
 * @LastEditTime: 2021-01-24 11:55:44
 * @FilePath: \undefinede:\source\virtualkvm_doc\README.md
-->
# VirtualKVM doc
虚拟KVM文档

## 快速开始

1. 使用USB线连接`HOST`口到主机电脑
2. 使用USB线连接`SLVAE`口到被控设备，使用HDMI线连接`HDMI`口到被控设备视频输出口
3. 在主控电脑上打开`VirtualKVM APP`

## 接口及指示灯


| 接口  | 功能                          | 连接至 |
|-------|-------------------------------|--------|
| HOST  | UVC视频数据输出 </br> 键鼠数据输入 | 主控机 |
| SLAVE | 键鼠数据输出                  | 被控机 |
| HDMI  | HDMI视频数据输入              | 被控机 |



| 指示灯| 功能             | 常亮●               | 熄灭○               | 闪烁◐                   |
|------|------------------|--------------------|--------------------|------------------------|
| STA1 | 视频采集（硬件） | 工作中             | 未工作             | N/A                    |
| STA2 | 键鼠模拟（硬件） | 工作中             | 未工作             | N/A                    |
| STA3 | 预览画面（软件） | 主控机正在预览画面 | 主控机未在预览画面 | N/A                    |
| ENUM | 键鼠枚举（软件） | 被控机已识别键鼠   | 被控机未识别键鼠   | N/A                    |
| UP   | 键鼠通信（软件） | N/A                | N/A                | 键鼠数据已发送至被控机 |

## 客户端下载

[VirtualKVM_win_x64](./app/VirtualKVM_win_x64.exe)

[VirtualKVM_win_x64_x86](./app/VirtualKVM_win_x64_x86.exe)