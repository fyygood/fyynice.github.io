# 修改完成：Growth 页面动态菜单功能

### 实现的功能
* **保留一级标题**：保留“生日、小学、初中、高中、大学、工作”等核心分类。
* **动态生成二级标题**：二级标题内容从实际存在的 `.md` 文档的**第一行标题**中提取。
* **按需显示**：只显示物理路径中实际存在的文件，不存在的文件不进入列表。

### 文件映射关系
系统根据文件名前缀将文档归类到对应模块：

| 文件名前缀 | 对应分类 |
| :--- | :--- |
| `birthday-*.md` | 生日 |
| `primary-*.md` | 小学 |
| `middle-*.md` | 初中 |
| `high-*.md` | 高中 |
| `university-*.md` | 大学 |
| `work*.md` | 工作 |

### 文件检测列表
目前系统支持检测并匹配以下文件：
* **生日**：`birthday-family.md`, `birthday-sick.md`, `birthday-play.md`
* **小学**：`primary-xinghua.md`, `primary-qianxian.md`, `primary-shaanshida.md`
* **初中**：`middle-xigongda.md`
* **高中**：`high-xigongda.md`
* **大学**：`university-zhejiang.md`
* **工作**：`work.md`

---

### 关键代码逻辑

#### 1. 文件映射关系 (第68-75行)
通过常量定义前缀与中文分类的映射：

```javascript
const categoryMapping = {
    'birthday-': '生日',
    'primary-': '小学',
    'middle-': '初中',
    'high-': '高中',
    'university-': '大学',
    'work': '工作'
};
