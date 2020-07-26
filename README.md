# 简单图片管理系统

~~非常的简单~~

## 功能罗列

- 用户的注册，登录，个人信息修改，登录密码修改
- 用户关注其他用户或取消关注其他用户
- 用户上传图片，浏览图片，管理自己的图片
- 搜索方面，用户可以搜索图片以及其他用户
- 用户也可以选择屏蔽其他用户，禁止其访问自己的空间，查看自己的图片
- 用户甚至可以选择举报其他用户，上交信息给管理员，由管理员亲自处理

### FrontEnd

铁打的React配合流水的Ant Design、React Router

#### 槽点

- 为什么languages占比最大的是css？
    >因为忘了import css，改用外联文件，Ant Design的说明文档网页内提取的css就那么大，欢迎PR
- 为什么js的模块文件分了相当于没分？
    >因为当时初学，将绝大部分功能点封装在一个按钮上，用户交互基本是Modal形式。
- 顺便在项目交付前尝试了一次将网络请求抽离，以callback的形式处理结果
    >因为该功能点涉及访问权限，仅需一个网络请求结果，反馈用户一个短提醒
    >后续回想：应该使用Promise来处理的

### BackEnd

常规的MVC：SpringMVC+Spring+SpringData

常规的数据库：MySQL

常规的接口说明：Swagger2

#### 槽点

- 整个C层竟然写在一个文件里
    >因为每个后端数据接口路径等取名粗糙，接口数量少就顺势杂糅在一起了
- 看看description/About，找到点后欢迎PR