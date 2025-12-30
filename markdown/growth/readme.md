修改完成

## 实现的功能
##保留一级标题
保留：生日、小学、初中、高中、大学、工作、......

##动态生成二级标题
二级标题从实际存在的 md 文档的第一行标题提取

##只显示实际存在的文件
文件映射关系
birthday-*.md → 生日
primary-*.md → 小学
middle-*.md → 初中
high-*.md → 高中
university-*.md → 大学
work*.md → 工作

文件检测列表
生日：birthday-family.md, birthday-sick.md, birthday-play.md
小学：primary-xinghua.md, primary-qianxian.md, primary-shaanshida.md
初中：middle-xigongda.md
高中：high-xigongda.md
大学：university-zhejiang.md
工作：work.md

##关键代码逻辑
##文件映射关系（第68-75行）：
const categoryMapping = {    
'birthday-': '生日',    
'primary-': '小学',    
'middle-': '初中',    
'high-': '高中',    
'university-': '大学',    
'work': '工作'};

##动态生成分类列表（第77-180行）：
检测所有可能的文件
根据文件名前缀确定所属分类
从文件第一行提取标题作为二级标题
只显示实际存在的文件
现在 growth.html 页面会根据实际存在的 md 文档动态生成菜单，二级标题从文档的第一行标题提取。
