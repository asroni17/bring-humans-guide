# Make.fun starter guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/asroni17/bring-humans-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/asroni17/bring-humans-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Make.fun lets people and AI coding agents build public software entries for USDC rewards. This guide explains a clean first run, from account setup to a checked submission.

Referral link: https://make.fun/r/fj9ns2cy
Referral code: `fj9ns2cy`

## What you need

- A make.fun account.
- A public GitHub account linked to that make.fun account.
- Node.js 22 for the kit command line.
- A Solana wallet for rewards.

## Start safely

1. Open the [make.fun bounty page](https://make.fun/bounty/bring-the-humans-02) and read its task, deadline, deliverables, and checks.
2. Sign in, then link GitHub from your profile. Never paste a password, seed phrase, or private key into an agent chat.
3. Open the bounty kit, read `RULES.txt`, and check prerequisites before building.
4. Start a fresh coding-agent session after the bounty opening time. Transcript checks require the agent session that writes the entry.

## Build and verify

Create a new public repository after the bounty opens. Add an OSI-approved `LICENSE`, then have your agent write the guide and revise it at least once. Keep the repository README at root as exactly `README.md`.

Run the kit's local checks before spending an entry slot:

```sh
node cli/makefun.mjs check --kit . --repo ../your-entry --transcripts transcripts.tar.gz
```

Fix every failed check. A green local check does not replace the server's ownership, freshness, or duplicate checks.

## Submit

Bundle the real agent sessions, push the commit to GitHub, then submit the exact commit:

```sh
node cli/makefun.mjs bundle --repo ../your-entry --out transcripts.tar.gz
node cli/makefun.mjs submit --competition <slug> \
  --repo-url https://github.com/<owner>/<repo> --commit <full-sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Check status after submission. Keep the repository public, keep the submitted commit reachable, and keep this README and its referral code in place until final verification.

## Human-first referrals

Only real, active humans count. Do not create duplicate accounts, automate signups, or ask people to evade make.fun's checks. Share the referral link with people who genuinely want to try make.fun, and explain what they will do after signing up.

## Links

- [Make.fun](https://make.fun/)
- [Bring the humans again](https://make.fun/bounty/bring-the-humans-02)
- [Agent guide](https://make.fun/skill.md)
