# 顺风车平台

一个现代化的顺风车平台应用,支持用户查看司机发布的路线,司机可以发布时间和路线信息。

## 功能特性

### 用户端
- 📋 浏览所有可用顺风车路线
- 🔍 搜索功能(按起点、终点搜索)
- 🔧 筛选功能(按时间、价格筛选)
- 📱 预约路线
- 💡 查看详细信息

### 司机端
- ➕ 发布顺风车路线
- 🎯 设置起点、终点、出发时间
- 💰 设置价格和座位数
- 📝 添加备注信息
- 🗑️ 管理已发布的路线

## 技术栈

- **前端框架**: React 18 + TypeScript
- **构建工具**: Vite 5
- **UI组件库**: TDesign React 1.12.0
- **样式**: Tailwind CSS 3.4.17
- **状态管理**: React Context API
- **数据存储**: LocalStorage

## 项目结构

```
顺风车/
├── public/                    # 静态资源
├── src/
│   ├── components/           # 可复用组件
│   │   ├── RideCard.tsx      # 路线卡片组件
│   │   ├── RideList.tsx      # 路线列表组件
│   │   ├── SearchBar.tsx     # 搜索栏组件
│   │   └── FilterPanel.tsx   # 筛选面板组件
│   ├── pages/                # 页面组件
│   │   ├── HomePage.tsx      # 首页
│   │   ├── PublishPage.tsx   # 发布页面
│   │   └── MyRidesPage.tsx   # 我的路线页面
│   ├── contexts/             # 上下文管理
│   │   └── RideContext.tsx   # 路线状态管理
│   ├── types.ts              # 类型定义
│   ├── App.tsx               # 主应用组件
│   ├── main.tsx              # 应用入口
│   └── index.css             # 全局样式
├── index.html                # HTML模板
├── package.json              # 项目依赖
├── tsconfig.json            # TypeScript配置
├── vite.config.ts           # Vite配置
├── tailwind.config.js       # Tailwind配置
└── postcss.config.js        # PostCSS配置
```

## 快速开始

### 安装依赖

```bash
npm install
```

### 启动开发服务器

```bash
npm run dev
```

访问 http://localhost:5173 查看应用

### 构建生产版本

```bash
npm run build
```

### 预览生产构建

```bash
npm run preview
```

## 使用说明

### 作为乘客
1. 打开应用首页
2. 使用搜索栏查找路线(输入出发地和目的地)
3. 使用筛选面板过滤结果(价格范围、日期)
4. 查看路线详情
5. 点击"立即预约"按钮

### 作为司机
1. 点击底部导航栏的"发布"按钮
2. 填写司机信息(姓名、电话)
3. 设置路线信息(出发地、目的地、出发时间)
4. 设置价格和座位数
5. 可选填写备注信息
6. 点击"发布路线"按钮

### 管理路线
1. 点击底部导航栏的"我的"按钮
2. 查看所有已发布的路线
3. 点击"删除"按钮删除不需要的路线

## 数据模型

### Ride (路线)
```typescript
interface Ride {
  id: string;                    // 路线ID
  driverName: string;            // 司机姓名
  phone: string;                 // 联系电话
  departure: string;             // 出发地
  destination: string;           // 目的地
  departureTime: string;         // 出发时间
  price: number;                 // 价格(元)
  seats: number;                 // 座位数
  availableSeats: number;        // 剩余座位
  note?: string;                 // 备注
  createdAt: string;             // 创建时间
}
```

## 特色功能

- 🎨 现代化UI设计,基于TDesign组件库
- 📱 完全响应式设计,支持移动端
- 💾 本地数据持久化,使用LocalStorage
- 🔄 实时搜索和筛选
- ✨ 流畅的用户体验
- 🚀 快速的开发和构建

## 注意事项

- 本项目使用LocalStorage存储数据,刷新页面后数据不会丢失
- 首次运行时会自动添加3条示例路线
- 所有价格单位为人民币元
- 时间格式为: YYYY-MM-DD HH:mm

## 许可证

MIT
