<p align="center">
  <img src="images/logo.png" width="120" height="120" />
</p>

# Gotcha HTTP Client - MacOS独占的HTTP接口测试工具

Gotcha HTTP Client是一个用于发送HTTP请求和查看返回信息的测试工具，UI设计简约，交互方便易于上手。使用过程中无需联网，所有数据均存放在本地。

Gotcha HTTP Client is a lightweight http client that allows you to make requests and inspect responses. It has pretty UI/UX design, and very easy to use. Gotcha is a standalone software and can be used without NETWORK.

Gotcha HTTP Client并非开源软件，本仓库用于BUG跟踪和问题反馈。

Gotcha HTTP Client is not open source, you can report any bugs or features here.

- [README_EN](README_EN.md)

**[Follow My Twitter For Latest News!!!](https://twitter.com/whitecosm0s)** 

![img](images/preview.png)

## 目录

- [最新版本](#最新版本)
- [下载地址](#下载地址)
- [收费方式](#收费方式)
- [技术支持](#技术支持)
- [功能列表](#功能列表)
- [使用指南](#使用指南)

### 最新版本 1.6.3 (2023/4/1)

【新功能】

- 在项目配置中新增全局模板功能，支持配置新建请求时的默认参数
- 专业版新增「请求模板」功能，可以保存某个请求为请求模板
- 新增繁体中文支持

【交互优化】

- 优化弹窗关闭效果，通过「esc」键可以关闭所有弹窗
- 优化功能分组，专业版功能单独分为一组(Schema管理/请求模板/批量导出)

【URL编辑】

- 修复新建请求并粘贴URL后，执行时URL自动变为httpbin.org的问题
- 修复在某些情况上直接编辑URL并发起请求，URL被自动修改的问题
- 修复Path参数存在动态变量时，修改URL后没有删除对应变量的问题
- 修复在Path中使用某些动态变量时，侧边栏中对应的请求路径未正确显示的问题
- 修复Query参数类型为数组时，无法正确导出的问题

【服务器管理】

- 在服务器选择中新增『服务管理』选项，直接打开服务器管理页面
- 修复服务绑定到环境后，未正确解析的问题
- 修复某些情况下选择服务器后，对应URL没有更新的问题

【JSON 编辑器】

- 增加复制按钮，可以一键复制整个Json
- 右键菜单增加复制Json和复制Json Path选项，可以独立复制某个JSON节点
- Json导入菜单新增『增量更新选项』

【接口文档】

- 支持通过Json直接生成并导入对应的Json Schema

【Json Schema管理】

- 修复某些情况下，展开和收起Schema无响应的问题
- 创建Json Schema后，支持通过导入Json生成对应的字段

【cURL导出】

- cURL导出支持"Binary"和"GraphQL"的请求类型

【Cookie管理】

- Cookie值允许使用动态变量
- Cookie管理面板中，支持拖动排序域名，或者改变域名所属的Cookie Jar
- 优化Cookie展示，通过hover菜单展示不常用的属性
- 修复向Cookie Jar中添加域名时，未正确添加的问题
- 修复删除Cookie Jar后，对应请求中的Cookie没有同步更新的问题

【环境变量管理】

- 修复环境变量右键菜单有时无法正常显示的问题
 
【Postman导出】

- 支持导出和导入Postman的Example(当前仅支持text模式)
- 修复某些情况下导出Postman时，item为空的问题

【其它】

- 修复选择Binary格式上传文件时，未正确读取文件的问题
- 优化切换项目后，一些数据没有同步更新到新项目的问题
- 点击『专业版』标签后，会显示当前专业版的所有功能

### 下载地址

[Mac App Store](https://apps.apple.com/cn/app/gotcha-http-client/id1524200727)

### 收费方式

Gotcha Rest Client 基础功能免费使用，高级功能需要购买专业版

- 专业版提供**28天**免费试用
- **98元**购买永久版本

### 技术支持

遇到问题请提交ISSUE，或加入以下群聊与我沟通。
 
- 技术支持邮箱 

**support@gotcha.rest**

- QQ交流群

![img](images/qq_group.jpg)

### 功能列表

以下为Gotcha HTTP Client支持的功能清单，未完成的功能会标注为**开发中**

 1. Url编辑
 
 - 支持复制curl到Url编辑栏，直接导入curl
 - 支持编辑Path和Query参数
 - 支持添加自定义HTTP请求方法
 
 2. 支持的请求体类型
 
 - Text 模式，支持多种语法高亮
 - JSON 模式，支持通过剪切板和文件导入JSON
 - Form 表单上传(form-urlencoded)
 - Multipart 文件上传
 - Binary格式**(开发中)**
 - GraphQL 请求

 3. Header 和 Cookie
 
 - 支持常用Header类型自动提示
 - 支持添加和删除自定义Cookie
 - 支持自动接收和发送Cookie
 - 多CookieJar切换和管理
 
 4. 接口认证
 
 - 支持 HTTP Basic Auth
 - OAuth 2.0 **(开发中)**
 - Digest Auth **(开发中)**
 
 5. 导入和导出
 
 - 支持导入Postman Collection文件
 - 支持通过文件或URL导入Swagger/OpenAPI文件，替代SwaggerUI
 - 支持通过Java项目直接生成API文档，支持Spring/SpringFox/JAX-RS框架
 - 支持导出单个请求到curl
 - 支持填写参数注释，并导出请求为Markdown格式的接口文档
 
 6. 环境变量
 
 - 支持环境变量和环境变量分组
 - 支持全局变量
 
 7. 为请求参数添加注释
 
 - 支持为请求参数添加注释
 - 支持保存返回响应作为文档示例
 - 支持导出Markdown格式的接口文档
 
 8. 返回响应断言和校验
 
 - 支持对响应Headers设置断言
 - 支持对Json格式的响应体设置断言
 
### 使用指南

#### 创建项目

> Gotcha启动后会生成一个默认项目"Playground"，你可以在该项目中测试各项功能。

![img](images/tutorial/create_project.png)

1. 点击打开项目创建和导入面板
2. 新建空白项目，你可以在项目中自由创建或导入HTTP请求
3. 导入OpenAPI/Swagger文件，查看接口文档，目前不可编辑
4. 通过URL方式导入OpenAPI/Swagger文件
5. 通过Java项目生成接口文档，支持Spring/JAX-RS框架，目前不可编辑

#### 接口与分组管理

> Gotcha中的分组和请求之间可以随意排列和嵌套

![img](images/tutorial/request_and_group_manager.png)

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

![img](images/tutorial/url_parameters_editor.png)

1. HTTP请求方法选择，点击菜单中的'+'按钮可以编辑自定义请求方法
2. URL编辑栏，支持直接导入**cURL**，过去使用过的URL会出现自动提示
3. Path编辑器，支持编辑任意一段Path参数
4. Query参数编辑
5. 对于参数较长的情况，可以打开一个独立的编辑页面

#### 编辑Header和Cookie

> Gotcha中可以直观的看到当前会发送的Cookie信息

![img](images/tutorial/headers_and_cookies_editor.png)

1. Header的编辑和URL参数是一样，也会提示常用的Header
2. Cookie编辑器会显示当前域名下存在的Cookie，也可以手动添加
3. 通过右上角的Cookie Jar管理页面，可以添加多个Cookie Jar，用于模拟多用户的情况

#### 编辑Body请求体

> Gotcha支持几种常见的Body类型，并提供了一个独立的JSON编辑器

PS: 切换Body类型后，对应的Content-Type也会自动修改。

##### Text

![img](images/tutorial/text_request_body.png)

1. 右下角可以选择文本模式，同时Content-Type也会对应变化，如果要改为其它类型，需要到Header页面手动修改

##### Json

使用Json编辑器的优势

- 无需处理格式和符号问题，例如忘记删除逗号
- 支持选择性发送某些值
- 支持拖动改变节点排列顺序和层级结构，交互模式与**接口管理**一致

![img](images/tutorial/json_request_body.png)

1. 全部展开或全部收起节点
2. 预览JSON文本(只读模式)
3. 通过剪切板或文件导入Json
4. 选择节点类型 

##### Form

![img](images/tutorial/form_request_body.png)

##### Multipart

![img](images/tutorial/multipart_request_body.png)

1. 支持选择文本类型或文件类型

##### GraphQL类型

![img](images/tutorial/graphql_request_body.png)

#### 参数注释

> Gotcha支持保存响应数据并作为示例导出

```
注意事项:

在Headers、Url Params、Body中填写的参数，会自动出现在Docs页面中，暂时无法直接修改
```

##### Header和Query参数

![img](images/tutorial/doc_header_params.png)

1. 参数名称
2. 是否必需填写
3. 参数注释

##### Path参数

![img](images/tutorial/doc_path_params.png)

1. 勾选Param选项后，可以指定某一段Path为参数，并且Index变为**可以编辑**的状态，填写参数名称
2. 指定Path参数后，上方的Path也会变为{{name}}的形式

##### 请求数据示例

![img](images/tutorial/doc_payload.png)

1. Text和Json会导出为请求示例
2. Form和Multipart类型可以填写注释
3. 在返回响应中保存为响应示例

##### 导出为Markdown格式的接口文档

![img](images/tutorial/doc_copy_as_markdown.png)

1. 点击'Copy as Markdown'即可

#### 使用环境变量与全局变量

> Gotcha通过表单的方式统一管理所有环境中的所有变量

![img](images/tutorial/environment_variables_manager.png)

1. 点击打开菜单，创建变量和新环境
2. 双击修改环境名称，拖动改变环境顺序，右键菜单删除环境
3. 在参数值中使用{{变量名}}即可引用环境变量

#### 使用Cookie Jar

> TODO

#### HTTP请求选项设置

> TODO 

#### 为返回响应设置断言

> TODO

#### 访问历史请求记录

> TODO






















