# 饭歪歪的个人网站

这是一个使用 GitHub Pages 托管的静态个人网站。

## 功能

- **首页**：个人简介和头像上传
- **日志**：按日期查看日志内容（支持 Markdown）
- **to do**：日历视图和任务管理
- **成长**：按分类查看成长记录（支持 Markdown）
- **思考**：查看思考文章（支持 Markdown）

## 页面说明

### 首页 (index.html)
- 左侧：圆形头像上传区域
- 右侧：个人简介输入框（最多100字）
- 底部：欢迎信息、联系方式和版权信息

### 日志 (log.html)
- 左侧：日期列表（从2025.12.29开始）
- 右侧：显示选中日期的 Markdown 文件内容

### to do (todo.html)
- 顶部：当前日期显示
- 中间：日历网格（7列x5行，从12.29开始）
- 底部：点击日期后显示该日的任务列表

### 成长 (growth.html)
- 左侧：分类列表（生日、小学、初中、高中、大学、工作等）
- 右侧：显示选中分类的 Markdown 文件内容

### 思考 (thought.html)
- 左侧：标题列表（16个标题）
- 右侧：显示选中标题的 Markdown 文件内容

## 部署到 GitHub Pages

1. 在 GitHub 上创建一个新仓库
2. 将所有文件推送到仓库
3. 在仓库设置中：
   - 进入 Settings → Pages
   - Source 选择 "Deploy from a branch"
   - Branch 选择 "main" 或 "master"
   - 点击 Save
4. 等待几分钟后，访问 `https://你的用户名.github.io/仓库名/`

## 本地开发

直接在浏览器中打开 `index.html` 即可查看。

## Markdown 文件结构

```
markdown/
├── log/           # 日志文件，命名格式：YYYY.MM.DD.md
├── growth/        # 成长文件
└── thought/       # 思考文件，命名格式：1.md, 2.md, ...
```

## 技术栈

- HTML5
- CSS3
- JavaScript (原生)
- Marked.js (Markdown 解析)

## 注意事项

1. **头像上传**：首页头像上传功能使用 localStorage 存储，仅在当前浏览器中保存
2. **任务存储**：to do 页面的任务使用 localStorage，仅在当前浏览器中保存
3. **Markdown 文件**：需要手动创建对应的 Markdown 文件，系统会自动加载显示

## 浏览器支持

- Chrome (推荐)
- Firefox
- Safari
- Edge

## 许可证

版权归@饭歪歪所有

