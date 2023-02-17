---
title: 技术文档
---

<img src="https://i.328888.xyz/2023/02/17/pNm1z.png" width="784" height="727" style="width: 784px; height: 727px;" />

## 管理中心

### 文件目录：

```
admin-webmin-web
├── Dockerfile
├── README.md
├── build
├── config
├── jest.config.js
├── jsconfig.json
├── mock
├── package-lock.json
├── package.json
├── public
├── src
│   ├── access.ts
│   ├── app.tsx
│   ├── components
│   ├── constant.ts
│   ├── constants
│   ├── e2e
│   │   └── baseLayout.e2e.js
│   ├── global.less
│   ├── global.tsx
│   ├── locales
│   ├── manifest.json
│   ├── models
│   ├── pages
│   │   ├── 404.tsx
│   │   ├── AdminCenter
│   │   ├── ChannelConfig
│   │   ├── DefendNotice
│   │   ├── GameCenter
│   │   ├── Home
│   │   ├── PayMethodManagement
│   │   ├── PaySupplierMamt
│   │   ├── PublishBusinessMamt
│   │   ├── PublishPlatformMamt
│   │   ├── Runner
│   │   ├── components
│   │   ├── document.ejs
│   │   └── typings.d.ts
│   ├── service-worker.js
│   ├── services
│   ├── typings.d.ts
│   └── utils
├── tests
├── tsconfig.json
└── yarn.lock
```

#### 根目录

```
tsconfig.json、package.json包含 ts配置以及 ”top-menu“ antd design umi ... 等第三方依赖库
```

#### src

```
工程核心。包含业务、请求、工具等
```

##### pages

:::info{title=模块对应前端组件}

- 配置管理
  - 游戏管理 &emsp; ./AdminCenter/GameManage
  - 签名管理 &emsp; ./AdminCenter/SignNameManage
- 环境配置
  - 服务组管理 &emsp; ./AdminCenter/SDKServiceManage
  - 区服组管理 &emsp; ./GameCenter/ZoneManage
  - 通道管理 &emsp; ./GameCenter/TunnelManage
  - 通道包管理 &emsp; ./GameCenter/TunnelAppMakerManage
- 发行配置
  - 发行商管理 &emsp; ./PublishBusinessMamt
  - 渠道商管理 &emsp; ./ChannelConfig
  - 发行平台管理 &emsp; ./PublishPlatformMamt
  - 支付方式管理 &emsp; ./PayMethodManagement
  - 支付供应商管理 &emsp; ./PaySupplierMamt
- 日志查询
  - 游戏订单查询 &emsp; ./GameCenter/GameOrder
  - 登陆日志查询 &emsp; ./GameCenter/LoginLog
  - 补单查询 &emsp; ./GameCenter/HelpOrder
- Runner 管理
  - Runner &emsp; ./Runner/RunnerList
  - 作业 &emsp; ./Runner/HomeWork
    :::

##### models

```
状态管理
```

#### components

```
全局共用组件
```

#### services

```
全局请求模块
```

#### dist

```
构建后输出的产物
```

#### public

```
包含模版、logo、icon 等静态资源
```

### 项目启动方式

```bash
# 安装依赖
$ yarn install

# 本地开发
$ yarn start

# 打包
$ yarn run build

```

### 打包&部署

---

## 游戏开发平台

### 文件目录：

```
developer-webmin-web
├── Dockerfile
├── README.md
├── build
├── config
├── jest.config.js
├── jsconfig.json
├── package.json
├── public
├── src
│   ├── access.ts
│   ├── app.tsx
│   ├── components
│   ├── e2e
│   │   └── baseLayout.e2e.js
│   ├── global.less
│   ├── global.tsx
│   ├── locales
│   ├── manifest.json
│   ├── models
│   ├── pages
│   │   ├── 404.tsx
│   │   ├── Admin.tsx
│   │   ├── Debugging
│   │   ├── DingTalkCards
│   │   ├── Home
│   │   ├── VersionGive
│   │   ├── VersionPush
│   │   ├── Welcome.less
│   │   ├── Welcome.tsx
│   │   └── document.ejs
│   ├── service-worker.js
│   ├── services
│   ├── typings.d.ts
│   └── utils
├── tests
├── tsconfig.json
└── yarn.lock
```

#### 根目录

```
config、tsconfig.json、package.json包含 ts配置以及 ”top-menu“ antd design umi ... 等第三方依赖库
```

#### src

```
工程核心。包含业务、请求、工具等
```

##### pages

:::info{title=模块对应前端组件}

- 平台接入
  - SDK 接入 &emsp; ./Debugging/SDKInsert
  - SDK 埋点检测 &emsp; ./Debugging/Point
  - G 数接入 &emsp; ./Debugging/GInsert
  - G 数埋点检测 &emsp; ./Debugging/Point
  - 日志查询 &emsp; ./Debugging/LogQuery
  -
