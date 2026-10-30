# teach-me — An Interactive AI Tutoring Skill

[简体中文](README.zh-CN.md)

**teach-me is an MIT-licensed Agent Skill for learning one concept or method in a short, focused conversation.** It guides an AI tutor to explain, ask you to try, give feedback, and check your understanding in a new situation. It keeps the session focused without creating a course or persistent learning records.

Use it when you want to understand something and practice it yourself, rather than simply receive an answer.

## When should I use teach-me?

- **Understand a concept:** explain database transactions in your own words and reason through an example.
- **Learn a method:** practice debugging a small problem, with hints instead of the finished solution.
- **Test your reasoning:** defend an explanation against counterexamples or find the flaw in an argument.
- **Learn by teaching:** explain the topic to the agent and have it check your reasoning.

Choose one topic for the session. You can ask for another explanation, repeat an exercise, request a challenge, or stop at any time.

## How does a session work?

**Check the starting point → explain one key idea → let you try → give feedback → test a changed example.**

The tutor waits for your answers and adjusts to specific misunderstandings. It does not treat “I get it,” a copied explanation, or a correct guess as proof of understanding. A session can end when you independently explain the key reasoning and apply it in a new situation; you choose whether to continue.

### Example interaction

*Illustrative example of the intended interaction, not a recorded test.*

> **You:** Help me understand why a database transaction matters for a money transfer.
>
> **Tutor:** Suppose debiting the sender succeeds, but crediting the receiver fails. What has gone wrong?
>
> **You:** The sender loses money, but the receiver gets nothing.
>
> **Tutor:** Right. Atomicity makes these updates succeed together or roll back together. Now suppose a stock update succeeds but creating the order fails. What should happen, and why?

## How is teach-me different from grill-me?

[grill-me](https://github.com/mattpocock/skills) uses questioning to sharpen a plan or decision. **teach-me uses teaching, practice, and challenges to check your understanding of a topic.** It was inspired by that focused questioning approach; its teaching instructions were written independently.

## Install

The skill is a Markdown instruction file, not a standalone tutoring app. Use an agent that supports the `SKILL.md` format. For Codex on macOS or Linux:

```sh
git clone https://github.com/SNSuperNova/teach-me.git
mkdir -p ~/.codex/skills/teach-me
cp teach-me/SKILL.md ~/.codex/skills/teach-me/SKILL.md
```

If you use a custom `CODEX_HOME`, use its `skills/teach-me` directory instead. Other agents use their own supported skill locations.

The default instructions are in English. To install the Chinese version, copy `SKILL.zh-CN.md` as `SKILL.md` instead. Install one version; both describe the same method. You can request teaching in either language.

## Use

```text
Use $teach-me to help me understand database transactions.
```

During the session, try: “Explain it differently,” “Give me another problem,” “Let me teach you,” or “Challenge my reasoning.”

## Frequently asked questions

**Does teach-me remember my progress between sessions?**

The skill uses the current conversation and does not create persistent learning records. It does not change your agent platform’s chat storage, memory, or retention settings.

**Does completing a session mean I have mastered the topic?**

It shows what you demonstrated in that session. It does not establish long-term retention. You can repeat the topic or request more practice yourself.

**Is teach-me only for programming?**

No. The instructions are topic-independent. Choose a concept or method whose understanding you can check through explanation, prediction, or a practical task. Teaching quality depends on the model and the sources available to it.

## Source and license

- [SKILL.md](SKILL.md): default English teaching instructions.
- [SKILL.zh-CN.md](SKILL.zh-CN.md): Chinese teaching instructions.
- Maintained by [SNSuperNova](https://github.com/SNSuperNova) in the [teach-me repository](https://github.com/SNSuperNova/teach-me).
- [MIT License](LICENSE).
