以下是 Ubuntu 终端快捷键与 Linux Vim 编辑器的快捷键详解及对比，内容分模块整理，便于快速查阅：

---

### **一、Ubuntu 终端常用快捷键**
主要用于提高命令行操作效率，适用于 Bash/Zsh 等 Shell 环境。

#### **1. 光标操作**
| 快捷键          | 功能描述                   |
|----------------|--------------------------|
| `Ctrl + A`     | 移动光标到行首             |
| `Ctrl + E`     | 移动光标到行尾             |
| `Alt + B`      | 向后移动一个单词（单词级左移） |
| `Alt + F`      | 向前移动一个单词（单词级右移） |
| `Ctrl + ←/→`   | 按单词左右跳转（部分终端支持）|

#### **2. 编辑与历史**
| 快捷键          | 功能描述                   |
|----------------|--------------------------|
| `Ctrl + U`     | 删除从光标到行首的内容       |
| `Ctrl + K`     | 删除从光标到行尾的内容       |
| `Ctrl + W`     | 删除前一个单词             |
| `Ctrl + C`     | 终止当前命令/进程           |
| `Ctrl + Z`     | 挂起当前进程（`fg` 恢复）   |
| `Ctrl + R`     | 反向搜索历史命令            |
| `Ctrl + L`     | 清屏（类似 `clear` 命令）   |
| `!!`           | 重复上一条命令              |
| `!<前缀>`      | 执行最近以指定前缀开头的命令 |

#### **3. 补全与多任务**
| 快捷键          | 功能描述                   |
|----------------|--------------------------|
| `Tab`          | 自动补全文件/命令/路径      |
| `Ctrl + D`     | 退出终端或发送 EOF 信号     |
| `Ctrl + S`     | 暂停终端输出（冻结）        |
| `Ctrl + Q`     | 恢复终端输出（解冻）        |

---

### **二、Vim 编辑器快捷键**
Vim 分不同模式，需注意当前模式（**普通模式**、**插入模式**、**可视模式**、**命令模式**）。

#### **1. 模式切换**
| 快捷键          | 功能描述                   |
|----------------|--------------------------|
| `i`            | 进入插入模式（光标前插入）   |
| `a`            | 进入插入模式（光标后插入）   |
| `o`            | 在当前行下方插入新行        |
| `O`            | 在当前行上方插入新行        |
| `Esc`          | 返回普通模式               |
| `:`            | 进入命令模式               |

#### **2. 普通模式操作**
| 快捷键          | 功能描述                   |
|----------------|--------------------------|
| `h/j/k/l`      | 左/下/上/右移动光标        |
| `w` / `b`      | 向前/向后跳转一个单词       |
| `0` / `$`      | 跳转到行首/行尾            |
| `gg` / `G`     | 跳转到文件首行/末行         |
| `Ctrl + F/B`   | 向前/向后翻页              |
| `dd`           | 删除当前行                 |
| `yy`           | 复制当前行                 |
| `p` / `P`      | 粘贴到光标后/前            |
| `u`            | 撤销操作                   |
| `Ctrl + R`     | 重做操作                   |
| `/文本`         | 向下搜索文本               |
| `?文本`         | 向上搜索文本               |
| `:%s/old/new/g`| 全局替换文本               |

#### **3. 可视模式操作**
| 快捷键          | 功能描述                   |
|----------------|--------------------------|
| `v`            | 进入字符可视模式           |
| `V`            | 进入行可视模式             |
| `Ctrl + V`     | 进入块可视模式             |
| 选中后按 `d`    | 删除选中内容               |
| 选中后按 `y`    | 复制选中内容               |

#### **4. 命令模式操作**
| 命令            | 功能描述                   |
|----------------|--------------------------|
| `:w`           | 保存文件                  |
| `:q`           | 退出 Vim                 |
| `:q!`          | 强制退出不保存            |
| `:wq` / `:x`   | 保存并退出                |
| `:set nu`      | 显示行号                  |
| `:行号`         | 跳转到指定行              |

---

### **三、终端与 Vim 快捷键对比**

| **类别**        | **终端快捷键**              | **Vim 快捷键**               | **对比说明**                  |
|----------------|---------------------------|-----------------------------|-----------------------------|
| **光标移动**    | `Ctrl + A/E` 跳转行首/尾   | `0/$` 跳转行首/尾            | 终端更依赖组合键，Vim 用单键符号  |
| **删除操作**    | `Ctrl + U/K` 删除行首/尾   | `dd` 删除整行                | 终端按区域删除，Vim 按行/块操作   |
| **历史操作**    | `Ctrl + R` 搜索历史命令    | `q:` 查看命令历史            | 终端直接搜索，Vim 需进入历史模式  |
| **进程控制**    | `Ctrl + C/Z` 终止/挂起进程 | Vim 无直接对应操作           | 终端面向进程，Vim 专注文本编辑    |
| **模式切换**    | 无模式概念                 | `Esc` 返回普通模式           | Vim 需频繁切换模式，终端无此设计  |
| **复制粘贴**    | 依赖鼠标或 `Shift` 组合键  | `yy/p` 纯键盘操作            | Vim 完全键盘驱动，终端依赖外部操作 |

---

### **四、使用建议**
1. **终端快捷键**：适合快速执行命令、管理进程、补全路径。
2. **Vim 快捷键**：需熟悉模式切换，通过组合键高效编辑文本。
3. **注意冲突**：如 `Ctrl + C` 在终端用于终止进程，在 Vim 普通模式下可能触发命令（需配置或按 `Esc` 确保模式正确）。

掌握这些快捷键可显著提升 Linux 环境下的操作效率。建议逐步练习，形成肌肉记忆。