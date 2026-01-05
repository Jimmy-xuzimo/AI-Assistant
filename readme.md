# AI 助手界面

一个现代化、响应式的AI助手网页界面，支持深色/浅色主题切换，流畅的动画效果，以及完整的聊天功能。
<img width="4400" height="2722" alt="image" src="https://github.com/user-attachments/assets/195c5562-6844-4e5c-9056-0a908f8d63d6" />
<img width="4400" height="2722" alt="image" src="https://github.com/user-attachments/assets/e2b414fb-acfe-4b11-8efc-eac3b4b929a5" />

## ✨ 功能特性

### 🎨 设计与UI
- **现代化设计**：采用渐变背景、玻璃态设计和流畅的动画效果
- **主题切换**：支持深色/浅色主题无缝切换，带有平滑过渡动画
- **响应式布局**：适配桌面、平板和移动设备
- **流畅动画**：优化的CSS动画，确保60fps流畅运行
- **硬件加速**：使用CSS硬件加速技术提升动画性能

### 💬 聊天功能
- **实时聊天**：支持与AI模型进行实时对话
- **历史记录**：自动保存聊天记录，支持查看和管理
- **多模型切换**：支持切换不同AI模型（Chat/Reasoner）
- **Markdown支持**：支持Markdown格式的消息展示
- **代码高亮**：支持代码块语法高亮

### 📱 用户体验
- **直观的主题切换**：太阳/月亮图标清晰指示当前主题
- **平滑的过渡效果**：所有交互都带有流畅的过渡动画
- **优化的内容显示**：最大化内容显示区域，减少滚动需求
- **移动端适配**：针对移动设备优化的触控体验

## 🛠️ 技术栈

- **HTML5**：语义化的HTML结构
- **CSS3**：现代CSS特性，包括渐变、动画、变量等
- **JavaScript (ES6+)**：原生JavaScript，无框架依赖
- **Marked.js**：Markdown解析库
- **Font Awesome**：图标库（间接使用）

## 🚀 快速开始

### 本地运行

1. **克隆或下载项目**
   ```bash
   git clone <repository-url>
   cd ai-assistant-interface
   ```

2. **添加API密钥**
   - 打开 `index.html` 文件
   - 找到以下代码行：
     ```javascript
     // 配置 - 请在此处添加您的API密钥
     const API_KEY = 'YOUR_API_KEY_HERE'; // 替换为您的DeepSeek API密钥
     const API_URL = 'https://api.deepseek.com/chat/completions';
     ```
   - 将 `YOUR_API_KEY_HERE` 替换为您的DeepSeek API密钥

3. **启动本地服务器**
   ```bash
   # 使用Python 3
   python -m http.server 8000
   
   # 或使用Node.js
   npx http-server -p 8000
   
   # 或使用PHP
   php -S localhost:8000
   ```

4. **访问应用**
   打开浏览器，访问 `http://localhost:8000`

### 直接部署

1. **使用无密钥版本**：项目提供了 `index(无秘钥).html` 文件，已移除所有真实API密钥，可直接用于部署
2. **添加API密钥**：在部署前，按照上述步骤添加您的API密钥
3. **上传文件**：将文件上传到任意静态文件服务器
4. **访问应用**：通过浏览器访问服务器上的HTML文件

### API密钥获取

您可以从 [DeepSeek 官网](https://www.deepseek.com/) 获取API密钥。注册并登录后，在控制台中创建API密钥。

### API密钥安全

- **不要提交到版本控制**：确保API密钥不会被提交到GitHub等版本控制系统
- **使用环境变量**：在生产环境中，建议使用环境变量管理API密钥
- **限制密钥权限**：根据需要为API密钥设置适当的权限
- **定期轮换**：定期更换API密钥以增强安全性

## 📖 使用说明

### 基本聊天
1. 在输入框中输入您的问题
2. 点击发送按钮或按 Enter 键发送消息
3. 等待AI回复

### 主题切换
- 点击右上角的太阳/月亮图标切换主题
- 浅色模式：太阳图标
- 深色模式：月亮图标

### 模型切换
- 点击顶部的 "Chat" 或 "Reasoner" 按钮切换AI模型
- 不同模型具有不同的功能特点

### 历史记录管理
- 点击左侧边栏的历史记录项查看历史对话
- 点击历史记录项右侧的 "×" 按钮删除该记录
- 点击 "新的对话" 按钮开始新的聊天

### 侧边栏操作
- 点击左上角的菜单图标打开/关闭侧边栏
- 在移动端，点击背景遮罩也可关闭侧边栏

## 📁 项目结构

```
ai-assistant-interface/
├── index.html          # 主页面文件
├── readme.md           # 项目说明文档
└── (可选) assets/      # 静态资源目录
    └── images/         # 图片资源
```

## ⚙️ 自定义配置

### 修改AI模型配置

在 `index.html` 文件中，找到以下配置项进行修改：

```javascript
// 配置
const API_KEY = 'YOUR_API_KEY_HERE';
const API_URL = 'https://api.deepseek.com/chat/completions';
```

### 修改主题颜色

在 `index.html` 文件中，修改CSS变量来自定义主题颜色：

```css
:root {
    /* 浅色模式 */
    --bg-light: linear-gradient(135deg, #F3F0F8 0%, #E3E6FF 50%, #FDFBFD 100%);
    --accent-light: #8A6FE6;
    /* 深色模式 */
    --bg-dark: linear-gradient(135deg, #1A1A2E 0%, #16213E 50%, #0F0F1A 100%);
    --accent-dark: #A78BFA;
    /* ... 更多变量 */
}
```

### 修改动画效果

在 `index.html` 文件中，修改CSS动画相关属性：

```css
/* 调整动画过渡时间 */
* {
    transition: background-color 0.5s var(--ease-ios), 
                color 0.5s var(--ease-ios),
                /* ... 更多过渡属性 */
}
```

## 🌐 浏览器兼容性

| 浏览器 | 版本要求 |
|--------|----------|
| Chrome | 80+      |
| Firefox| 75+      |
| Safari | 13+      |
| Edge   | 80+      |

## 📝 开发说明

### 性能优化

- 使用CSS硬件加速：`transform: translateZ(0)`
- 优化动画效果：使用`will-change`属性提示浏览器
- 减少重绘重排：避免频繁DOM操作
- 缓存DOM元素：减少DOM查询次数

### 代码规范

- 使用语义化HTML标签
- 采用BEM命名规范
- 使用CSS变量管理样式
- 模块化JavaScript代码
- 注释清晰，便于维护

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源。

## 🤝 贡献指南

欢迎提交Issue和Pull Request！

### 提交Pull Request流程

1. Fork 本仓库
2. 创建特性分支：`git checkout -b feature/AmazingFeature`
3. 提交更改：`git commit -m 'Add some AmazingFeature'`
4. 推送到分支：`git push origin feature/AmazingFeature`
5. 提交Pull Request

### 代码审查

- 确保代码符合项目风格
- 确保所有功能正常工作
- 确保性能优化
- 编写清晰的注释

## 📧 联系方式

如有问题或建议，请通过以下方式联系：

- 提交 [Issue](https://github.com/Jimmy-xuzimo/AI-Assistant/issues)
- 发送邮件到：xuzimojimmy@163.com

## 🙏 致谢

- [Marked.js](https://marked.js.org/) - Markdown解析库
- [Google Fonts](https://fonts.google.com/) - 字体资源
- 所有为项目做出贡献的开发者

---

**享受使用AI助手界面！** 🚀
