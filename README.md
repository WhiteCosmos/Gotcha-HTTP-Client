# Gotcha HTTP Client - MacOS独占的HTTP接口测试工具

Gotcha HTTP Client是一个用于发送HTTP请求和查看返回信息的测试工具，UI设计简约，交互方便易于上手。使用过程中无需联网，所有数据均存放在本地。

Gotcha HTTP Client并非开源软件，本仓库用于BUG跟踪和问题反馈。

## 目录

- [最新版本](#最新版本)
- [下载地址](#下载地址)
- [收费方式](#收费方式)
- [技术支持](#技术支持)
- [功能列表](#功能列表)
- [使用指南](#使用指南)

### 最新版本 1.4.3 (2022/03/27)

新功能

1. 新增全局变量功能，进入环境变量管理页面添加全局变量
2. 增加Postman Collection文件导入功能，包括以下部分
	- Header
	- Path参数
	- Query参数
	- Body(Raw, Form, Multipart)

BUG修复

1. 修复使用URL补全后，对URL的修改没有同步到对应参数的问题

### 下载地址

[Mac App Store](https://apps.apple.com/cn/app/gotcha-http-client/id1524200727)

### 收费方式

Gotcha HTTP Client是一个买断制应用，一次购买，终身更新。

- 提供**14天**免费试用
- **78元**购买永久版本

### 技术支持
 
- 微信交流群

![img](images/wechat_group.jpg)

- QQ交流群

![img](images/qq_group.jpg)

### 功能列表

> TODO

### 使用指南

#### 创建项目

> Gotcha启动后会生成一个默认项目"Playground"，你可以在该项目中测试各项功能。

![img](images/tutorial/#1_create_project.jpeg)

1. 点击打开项目创建和导入面板
2. 新建空白项目，你可以在项目中自由创建或导入HTTP请求
3. 导入OpenAPI/Swagger文件，查看接口文档，目前不可编辑
4. 通过URL方式导入OpenAPI/Swagger文件
5. 通过Java项目生成接口文档，支持Spring/JAX-RS框架，目前不可编辑

#### 接口与分组管理

> Gotcha中的分组和请求之间可以随意排列和嵌套

![img](images/tutorial/#2_request_and_group.jpeg)

1. 在根目录创建请求或分组，也可以导入Postman Collection文件
2. 使用右键菜单
	- 在请求上点击'New Request'或'New Group'，会创建在相邻位置
	- 在分组上点击'New Request'或'New Group'，如果分组为**展开状态**，则会作为子项目创建，如果分组为**收起状态**，则会在相邻位置创建。
	- 剪切与复制也遵循上述规则
3. 拖动改变接口与分组的排列方式或层级结构
	- 使用**Command**快捷键多选，**Shift**快捷键可以连选，支持批量拖动
	- 当分组为**收起状态**时，拖动位置会区分为**里侧**和**外侧**，里侧会放置对象到目标分组内部，外侧则放置在相邻位置
	
#### 编辑URL参数

> Gotcha通过参数化URL的模式可以让你直接编辑其中的每一部分

![img](images/tutorial/#3_url_parameters.jpeg)

1. HTTP请求方法选择，点击菜单中的'+'按钮可以编辑自定义请示方法
2. URL编辑栏，支持直接导入**cURL**，过去使用过的URL会出现自动提示
3. Path编辑器，支持编辑任意一段Path参数
4. Query参数编辑
5. 对于参数较长的情况，可以打开一个独立的编辑页面

#### 编辑Header和Cookie

> Gotcha中可以直观的看到当前会发送的Cookie信息

![img](images/tutorial/#3_url_parameters.jpeg)

1. Header的编辑和URL参数是一样，也会提示常用的Header
2. Cookie编辑器会显示当前域名下存在的Cookie，也可以手动添加


