- 版本交付
  - 版本交付管理 &emsp; ./VersionGive/VersionGiveConfig
  - 钉钉卡片 &emsp; ./DingTalkCards/VersionInfo
    :::

#### services

```
全局请求模块
```

#### dist

```
构建后输出的产物
```

#### public

```
logo、icon 等静态资源
```

### 打包&部署

```bash
# 安装依赖
$ yarn install

# 本地开发
$ yarn start

# 打包
$ yarn run build

```

---

## 发行平台

### 文件目录：

```
pubsdk-webmin-web
├── Dockerfile
├── README.md
├── build
├── config
├── jest.config.js
├── jsconfig.json
├── mock
├── models
├── package-lock.json
├── package.json
├── public
├── src
│   ├── access.ts
│   ├── app.tsx
│   ├── components
│   ├── constants
│   ├── e2e
│   │   └── baseLayout.e2e.js
│   ├── global.less
│   ├── global.tsx
│   ├── locales
│   ├── manifest.json
│   ├── models
│   ├── pages
│   │   ├── 404.tsx
│   │   ├── Admin.tsx
│   │   ├── BusConnect
│   │   ├── OperationCenter
│   │   ├── ReleaseCenter
│   │   │   └── utils
│   │   └── document.ejs
│   ├── service-worker.js
│   ├── services
│   ├── typings.d.ts
│   └── utils
├── tests
├── tsconfig.json
└── yarn.lock
```

#### 根目录

```
config、tsconfig.json、package.json包含 ts配置以及 ”top-menu“ antd design umi ... 等第三方依赖库
```

##### pages

:::info{title=模块对应前端组件}

- 发行中心
  - 子游戏管理 &emsp; ./ReleaseCenter/GameConfig
  - 游戏母包管理 &emsp; ./ReleaseCenter/GamePackage
  - 渠道包模版 &emsp; ./ReleaseCenter/ChannelPackManage
  - 投放包管理 &emsp; ./ReleaseCenter/LaunchPackManage
- 运营中心
  - 账号服务管理
    - 注册登陆管理&emsp; ./OperationCenter/AccountService/RegAndLoginManagement
    - 协议管理&emsp; ./OperationCenter/AccountService/RegAndLoginManagement
  - 支付服务管理
    - 订单查询&emsp; ./OperationCenter/PayMamtService/OrderManagement
    - 补单日志&emsp;./OperationCenter/PayMamtService/SupplementLog
    - 支付套件管理&emsp; ./OperationCenter/PayMamtService/PayKITConfig
    - 支付套件切换&emsp; ./OperationCenter/PayMamtService/PayConfig
  - 悬浮球管理
    - 悬浮球管理&emsp;./OperationCenter/AccountService/RegAndLoginManagement
  - 商品管理
    - 游戏商品库&emsp;./OperationCenter/Goods/GameGoodsLibrary
    - 渠道商品配置&emsp;./OperationCenter/Goods/ChannelGoodsConfig
  - 防沉迷管理
    - 防沉迷管理&emsp;./OperationCenter/AccountService/RegAndLoginManagement
    - 节假日管理&emsp;./OperationCenter/PreventAddiction/HolidayManage
  - 实名认证管理
    - 公司管理&emsp;./OperationCenter/RealName/CompanyMamt
    - 认证项目管理&emsp;./OperationCenter/RealName/AuthenticationProjectMamt
    - 实名认证查询&emsp;./OperationCenter/RealName/AuthenticationUser
    - 认证流水查询&emsp;./OperationCenter/RealName/CertificationFlow
  - 查询工具
    - 账号查询&emsp;./OperationCenter/OperationTools/AccountQuery
    - 角色查询&emsp;./OperationCenter/OperationTools/RoleQuery
  - 全局配置
    - 项目管理&emsp;'./ReleaseCenter/ProjectManage
    - 支付商户管理管理&emsp;/OperationCenter/GlobalConfig/MerchantManagement
    - iOS 证书管理&emsp;./OperationCenter/GlobalConfig/IOSCertManagement
  - 商务对接 - 外部商务登记&emsp;/BusConnect/BusSign - 体验账号管理&emsp;/BusConnect/TYAccountManage' - 内部商务管理&emsp;./BusConnect/InBusManage - 二维码下载&emsp;/BusConnect/QRCode
    :::

#### src

```
工程核心。包含业务、请求、工具等
```

#### dist

```
构建后输出的产物
```

#### public

```
logo、icon 等静态资源
```

### 打包&部署

> 修改以下内容，然后提交代码即可自动编译

1. 将 build 文件夹下所有的`xnodeng-web-archtype`替换为你的项目名
2. 将根目录下的`.gitlab-ci.yml.temp` 改为 `.gitlab-ci.yml`，并修改`APP_DEPLOY_GROUP`的值
   > 如果需要修改编译节点，可将`xnodeng-nodejs-1`改为`xnodeng-nodejs-2`
3. 将根目录下`Dockerfile`文件里所有的`xnodeng-web-archtype`替换为你的项目名
