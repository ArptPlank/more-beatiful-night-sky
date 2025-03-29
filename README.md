# GitHub风格个人博客

一个基于 Vue 3、Vite 和 Tailwind CSS 构建的现代化个人博客平台，采用 GitHub 风格设计。提供博客发布、项目展示、个人简历和待办事项管理等功能。支持亮色和暗色模式，响应式设计适配各种设备。

![GitHub风格博客预览](./public/preview.png)

## ✨ 功能特性

- 🌙 **亮色/暗色主题**：支持自动和手动切换主题模式
- 📝 **Markdown 博客**：支持 Markdown 格式博客的上传、展示和编辑
- 🌟 **项目展示**：可以从 GitHub 自动导入项目，或手动添加项目
- 📊 **个人简历**：展示个人技能、工作经历和教育背景
- ✅ **待办事项**：简单的任务管理系统，帮助跟踪待办事项
- 🔍 **分类与标签**：通过分类和标签组织和筛选内容
- 🔄 **本地存储**：使用浏览器本地存储保存数据
- 💻 **响应式设计**：完美适配桌面、平板和移动设备

## 🛠️ 技术栈

- **前端框架**：Vue 3 (组合式 API)
- **状态管理**：Pinia
- **路由管理**：Vue Router
- **构建工具**：Vite
- **CSS 框架**：Tailwind CSS
- **UI 组件**：Headless UI
- **图标库**：Heroicons
- **Markdown 渲染**：markdown-it + highlight.js
- **HTTP 请求**：Axios

## 📦 安装与使用

### 环境要求

- Node.js >= 16.20.2
- npm >= 10.9.0

### 安装依赖

```bash
npm install
```

### 开发模式

```bash
npm run dev
```

应用将在 http://localhost:5173 启动开发服务器。

### 构建生产版本

```bash
npm run build
```

### 预览生产构建

```bash
npm run preview
```

## 🚀 部署

### Webify 部署

1. 在 Webify 创建一个新项目
2. 选择 Vue.js 框架
3. 连接您的 Git 仓库或上传构建文件
4. 配置构建命令：`npm run build`
5. 设置输出目录：`dist`
6. 点击部署

### 数据持久化

项目目前使用浏览器本地存储进行数据管理。如需将数据迁移到后端数据库，可以：

- 集成 Firebase Firestore
- 搭建 MongoDB + Express 后端
- 使用其他云数据库服务

## 📄 项目结构

```
my_blog/
├── public/          # 静态资源
├── src/
│   ├── assets/      # 项目资源文件
│   ├── components/  # Vue 组件
│   ├── router/      # 路由配置
│   ├── stores/      # Pinia 状态管理
│   ├── utils/       # 工具函数
│   ├── views/       # 页面视图
│   ├── App.vue      # 根组件
│   └── main.js      # 应用入口
├── .gitignore       # Git 忽略配置
├── index.html       # HTML 入口
├── package.json     # 项目依赖
├── vite.config.js   # Vite 配置
└── README.md        # 项目说明
```

## 🔧 自定义配置

### 主题设置

主题颜色可以在 `src/App.vue` 中的 CSS 变量部分修改：

```css
:root {
  --color-bg-primary: #ffffff;
  --color-bg-secondary: #f6f8fa;
  /* 其他主题变量... */
}
```

### GitHub 集成

要启用 GitHub 项目导入，您需要在 `ProjectsView.vue` 中配置您的 GitHub 用户名：

```javascript
// 修改为您的 GitHub 用户名
const githubUsername = ref('your-github-username')
```

## 📝 许可证

[MIT](LICENSE)

## 🙏 贡献

欢迎提交 Issues 和 Pull Requests 贡献代码！
