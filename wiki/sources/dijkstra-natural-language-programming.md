---
title: "EWD 667: On the foolishness of \"natural language programming\""
type: source
status: active
created: 2026-05-10
updated: 2026-05-10
domain: programming-languages
tags:
  - wiki/source
  - dijkstra
  - natural-language-programming
  - formal-methods
source_files:
  - raw/assets/E.W.Dijkstra Archive On the foolishness of "natural language programming". (EWD 667).md
original_url: https://www.cs.utexas.edu/~EWD/transcriptions/EWD06xx/EWD667.html
---

# EWD 667: On the foolishness of "natural language programming"

## 摘要

- EWD 667 是 Dijkstra 对 "自然语言编程" 构想的尖锐反驳。他认为编程必须使用形式符号系统, 这不是负担而是特权; 自然语言编程不仅不会让编程变简单, 反而会让机器和人都更难工作。
- 文章发表于手稿编号 EWD 667, 源自 Dijkstra 在 UT Austin 时期的手写笔记转录。

## 关键论点

### 形式符号不是缺陷, 而是进步的前提

- 早期的机器码几乎没有冗余, 琐碎笔误就会导致错误结果。高级语言改善了这一点, 使得错误可以被检测和报错, 而非悄悄产生错误答案。
- 有些人至今仍将 "容易编程" 等同于 "容易制造不被发现的错误"。Dijkstra 认为这种态度恰恰暴露了对形式系统的根本误解。
- 形式文本的美德在于: 操作是否合法只需满足少数几条简单规则, 因此可以用极小代价排除自然语言中几乎不可避免的各种 nonsense。

### 数学史的证据

- 希腊数学停留在口头与图示阶段而停滞; 穆斯林代数在象征化尝试后回到修辞文体而消亡; 西欧能从中世纪经院哲学的 "口头精确" 幻想中挣脱, 靠的是 Vieta、Descartes、Leibniz、Boole 等人有意识设计的形式符号系统。
- 形式符号系统使 "学童也能做到从前只有天才才能做到的事"。

### "窄界面" 优于自然语言界面

- 界面的选择不只是固定工作量的切分, 跨界面协作与沟通本身会新增工作量。改变界面形式 "很容易让界面两端的工作量都急剧增加", 因此窄界面更可取。
- 自然语言界面会极大增加机器的负担, 但对人真的会变简单吗? Dijkstra 表示高度怀疑。

### 如果一开始就只有自然语言界面

- Dijkstra 推测: 计算机科学将主要成为一门 "黑魔法般的技艺", 全部智力都将消耗在从自然语言引导出一个可用形式系统的过程上, "可能需要再花几千年"。

### "新文盲" 的警句

- Dijkstra 观察到 20 世纪后期西方世界母语掌握能力急剧衰退 (The New Illiteracy), 大量科学文章、技术报告和政府出版物充满 "仔细阅读后毫无意义的废话"。
- 他认为这一现象足以让那些缺乏技术洞察力、却相信自然语言编程的人感到气馁。

### 最后的一丝慰藉

- "能用母语编程的机器, 做起来和用起来大概都同样难到该死。"

## 值得注意的引述

- "形式文本的美德在于: 其操作是否合法只需满足少数几条简单规则——想想看, 这真是排除各种 nonsense 的惊人高效工具。"
- "当我们说使用母语很 '自然' 时, 归根结底指的是我们很容易用它说出 nonsense 不明显的话。"
- "我们不应把使用形式符号的义务看作负担, 而应看作特权。"

## 开放问题

- Dijkstra 写于 1970 年代末; 今天的 LLM 作为自然语言编程界面, 在多大程度上印证或反驳了他的论点?
- "窄界面" 对 LLM agent 设计的启示: 是否应刻意限制 agent 与工具之间的语义带宽?
- "新文盲" 在互联网时代是否加速了?

## 相关页面

- [Edsger W. Dijkstra](../entities/edsger-dijkstra.md)
- [Natural Language Programming](../concepts/natural-language-programming.md)
- [Agent-First Engineering](../concepts/agent-first-engineering.md)
