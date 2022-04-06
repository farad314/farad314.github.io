# 法拉(Farad)的小说站架构源码

[![Jekyll-theme-cayman](https://img.shields.io/badge/Jekyll_theme-cayman-%23159957?style=flat)](https://pages-themes.github.io/cayman/)

## 写在前面

### ~~注意！此分支的LICENCE文件仅对此分支有效 NOTE: The LICENCE file for this branch is only valid for this branch~~

~~出于著作权保护的原因，`Main`分支不包含LECENCE文件，保留完整著作权。这个分支是在`Main`分支基础上分离所有内容创建的开源框架，如果看到未删除的非源码内容，请不要使用，它们大部分都不基于`MIT`协议，使用即侵权。~~

~~遇到此事最好的解决方案是在此分支的Issues区创建一个新Issue，向我告知未删除内容。可以接受中文或英文。~~

~~此分支使用`MIT`协议开源，但此分支的LICENCE文件仅对此分支有效。~~

~~For copyright protection reasons, the `Main` branch does not contain the LECENCE files and retains full copyright. This branch is an open source framework created by separating all contents based on Main branch, if you see non-source contents that are not removed, please do not use them, most of them are not based on MIT protocol, use is infringement.~~

~~The best solution is to create a new Issue in the Issues section of this branch, informing me of the undeleted content. Chinese or English is acceptable.~~

~~This branch is open source using the `MIT` licence, but the LICENCE file for this branch is only valid for this branch.~~

-----

在确认`MIT`协议细节之前，此分支暂不开源，与`Main`分支一致，保留所有著作权。

This branch is not open source until the details of the `MIT` licence are confirmed, all copyrights are reserved for now.

## TODO表 Todos

### 此页相关 Todos about this page

- [x] 此页内容改成表格
- [x] 收录所有信息&nbsp;&nbsp;&nbsp;*待确认*
- [ ] 将此页翻译为英文 Translate this page into English

### 开发相关

- [ ] 功能
  - [ ] 推荐
  - [ ] 自动目录
  - [ ] 佳作推荐
  - [ ] 随机翻阅
  - [ ] 导航栏
  - [ ] 无障碍
    - [ ] 屏幕阅读器适配
  - [ ] 显示写作时间
- [x] 重构
  - [x] 变量名&nbsp;&nbsp;&nbsp;*待确认*
  - [x] 文件名
  - [x] 注释
- [ ] 将网站翻译为英文 Translate this site into English

### 内容相关

- [x] 页面
  - [x] 关于法拉
  - [x] 关于本站
  - [x] 文章
    - [x] 灵感/棱镜
    - [x] 灵感/蜂巢
    - [x] 灵感/胶卷
    - [x] 未完成/上帝已死

## 已完成功能

- 暗色适配
- 浏览器兼容提示
- 部分样式较原模版优化
- 著作权提示

## 元信息列表

命名方式：连字符，简称全大写

### Site元信息

|变量名|变量用途|使用范围|备注|
|:---|:---|:---|:---|
|title|网站标题|全站||
|description|网站简介|全站||
|theme|网站主题|全站||

### Page元信息

#### 页面信息

##### 内建

|变量名|变量用途|使用范围|备注|
|:---|:---|:---|:---|
|layout|版式类型|所有页面|只可填入_includes中的版式，不需要扩展名|
|title|页面标题|所有页面||
|description|页面描述|所有页面||

##### 自定义

|变量名|变量用途|使用范围|备注|
|:---|:---|:---|:---|
|no-like|禁用推荐|novel版式页面|仅布尔值|
|footer|页脚信息|novel/function版式页面||
|time|写作时间|novel版式页面|格式 YY/MM/DD HH:MM|

#### 版权类

|变量名|变量用途|使用范围|备注|
|:---|:---|:---|:---|
|cc-type|版权类型|CCTemple|可用值见下|
|cc-name|版权声明名称|CCTemple||
|cc-link|版权声明链接|CCTemple||
|no-cc|隐藏声明|CCTemple|仅布尔值|

cc-type可用值列表：["by","by-sa","by-nd","by-nc","by-nc-sa","by-nc-nd","cr"]，cr代表CopyRight,其他皆为CC协议名

## 模板列表与功能简介

命名方式：小驼峰，简称全大写
|模板名|模板用途|使用范围|备注|
|:---|:---|:---|:---|
|CCTemple:|生成著作权声明或CC授权声明|各种页面的页尾||
|defaultFooter|默认底栏|页面底部||
|defaultHead|默认头信息|页面头||
|defaultHeader|默认顶栏|页面顶部||
|head-custom|自定义头信息|defaultHead|将被合并至defaultHead中|
|likeDisabled|推荐禁用提示|页尾||
|Liketemple|展示推荐功能|页尾|未完成|
|profiles/(name)|特殊页面的独立配置|MD文件末尾|应[MD033](https://github.com/DavidAnson/markdownlint/blob/v0.25.1/doc/Rules.md#md033)要求，将应用于特殊页面的HTML做成模板|

## 版式列表与功能简介

命名方式：小驼峰，简称全大写
|版式名|版式用途|使用范围|备注|
|:---|:---|:---|:---|
|default|默认排版|无||
|functional|功能性页面使用的模板|主页，关于|目前与default一致|
|novel|小说页模板，自动正文首行缩进，带推荐功能|小说页||
