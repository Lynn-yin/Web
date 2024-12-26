# 仿站电商平台项目

## 项目简介

这是一个基于Express + Node.js开发的电商平台项目，采用前后端分离架构。
项目模拟了真实电商网站的主要功能，包括用户注册登录、商品浏览、个人中心等模块。用于学习和练习Web开发。

## 技术栈说明

### 前端技术
- HTML5：页面结构
- CSS3：页面样式
- JavaScript：页面交互
- Axios：HTTP请求库，用于前后端通信
- Swiper：轮播图组件，实现首页轮播效果

### 后端技术  
- Node.js：JavaScript运行环境
- Express：Web应用框架
- JSON：数据存储方案

## 详细功能说明

### 1. 首页功能 (index.html)
- **页面布局**
  - 顶部导航栏
  - 轮播图展示区域
  - 商品购买入口
- **用户状态显示**
  - 未登录状态显示"请登录"链接
  - 已登录显示用户昵称
  - 个人中心和退出登录按钮
- **轮播图功能**
  - 自动轮播（1秒切换一次）
  - 鼠标悬停暂停
  - 左右切换按钮
  - 底部分页指示器

### 2. 用户系统
#### 2.1 登录页面 (login.html)
- **页面布局**
  - 居中表单设计
  - 统一的输入框样式
- **功能特点**
  - 用户名和密码输入验证
  - 错误提示信息显示
  - 注册页面快捷链接
  - 登录成功自动跳转首页

#### 2.2 注册页面 (registe.html)
- **表单内容**
  - 用户名输入框
  - 密码输入框
  - 确认密码输入框
  - 昵称输入框
- **功能特点**
  - 表单完整性验证
  - 密码一致性检查
  - 登录页面快捷链接
  - 注册成功跳转登录页

#### 2.3 个人中心 (self.html)
- **信息展示与修改**
  - 用户名（只读）
  - 年龄设置
  - 性别选择
  - 昵称修改
- **页面功能**
  - 修改密码入口
  - 返回首页链接
  - 表单验证
  - 修改成功提示

#### 2.4 密码修改 (pwd.html)
- **表单设计**
  - 原密码输入
  - 新密码输入
  - 确认新密码
- **安全特性**
  - 密码格式验证
  - 新旧密码一致性检查
  - 修改成功后自动退出

### 3. 商品系统
#### 3.1 商品列表页 (list.html)
- **分页控制**
  - 首页/末页快速跳转
  - 上一页/下一页导航
  - 当前页/总页数显示
  - 页码跳转输入框
  - 每页显示数量选择（12/16/20/24条）
- **商品展示**
  - 网格布局（每行4个商品）
  - 商品图片
  - 商品标题
  - 价格信息
  - 点击商品跳转详情

#### 3.2 商品详情页 (goods.html)
- **商品信息**
  - 左侧大图展示
  - 右侧信息区域
    - 商品标题
    - 原价（带删除线）
    - 折扣信息（绿色显示）
    - 现价（红色显示）
- **页面导航**
  - 返回列表页链接
  - 商品详情描述

## 页面样式特点

### 1. 统一设计风格
- 顶部导航栏统一使用skyblue背景色
- 内容区域采用1200px居中布局
- 表单采用统一的粉色边框样式
- 按钮使用统一的样式和过渡效果

### 2. 响应式布局
- 首页轮播图自适应
- 商品列表网格布局
- 表单居中显示

### 3. 交互体验
- 表单验证即时反馈
- 操作成功/失败提示
- 页面间平滑跳转
- 按钮悬停效果

## 项目结构详解

```
project/
├── 本地server/              # 后端服务器代码
│   ├── src/                 # 源代码目录
│   │   ├── app.js          # 服务器入口文件
│   │   ├── conf/           # 配置文件目录
│   │   │   └── config.js   # 系统配置（端口、Token等）
│   │   ├── controller/     # 控制器：处理业务逻辑
│   │   ├── middleware/     # 中间件：处理请求、验证等
│   │   ├── model/         # 数据模型：数据处理
│   │   ├── routes/        # 路由：URL映射
│   │   ├── utils/         # 工具函数
│   │   └── views/         # 视图模板
│   └── 接口文档.md          # API接口说明文档
├── img/                    # 项目图片资源
│   ├── img1.jpg           # 轮播图等图片
│   └── ...
├── lib/                    # 第三方库文件
│   ├── axios.min.js       # Axios库
│   └── swiper/            # 轮播图组件
├── pages/                  # 页面JS文件
│   ├── axios.min.js       # Axios库
│   └── http.js            # 请求配置和封装
└── views/                  # 前端页面文件
    ├── index.html         # 首页
    ├── login.html         # 登录页
    ├── registe.html       # 注册页
    ├── list.html          # 商品列表页
    ├── goods.html         # 商品详情页
    ├── self.html          # 个人中心页
    └── pwd.html           # 修改密码页
```

## 运行指南

### 1. 环境准备
- 安装 Node.js
- 安装项目依赖：
  ```bash
  cd 本地server/src
  npm install
  ```

### 2. 启动服务器
- Windows系统：
  - 双击运行 "win点我启动.bat"

### 3. 访问项目
- 打开浏览器，访问：http://localhost:8888/views/index.html
- 默认端口：8888（可在配置文件中修改）

## 重要配置说明

### 1. 用户名密码规则
- 用户名要求：
  - 格式：/^[a-z0-9]\w{3,11}$/
  - 说明：4-12位字符，只能包含字母、数字和下划线，首字符必须是小写字母或数字

- 密码要求：
  - 格式：/\w{6,12}/
  - 说明：6-12位字符，只能包含字母、数字和下划线

### 2. 登录状态配置
- 配置文件位置：src/conf/config.js
- 默认保持时间：1小时

### 3. 数据存储说明
- 存储方式：JSON文件
- 存储位置：src/db/目录
- 数据文件：
  - users.json：用户数据
  - goods.json：商品数据
  - token.json：登录状态数据

## 开发注意事项

1. 所有需要登录后操作的接口都需要：
   - 在请求头中携带 authorization 字段
   - 传递有效的 token 值

2. 接口返回状态码说明：
   - 1：操作成功
   - 0：操作失败
   - 5：参数错误
   - 401：未登录或token失效

3. 本地开发时注意：
   - 保持服务器运行状态
   - 注意检查接口返回的错误信息
   - 查看浏览器控制台的报错信息

## 接口文档

详细的API接口说明请查看：本地server/接口文档.md