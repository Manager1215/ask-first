# ask-first

A skill for Claude that makes it **ask clarifying questions before doing any non-trivial task**, instead of guessing what you meant.

## The problem

You ask Claude for a script, a config, a document or a plan — and it immediately produces something based on assumptions you never made. Then you spend several messages correcting it.

## What ask-first does

- **Triggers only on real tasks** — code, configs, deployments, documents, presentations, designs, plans, emails. Simple questions ("what is X", a fact, a quick translation) are answered right away.
- **Asks in rounds** of up to 4 multiple-choice questions (you can always type your own answer), covering:
  goal → context → constraints → result format → audience → examples → edge cases and risks.
- **Builds each round on your previous answers** and never asks what you've already told it.
- **Confirms before working** — it restates its understanding of the task and waits for your "yes".
- **Easy to stop** — say "enough questions" or "do it your way", and Claude starts immediately, listing the assumptions it made.
- Replies in your language.

## Installation

### Claude Code (as a plugin)

```
/plugin marketplace add Manager1215/ask-first
/plugin install ask-first@ask-first
```

### Claude Code (manually)

Copy the skill folder into your skills directory:

```bash
git clone https://github.com/Manager1215/ask-first.git
mkdir -p ~/.claude/skills
cp -r ask-first/plugins/ask-first/skills/ask-first ~/.claude/skills/
```

### Claude apps (claude.ai, desktop, mobile)

1. Download [`ask-first.zip`](https://github.com/Manager1215/ask-first/raw/main/ask-first.zip) (or zip the `plugins/ask-first/skills/ask-first` folder yourself).
2. Upload it in the Skills section of your Claude settings.

## Repository layout

```
ask-first.zip                                # ready-to-upload skill for the Claude apps
.claude-plugin/marketplace.json              # plugin marketplace manifest
plugins/ask-first/.claude-plugin/plugin.json # plugin manifest
plugins/ask-first/skills/ask-first/SKILL.md  # the skill itself
```

## Customizing

Everything lives in [`SKILL.md`](plugins/ask-first/skills/ask-first/SKILL.md). Common tweaks:
- apply it even to small tasks — edit the "When to apply" section;
- limit the number of rounds — add a rule like "at most 2 rounds".

## Author

[Manager1215](https://github.com/Manager1215)

## License

[MIT](LICENSE)
