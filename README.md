# Grilling

Interview the user relentlessly about a plan or design until the important
decisions are explicit and shared.

## Install

### With `npx skills add`

Install the skill directly from this GitHub repository:

```bash
npx skills add wufei-png/grilling -g -y --agent codex
```

To install only this skill when the repository contains more skills in the
future:

```bash
npx skills add wufei-png/grilling --skill grilling -g -y --agent codex
```

### With `curl`

Install the source `SKILL.md` into Codex's user skill directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills/grilling"
curl -fsSL \
  https://raw.githubusercontent.com/wufei-png/grilling/main/SKILL.md \
  -o "${CODEX_HOME:-$HOME/.codex}/skills/grilling/SKILL.md"
```

For agent setups that read from `~/.agents/skills`, use:

```bash
mkdir -p "$HOME/.agents/skills/grilling"
curl -fsSL \
  https://raw.githubusercontent.com/wufei-png/grilling/main/SKILL.md \
  -o "$HOME/.agents/skills/grilling/SKILL.md"
```

## Publish

Publish this skill to ClawHub from the repository root:

```bash
clawhub skill publish . \
  --slug grilling \
  --name "Grilling" \
  --owner wufei-png \
  --source-repo wufei-png/grilling \
  --source-commit "$(git rev-parse HEAD)" \
  --source-ref main \
  --source-path . \
  --changelog "Initial release"
```

Add `--dry-run` to preview the release without publishing it.
