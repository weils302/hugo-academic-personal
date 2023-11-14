---
title: 自制电子在室表
summary: 一个利用最新技术对现有产品进行升级的尝试
tags:
  - 电子在室表
  - AI
date: '2023-11-09T00:00:00Z'


# Optional external URL for project (replaces project detail page).
# external_link: ''
# related_posts:
#  - 'https://weils302.com/zh/techblog/status_list_1_20230407/'
  
#image:
#  caption: Photo by rawpixel on Unsplash
#  focal_point: Smart

# links:
#  - icon: twitter
#    icon_pack: fab
#    name: Follow
#    url: https://twitter.com/georgecushen
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: ''
---

# 概要
---

<div style="text-align: justify;">
此项目中制作的产品为利用最新的AI技术对传统的纸质在室表进行升级的试验产品。该产品主要由显示屏、树莓派、控制端设备以及显示屏支架组成。
主要原理为通过控制端程序向树莓派发送图像内容并在显示屏中显示。AI技术在此项目中的应用主要在图像的生成（Midjourney）以及代码编写的辅助（ChatGPT）部分。
</div>


# 项目背景与目标
---

<div style="text-align: justify;">
传统的纸质在室表能够表示的状态有限，其内容的可扩展性也较差。比如某个房间有新的成员加入，或者某成员有更多的状态需要表示时，需要重新进行表格的设计
以及制作。每个在室表所能呈现的内容多少也被该表格的纸张大小所限制。此外如果成员在不回到房间的情况下状态发生了改变（比如从校外直接回家），那么房间
门上的纸质在室表状态并不能实时更新。此时一个电子版的、可以联网更改状态的在室表则能解决以上所有问题。
</div>

![纸质版到电子版](upgrade.jpg)

# 产品特点
---
<div style="text-align: justify;">

・可定制：由于不再受限于纸质媒介，成员可自由定制想显示的状态以及表示该状态的图像内容，且理论上没有数量上限。

・可远程操控：因为不需要直接操控显示屏的控制单元（树莓派），成员可在外直接修改状态。

・内容呈现更加形象：比起冷冰冰的文字和方格子上的磁铁，能代表成员的卡通形象以及该形象所呈现的状态能更加直观形象地表示成员状态。

</div>

<p style="font-size: 16px; line-height: 1.6;"><i>(以上功能中有一部分在现阶段还未能完美实现)</i></p>

# 技术原理
---

![技术原理](tech_flow.jpg)
<div style="text-align: justify;">
首先由Midjourney根据成员需求进行状态图像的生成并储存在客户端设备上，然后客户端程序通过成员选择的状态将对应的状态及其对应图像发送至服务器端设备
（树莓派）。这样服务器端设备连接的显示屏上就会显示成员选择的状态。其中ChatGPT在客户端和服务器端程序的编写上提供了辅助。
</div>

# 相关博文
---

[基于AI应用的电子在室表制作（一）](https://weils302.com/zh/techblog/status_list_1_20230407/)  
[基于AI应用的电子在室表制作（二）](https://weils302.com/zh/techblog/status_list_2_20230415/)  
[基于AI应用的电子在室表制作（三）](https://weils302.com/zh/techblog/status_list_3_20230418/)

# 更新日志
---
[电子在室表更新日志](https://weils302.com/zh/techblog/status_list_update/) 
