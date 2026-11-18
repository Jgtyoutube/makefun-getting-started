# AGENTS.md

Instructions for any AI agent working in this repository.

## What this repository is

A single-file guide: `README.md` at the root is a getting-started tutorial for make.fun, written for a person who has
never entered a bounty. `LICENSE` is MIT. There is no build, no test suite and no code to run — the deliverable is
prose that has to be true.

## Rules for editing it

- **Keep `README.md` at the root, named exactly so.** A `.github/README.md` would take its place on GitHub's
  repository page and is not allowed.
- **Keep the three badge lines at the top, unchanged in form.** The first line is the bounty badge, the second and
  third are this repository's own rank and reward badges:

  ```md
  [![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
  [![rank](https://make.fun/badge/bring-the-humans-02/{owner}/{repo}/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
  [![reward](https://make.fun/badge/bring-the-humans-02/{owner}/{repo}/reward.svg)](https://make.fun/bounty/bring-the-humans-02)
  ```

  `{owner}` and `{repo}` are the only placeholders allowed in the file. **Replace both with this repository's GitHub
  owner and name before submitting anywhere that reads the badges** — an entry whose README keeps a template
  placeholder in a badge URL fails the `repo_readme` check. Do not wrap a badge in an HTML comment or a code block,
  and do not swap a live make.fun badge for a static shields.io one.
- **Keep one make.fun link and the referral link.** The footer carries `https://make.fun/r/27950n3s` (code
  `27950n3s`). The README must always name the referral code: the bare code, `/r/<code>` or `?ref=<code>`.
- **Everything in `README.md` must be true and verifiable.** Facts about make.fun come from its own docs, not from
  memory: [skill.md](https://make.fun/skill.md) (the whole agent loop), [llms.txt](https://make.fun/llms.txt),
  [how-it-works](https://make.fun/how-it-works), the guides, and a bounty's own kit (`RULES.txt`,
  `competition.yaml`). When a command or flag changes, re-check it against the kit CLI's `--help` output before
  editing the guide.
- **Keep commands copy-pasteable and exact**: real flags, real paths, real endpoints. No invented subcommands, no
  invented API routes, no version numbers you have not checked.
- **Do not commit secrets.** No keypairs, no API keys, no `.env` files, no tokens. Transcripts and personal details
  belong in the entry bundle, never in this repository.
- **Do not add a screenshot of this repository unless the bounty's deliverables ask for one.** Where they do, it goes
  at the root as `screenshot.png`, a PNG/JPEG/WebP under the size and pixel caps in the rules, showing the GitHub
  repository page with this README rendered — taken once the repository is public.
- Keep the tone of the existing guide: plain, step-by-step, second person, no marketing padding. Short paragraphs,
  numbered steps, real commands in fenced blocks.

## Writing a guide for a bounty, not just for readers

Where this repository is entered into a make.fun bounty, the entry is this guide plus the AI transcripts of the
sessions that wrote it. That means:

- Start the agent session at or after the bounty's opening time. A session that began earlier cannot be entered.
- Author the file in the session: at least one line of `README.md` must be a line the agent wrote, and the transcript
  gate wants the file written or edited in at least two assistant messages. Editing by hand is allowed but lowers the
  authored share; a starter README copied in unchanged fails the gate.
- Bundle the transcripts with the kit's CLI (`node cli/makefun.mjs bundle --repo .`) and run `check` before submitting.
  Both need the run record complete: the person's opening prompt, harness and version, provider, model, effort, system
  prompt and instruction files.

## Before you push

1. `README.md` at the root, no `.github/README.md`.
2. No `{owner}` / `{repo}` left in the badge URLs, and both resolve to this repository.
3. The referral code appears in the text, and the footer referral link is intact.
4. Commands and flags match make.fun's current docs and the kit CLI's `--help`.
5. No secrets, keys, or personal details of anyone in any file.
