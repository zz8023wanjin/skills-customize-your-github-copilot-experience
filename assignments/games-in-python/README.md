
# 🎮 Assignment: Hangman — Word Guessing Game

## 🎯 Objective

实现经典的 Hangman（刽子手）文字猜词游戏，练习字符串处理、控制流与用户交互。

## 🎯 Learning Outcomes

完成此作业后，你将能够：

- 使用列表/集合跟踪已猜字母与剩余尝试次数
- 将程序分解为可复用函数（例如：选择单词、显示进度、处理猜测）
- 处理用户输入与常见错误（重复猜测、非法输入）
- 撰写简单的单元测试来验证关键函数

## 🔧 Prerequisites

- Python 3.8+ 已安装
- 熟悉基本语法（字符串、列表、控制流、函数）
- 已克隆仓库并能在终端运行 Python 脚本

## 📝 Tasks

### 🛠️ Task 1 — 实现 Hangman 游戏

#### Description

实现一个命令行版 Hangman：程序从单词列表中随机选择一个单词，玩家通过输入字母逐步猜出单词。在每次猜测后显示当前猜测进度（例如 `a _ _ l e`）与剩余错误次数。

#### Input / Output 示例

- 启动：

```
$ python3 starter-code.py
```

- 交互示例：

```
Word: _ _ _ _ _
Guess a letter: e
Correct! Word: _ _ _ _ e
Guesses remaining: 6
```

#### Requirements (验收条件)

你的程序必须：

- 从一个预定义的单词列表随机选择单词（列表可存于代码中或单独文件）
- 接受单字母猜测，并在每次显示当前进度（例如 `_ a _ _`）
- 跟踪并显示剩余的错误猜测次数
- 当单词被完全猜出或尝试用尽时结束游戏并显示胜利/失败消息
- 对重复猜测给出提示且不重复扣除尝试次数
- 对非法输入（如多字符、非字母）友好地提示用户并要求重试

#### 评估要点 / Grading Notes

- 功能正确性（70%）：所有验收条件均满足并通过示例交互
- 代码质量（20%）：函数划分合理、变量命名清晰、包含必要注释
- 错误处理与可用性（10%）：对边界条件与无效输入处理良好

### 🛠️ Task 2 — 可选扩展（加分）

- 增加一个“难度”选项来控制单词长度或允许的错误次数
- 将单词列表放入外部文件并实现从文件加载
- 使用简单的 GUI（如 Tkinter）实现图形界面

## 📁 Deliverables

- `starter-code.py`（或 `hangman.py`）——完整可运行的程序
- 可选：`tests/test_game.py` —— 若写了自动化测试
- `README.md`（本文件）说明如何运行与测试

提交说明：将代码推送到你的作业目录，或按课堂要求打包上传，例如 `user-<学号>-hangman.zip`。

## 🧾 Rubric

- 正确性：70
- 代码质量与风格：20
- 文档与测试：10

## 💡 Hints & Resources

- 先实现最小可行版本（MVP）：随机选词 + 显示 `_ _ _` 格式 + 处理单字符猜测
- 使用集合（set）来跟踪已猜字母会更方便
- Python 文档：string 模块与 random.choice

## ✅ Suggested Tests

- 手动测试：
	- 猜到正确字母后进度更新
	- 猜错时尝试次数减少
	- 重复猜测不扣次数
	- 非字母输入被拒绝

- 自动化（可选）：写几个单元测试验证 `reveal_letters(secret, guesses)` 等纯函数的输出

运行测试示例：

```
$ python3 -m pytest tests
```

## 📦 Starter Files

- `starter-code.py` — 提供了基本程序骨架（如 `main()`、单词列表加载）

如果仓库里没有 `starter-code.py`，请将你的主脚本命名为 `hangman.py` 并在 README 中说明运行方法。

## 🔁 Optional Extensions (加分项)

- 添加游戏计分或排行榜
- 为 GUI 或网络版实现基础逻辑并把 CLI 作为备选项

## 🧑‍⚖️ Academic Integrity

允许讨论问题与伪代码，但禁止直接共享完整代码答案。提交时请注明任何参考资源与合作者。

---

祝你编码愉快！如果你想，我可以基于此模板自动生成 `starter-code.py` 的一个参考实现或添加单元测试示例。
