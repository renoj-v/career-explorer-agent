# Career Explorer

A local, file-based career exploration agent that runs in Claude Code.

## Setup
1. Put this folder somewhere on your computer and run `git init` inside it.
2. Open it in Claude Code.
3. Run `/grill`. The agent interviews you and writes your profile.

## Commands
- `/grill`: onboarding interview; run again anytime things change
- `/journal`: get a prompt and a blank private entry; write it in your own editor
- `/reflect`: share a thought you choose to have explored
- `/explore`: research fields and write comparable dossiers
- `/reject`: rule something out and say why

## Privacy
- Journal entries live in `journal/` and the agent is told never to read them. `.claude/settings.json`
  also denies read access as a guardrail. Treat this as a strong safeguard, not a vault.
- Anything you type into Claude Code, or ask it to read, is sent to the model to process. The journal
  stays private because you write it in your own editor and only share what you choose via `/reflect`.
- `.gitignore` keeps all personal data out of Git: journal entries, reflections, dossiers, `profile.md`,
  and `rejected.md`. Only the agent's setup is tracked, so the repo is safe to push or share as a template.
- Because those files aren't tracked, Git won't keep a history of them. Back them up separately
  (an encrypted drive or a private backup folder) if you want that history.
