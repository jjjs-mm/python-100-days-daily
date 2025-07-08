# 🏷 Day 01 - git管理技术学习

## ✅ 今日目标

- 以我的新的库python-100-days-daily为例用git我的代码管理

## 💡 学习内容

- ***知识点总结***

  git的建立，clone，更新，连接到github上，使用SSH进行远程连接到库（基本上都在终端操作）

**首次操作（每次建立新的仓库时需要操作的）：**

1. 先在我的GitHub上建立了一个new repository（新仓库）即python-100-days-daily
2. 然后进行clone（如果克隆过就不再需要），即利用终端在**本地桌面**建了这个文件夹：

       jsdymmm@192 ~ % cd ~/Desktop    

       jsdymmm@192 Desktop % git clone [https://github.com/jjjss-mm/python-100-days-daily.git](https://github.com/jjjss-mm/python-100-days-daily.git)

       即以后打开需要在终端输入cd ~/Desktop/python-100-days-daily打开仓库

**需要每日做的操作：**

1. 检查远程地址：git remote -v
2. 直接push每日更新内容（每日代码和笔记整理好后）：

       git add .
       git commit -m "Day 2: 更新内容-Python基础知识学习”
       git push

**SSH部分操作：**

测试SSH连接：

ssh -T [git@github.com](mailto:git@github.com)

会提示：

Hi jjjs-mm! You've successfully authenticated, but GitHub does not provide shell access.

- 难点、易错点：在GitHub上我的SSH在这个界面

![截屏2025-07-06 17.51.20.png](%F0%9F%8F%B7%20Day%2001%20-%20git%E7%AE%A1%E7%90%86%E6%8A%80%E6%9C%AF%E5%AD%A6%E4%B9%A0%20228751064ef88038ba75f97687f29780/%E6%88%AA%E5%B1%8F2025-07-06_17.51.20.png)

## ✍️ 代码/笔记

```python
# 示例代码
print("暂无代码学习")

```

- 每日提交一次 GitHub / Notion 笔记