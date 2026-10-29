# teach-me

[English](README.md)

一个短小的 Agent Skill，通过集中对话帮你学会一个具体问题。

讲解 → 尝试 → 反馈 → 换个情境应用。持续到你能展示当轮理解，或主动选择结束。你可以随时要求重讲、重练、角色互换或辩论挑战。

不搭建课程，不创建长期学习档案。“不创建记忆文件”不影响平台自身的聊天保存或数据保留设置；通过当轮检验也不代表已经长期掌握。

## 安装

将仓库中的 `SKILL.md` 复制到你的 Agent 技能目录下的 `teach-me` 文件夹。以 macOS 或 Linux 上的 Codex 为例：

```sh
git clone https://github.com/SNSuperNova/teach-me.git
mkdir -p ~/.codex/skills/teach-me
cp teach-me/SKILL.md ~/.codex/skills/teach-me/SKILL.md
```

如果设置了自定义 `CODEX_HOME`，使用其中的 `skills/teach-me` 目录。其他 Agent 使用各自支持的技能目录。

默认指令为英文。如需中文指令，将 `SKILL.zh-CN.md` 复制到安装目录并命名为 `SKILL.md`。两个版本采用同一方法，只需安装其中一个。指令语言不限制实际教学使用的语言。

## 使用

```text
用 $teach-me 帮我理解数据库事务。
```

过程中可以说：“换一种解释”“再来一道题”“我来教你”“挑战一下我的推理”。

## 文件

- [SKILL.md](SKILL.md)：默认英文版。
- [SKILL.zh-CN.md](SKILL.zh-CN.md)：中文版。

受 [grill-me](https://github.com/mattpocock/skills) 聚焦追问方式启发，面向互动学习独立编写。

## 许可证

[MIT](LICENSE)。
