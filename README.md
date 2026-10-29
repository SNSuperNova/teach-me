# teach-me

[简体中文](README.zh-CN.md)

A small Agent Skill for learning one thing through a focused conversation.

Explain → try → get feedback → apply it in a new situation. Keep going until you can demonstrate understanding for this session, or choose to stop. Request another explanation, more practice, role reversal, or a debate whenever useful.

No course scaffolding or persistent learning records. The skill does not create memory files; it does not change your agent platform’s chat storage or retention settings. Passing a session check does not establish long-term retention.

## Install

Copy this repository’s `SKILL.md` into a `teach-me` folder in your agent’s skills directory. For Codex on macOS or Linux:

```sh
git clone https://github.com/SNSuperNova/teach-me.git
mkdir -p ~/.codex/skills/teach-me
cp teach-me/SKILL.md ~/.codex/skills/teach-me/SKILL.md
```

If you use a custom `CODEX_HOME`, use its `skills/teach-me` directory instead. For another agent, use that agent’s supported skills directory.

The default instructions are in English. To use the Chinese instructions, copy `SKILL.zh-CN.md` as `SKILL.md` in the installed skill folder instead. Install one version; both implement the same method. Instruction language does not restrict the language you can learn in.

## Use

```text
Use $teach-me to help me understand database transactions.
```

During the session, try: “Explain it differently,” “Give me another problem,” “Let me teach you,” or “Challenge my reasoning.”

## Files

- [SKILL.md](SKILL.md): default English instructions.
- [SKILL.zh-CN.md](SKILL.zh-CN.md): Chinese translation.

Inspired by the focused questioning approach of [grill-me](https://github.com/mattpocock/skills), adapted here for interactive learning. This repository’s teaching instructions were written independently.

## License

[MIT](LICENSE).
