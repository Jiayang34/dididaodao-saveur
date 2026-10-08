# 地地道道 · Saveur

## 一、项目简介

“地地道道 · Saveur”是一个用于整理、保存和分享菜谱的公开仓库。菜谱按照烹饪方式和菜品类型分为炒菜、汤菜、炖菜、凉菜、面食、甜点、茶点和西餐八类。

每道菜谱使用独立的 Markdown 文件保存，可以包含成品图片、食材用量、制作步骤和补充说明。项目首页的“菜品总览”按照编号列出全部菜谱，并链接到对应文件。

## 二、使用 Git 参与项目

### 1. 获取仓库

如果你已经被添加为本仓库的协作者，可以直接克隆仓库：

```bash
git clone https://github.com/Jiayang34/dididaodao-saveur.git
cd dididaodao-saveur
```

如果你没有本仓库的写入权限，请先在 GitHub 页面右上角点击 **Fork**，将仓库复制到自己的账号，再克隆自己的 Fork：

```bash
git clone https://github.com/你的用户名/dididaodao-saveur.git
cd dididaodao-saveur
git remote add upstream https://github.com/Jiayang34/dididaodao-saveur.git
```

首次修改前，先让本地 `main` 与远程仓库保持同步：

```bash
git switch main
git pull origin main
```

通过 Fork 参与时，可以从主仓库同步：

```bash
git fetch upstream
git merge upstream/main
```

### 2. 创建自己的分支

不要直接修改 `main`。每次新增或修改菜谱时，从最新的 `main` 创建一个独立分支：

```bash
git switch main
git pull origin main
git switch -c recipe/001-hong-shao-rou
```

建议使用 `recipe/编号-英文或拼音名称` 作为新增菜谱的分支名；修正已有菜谱时可以使用 `fix/编号-修改内容`。

### 3. 编写菜谱

在对应分类目录中创建 Markdown 文件，文件名格式为：

```text
编号-菜名.md
```

例如：

```text
炖菜/001-红烧肉.md
```

推荐使用以下基本结构：

```md
# 001 红烧肉

![成品照片](图片相对路径)

## 食材

| 食材 | 用量 |
| --- | ---: |
| 猪肉 | 500 g |
| 盐 | 10 g |

## 做法

1. 第一步……
2. 第二步……

## 补充说明

- 特别注意事项、火候、替代食材或保存方法等。
```

### 4. 在菜品总览中添加链接

完成菜谱后，在本 README 的“菜品总览”中找到对应分类，按照编号添加相对链接：

```md
- [001 红烧肉](炖菜/001-红烧肉.md)
```

请确保编号、菜名、文件名和链接保持一致。

### 5. 检查并提交修改

先查看本次修改：

```bash
git status
git diff
```

添加菜谱文件和 README，然后提交：

```bash
git add "炖菜/001-红烧肉.md" README.md
git commit -m "Add recipe 001 红烧肉"
```

### 6. 推送自己的分支

```bash
git push -u origin recipe/001-hong-shao-rou
```

后续继续修改同一分支时，只需执行：

```bash
git push
```

### 7. 请求合并到 main

推送后，打开 GitHub 仓库页面并创建 Pull Request：

1. 将目标分支（base）选择为 `main`。
2. 将来源分支（compare）选择为自己的菜谱分支。
3. 填写本次新增或修改的内容，然后创建 Pull Request。
4. 检查文件和链接无误后，再手动合并到 `main`。
5. 合并完成后，可以删除已经使用完毕的菜谱分支。

受保护的 `main` 分支不接受直接推送，所有菜谱修改都应通过 Pull Request 合并。

## 三、菜品总览

### 炒菜

暂无菜谱。

### 汤菜

暂无菜谱。

### 炖菜

暂无菜谱。

### 凉菜

暂无菜谱。

### 面食

暂无菜谱。

### 甜点

暂无菜谱。

### 茶点

暂无菜谱。

### 西餐

暂无菜谱。
