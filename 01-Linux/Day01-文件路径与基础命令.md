---
标题: Linux Day 01｜文件、路径与基础命令
日期: 2026-09-18
阶段: Linux基础
Day: 01
状态: 已完成
标签:
  - Linux
  - 云运维
  - 文件系统
  - 路径
  - 基础命令
---

# Linux Day 01｜文件、路径与基础命令

> 今天的核心不是背命令，而是建立 Linux 最基本的操作模型：**我在哪、这里有什么、我要去哪、文件在哪里、命令到底对谁生效。**

## 🚨 Day 1 结束时的重点提醒

### 1. `pwd`

> [!warning] 高频薄弱点
> `pwd` = **Print Working Directory**  
> 作用：输出当前工作目录的路径。  
> 最短记忆：**我现在在哪？**

### 2. `~`

```text
~ = /home/yuaner
```

不是：

```text
/home/yuaner/下载
```

### 3. `tail`

```text
tail = 从文件结尾取内容
```

不是倒序显示。

### 4. `>` / `>>`

```text
>  = 覆盖
>> = 追加
```

并且重定向符应该写在引号外面。

### 5. 删除目录

```text
rmdir   = 只删空目录
rm -r   = 递归删除目录和内部内容
```

详细累计见：`[[高频薄弱点]]`

---

## 📌 今日完成内容

- [x] `pwd`
- [x] `whoami`
- [x] `hostname`
- [x] `uname -a`
- [x] `ls`
- [x] `ls -1`
- [x] `ls -l`
- [x] `ls -a`
- [x] `ls -la`
- [x] `cd`
- [x] `~`
- [x] `.`
- [x] `..`
- [x] 绝对路径
- [x] 相对路径
- [x] `mkdir`
- [x] `touch`
- [x] `cp`
- [x] `cp -r`
- [x] `mv`
- [x] `rm`
- [x] `rmdir`
- [x] `rm -r`
- [x] `echo`
- [x] `>`
- [x] `>>`
- [x] `cat`
- [x] `less`
- [x] `head`
- [x] `tail`

---

## 1. 三个最核心命令

```text
pwd = 我在哪？
ls  = 这里有什么？
cd  = 我要去哪？
```

### `pwd`

```bash
pwd
```

输出当前工作目录。

### `ls`

```bash
ls
```

查看当前目录内容。

### `cd`

```bash
cd 路径
```

切换目录。

---

## 2. 路径

### `~`

当前用户家目录：

```text
/home/yuaner
```

### `.`

当前目录。

### `..`

上一级目录。

### 绝对路径

从 `/` 开头：

```text
/home/yuaner/linux-lab/day1
```

### 相对路径

从当前 `pwd` 开始解释：

```text
linux-lab/day1
```

---

## 3. 文件和目录

### 创建目录

```bash
mkdir backup
```

### 创建空文件

```bash
touch file1.txt
```

`.txt` 只是文件名的一部分，不代表 Linux 创建了某种特殊“文本文档”。

---

## 4. 复制与移动

### 复制文件

```bash
cp file1.txt backup/
```

意思：

> 把 `file1.txt` 复制到 `backup/`。

### 复制目录

```bash
cp -r demo-dir demo-copy
```

`-r = recursive`

### 移动 / 改名

```bash
mv file2.txt hello.txt
```

或者：

```bash
mv file1.txt backup/
```

---

## 5. 删除

```bash
rm file.txt
```

删除文件。

```bash
rmdir backup
```

删除空目录。

```bash
rm -r backup
```

递归删除目录。

---

## 6. 查看文件内容

```bash
cat hello.txt
```

看全部。

```bash
head -n 3 hello.txt
```

看前 3 行。

```bash
tail -n 2 hello.txt
```

看后 2 行。

```bash
less hello.txt
```

分页查看。

---

## 7. 输出重定向

```bash
echo "A" > file.txt
```

覆盖。

```bash
echo "B" >> file.txt
```

追加。

---

## ⚠️ 今日真实错误

### 命令拼写

错误：

```bash
umname -a
```

正确：

```bash
uname -a
```

### 多条命令直接挤在一起

错误：

```bash
cd / pwd ls -l
```

正确：

```bash
cd /
pwd
ls -l
```

### 命令与参数之间缺空格

错误：

```bash
cd/
```

正确：

```bash
cd /
```

### 重定向符位置错误

错误：

```bash
echo ""Linux Day 1">notes.txt"
```

正确：

```bash
echo "Linux Day 1" > notes.txt
```

---

## ❓ 今日重点疑问

- `ls` 多列显示时，左右是不是对应关系？→ 不是。
- `~` 到底是什么？→ `/home/yuaner`
- 相对路径和绝对路径有什么区别？
- `rm backup/` 为什么不行？
- `rmdir` 为什么提示目录非空？
- `tail` 是不是倒着显示？→ 不是。
- `cp file1.txt backup/` 为什么要写 `backup/`？→ 它是目标目录。
- Obsidian 仓库嵌套怎么处理？→ 用 `mv` 移出真正仓库，再删空外层目录。

---

## 🧪 Obsidian 真实路径案例

原来：

```text
/home/yuaner/
└── Cloud-Learning/
    └── cloud-learning/
```

移动：

```bash
mv ~/Cloud-Learning/cloud-learning ~/cloud-learning
```

确认外层为空后：

```bash
rmdir ~/Cloud-Learning
```

最终：

```text
/home/yuaner/
└── cloud-learning/
```

这个案例体现：

```text
先检查
↓
移动
↓
再检查
↓
确认空目录
↓
删除
```

---

## 🔀 易混淆速查

| 容易混 | 正确区别 |
|---|---|
| `pwd` / `ls` | 当前在哪 / 当前有什么 |
| `~` / `~/下载` | 家目录 / 家目录下的下载目录 |
| `cp` / `mv` | 复制 / 移动 |
| `rm` / `rmdir` / `rm -r` | 文件 / 空目录 / 递归目录 |
| `>` / `>>` | 覆盖 / 追加 |
| `head` / `tail` | 前 N 行 / 后 N 行 |
| `Cloud-Learning` / `cloud-learning` | Linux 下是不同名字 |

---

## 🔁 下次开始前先答

1. `pwd` 到底是什么意思？
2. `~` 等于哪个路径？
3. `tail -n 2 file.txt` 会不会倒序？
4. `>` 和 `>>` 区别是什么？
5. `rmdir` 和 `rm -r` 区别是什么？
6. 当前在 `/home/yuaner/linux-lab/day1`，执行 `mkdir test`，完整路径是什么？

---

## ✅ Day 1 状态

- [x] ==Day 1 已完成==
- [x] 已建立 Obsidian 学习库
- [x] 已开始记录真实错误
- [x] 已建立“高频薄弱点”机制
- [ ] Day 2 开始前完成快速复习
