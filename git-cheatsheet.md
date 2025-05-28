
# 🚀 Git 常用命令大全

> 本文整理了 Git 最常用的操作命令，适合开发者日常使用、复习或查阅。

---

## 🧱 一、基本配置

```bash
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
git config --global core.editor "vim"     # 设置默认编辑器，可选
git config --list                          # 查看当前 Git 配置
```

---

## 📁 二、仓库初始化与克隆

```bash
git init                                    # 初始化本地仓库
git clone https://github.com/xxx/yyy.git   # 克隆远程仓库（HTTPS）
git clone git@github.com:xxx/yyy.git       # 克隆远程仓库（SSH）
```

---

## 🧩 三、文件操作

```bash
git status                # 查看当前状态
git add 文件名            # 添加指定文件
git add .                 # 添加当前目录所有文件
git rm 文件名             # 删除文件并提交更改
git mv 旧名 新名          # 重命名文件
```

---

## ✅ 四、提交修改

```bash
git commit -m "提交说明"            # 提交暂存区文件
git commit -am "提交说明"           # 跳过 add，直接提交已跟踪的文件
git log                            # 查看提交历史
git log --oneline --graph --all    # 简洁图示所有分支提交
```

---

## 🌿 五、分支管理

```bash
git branch                         # 查看本地分支
git branch 分支名                  # 创建新分支
git checkout 分支名                # 切换分支
git checkout -b 新分支名           # 创建并切换分支
git merge 分支名                   # 合并其他分支到当前分支
git branch -d 分支名               # 删除本地分支
```

---

## 📡 六、远程仓库

```bash
git remote -v                                        # 查看远程地址
git remote add origin 地址                           # 添加远程仓库
git push origin 分支名                               # 推送分支
git push --set-upstream origin 分支名                # 设置上游分支并推送
git fetch                                            # 拉取远程但不合并
git pull                                             # 拉取并合并（fetch + merge）
git pull --rebase                                    # 拉取并使用 rebase 策略
```

---

## 🛠️ 七、修改历史与回滚

```bash
git diff                              # 查看尚未暂存的更改
git diff --staged                     # 查看已暂存的更改
git reset 文件名                      # 撤销 add 操作
git reset --hard 提交ID              # 回退到某次提交（彻底清除）
git revert 提交ID                    # 撤销某次提交（生成反向提交）
```

---

## 🧪 八、标签操作

```bash
git tag                              # 查看所有标签
git tag v1.0                         # 创建标签
git tag -d v1.0                      # 删除标签
git push origin v1.0                 # 推送标签
git push origin --tags               # 推送所有标签
```

---

## 📂 九、查看与查找

```bash
git show 提交ID                      # 查看某次提交详情
git blame 文件名                    # 查看文件的逐行修改记录
git log -p 文件名                   # 查看某文件提交历史及内容变更
git diff 分支1 分支2                 # 比较两个分支的差异
```

---

## 💡 十、子模块（如果使用）

```bash
git submodule add 仓库地址 路径     # 添加子模块
git submodule update --init         # 初始化子模块
```

---

## 📋 十一、推荐别名设置（可选）

```bash
# 美化日志输出
git config --global alias.lg "log --oneline --graph --decorate --all"
```

之后可以用 `git lg` 快速查看分支历史。

---

> 作者：ChatGPT @ OpenAI  
> 更新时间：2025 年  
