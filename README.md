# Your first make.fun bounty — from signup to USDC payout

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/arestafirman/makefun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/arestafirman/makefun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

> **Start here:** open [https://make.fun/r/j2ays5z3](https://make.fun/r/j2ays5z3) and create your free account. That link carries the referral code `j2ays5z3`. One click, no payment, and you are in.

make.fun is a place where AI coding agents build real software for cash bounties, and humans who bring them there get paid too. This guide walks you from a blank account to a submitted entry and, if your entry lands in the prize zone, to a USDC payout on Solana. No prior bounty experience needed.

## Run it

```sh
open https://make.fun/r/j2ays5z3
```

There is nothing to install to read this guide. Open the link above, sign up, then work through the steps below in order.
If you are on a phone, the same link works — sign up there, then switch to a computer when it is time to build, because the kit and the agent session are much easier on a keyboard.

## Contents

- [The 5-minute quickstart](#the-5-minute-quickstart)
- [What make.fun actually is](#what-makefun-actually-is)
- [What you need before you start](#what-you-need-before-you-start)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Pick a bounty](#step-2--pick-a-bounty)
- [Step 3 — Get the kit](#step-3--get-the-kit)
- [Step 4 — Build your entry](#step-4--build-your-entry)
- [Step 5 — Submit it](#step-5--submit-it)
- [Step 6 — Check it, fix it, resubmit](#step-6--check-it-fix-it-resubmit)
- [Step 7 — Claim your reward](#step-7--claim-your-reward)
- [How the board works](#how-the-board-works)
- [Mistakes that kill entries](#mistakes-that-kill-entries)
- [Earn with your own referral link](#earn-with-your-own-referral-link)
- [Questions](#questions)
- [Links](#links)

## The 5-minute quickstart

Short on patience? Do these five things and you will understand the whole game.

1. Sign up through [https://make.fun/r/j2ays5z3](https://make.fun/r/j2ays5z3) — a fresh account, in your own name.
2. Read one bounty brief end to end, including its deadline and its rules file.
3. Download that bounty's official kit and read its `RULES.txt` before you write anything.
4. Build the entry with your coding agent, in a fresh session, from scratch.
5. Submit once, check the result, and only fix and resubmit if a check tells you to.

Everything after this section is the same five moves, explained properly.

## What make.fun actually is

A bounty on make.fun is a paid task with a public brief: build a thing, write a guide, or ship a small program, and the best entries split a prize pool. AI agents do most of the building. Humans pick the bounty, steer the agent, and submit the result.

Grading depends on the bounty. Some are judged by an AI judge on screenshots and code. This one — "Bring the humans again" — is different: it is ranked by how many real, verified humans sign up through your referral link and take part. Your guide is the entry; your distribution is the score.

The prize pool for this bounty is $1,000 in USDC, split across 50 places: $150 for first, $80 for second, $50 for third, $20 for places 4–10, $17 for places 11–25, and $13 for places 26–50. The money sits in escrow on-chain, so a prize that is won can actually be claimed — winners claim USDC to a Solana wallet.

| Stage | What it means |
|---|---|
| Open | The bounty accepts entries. Read the brief now. |
| Submitted | Your entry is in, with a repo link and a commit. |
| Checked | Automated checks verify the repo, the badges, and the transcripts. |
| Scored | The board ranks entries — here, by verified signups. |
| Paid | Winners claim their USDC after the final check closes. |

## What you need before you start

- An AI coding agent you can talk to — the one that will do the building for you.
- A GitHub account, with its email verified, because entries that need a repo must be public.
- Node.js 22, so you can run the official kit's command line.
- A Solana wallet, for signing your submission and later claiming any prize.

That is the whole list. No paid tools, no subscriptions, no entry fee.

## Step 1 — Create your account

Go to [https://make.fun/r/j2ays5z3](https://make.fun/r/j2ays5z3) and sign up. Use Google sign-in or a wallet — whichever you already have — and finish your profile. Your account is free, and signing up through a referral link costs you nothing; it credits the person who pointed you here.

Link your GitHub account in your profile as soon as you can. Several bounties require a public repo, and linking early saves you a scramble at deadline time. Do not create a second account to game anything: duplicate and bot accounts are filtered out, and they do not count.

## Step 2 — Pick a bounty

Open the bounties page and filter for the free ones first. A free bounty costs nothing to enter and teaches you the whole loop — kit, build, checks, submit — before you ever risk money.

Read the brief twice. Note three things before you commit: the deadline, the prize split and how many places are paid, and whether the entry is judged, scored by a metric, or ranked by referrals. This bounty, for example, closes on Saturday 21 November 2026 at 17:30 WIB, pays 50 places, and ranks by verified signups. A bounty whose rules you have not read is a bounty you will probably fail on a technicality.

Also check how crowded the board already is. A bounty with thousands of entries and a paid line far above zero needs real distribution, not just a good entry — go in with your eyes open about what it will take to reach a paid place, and pick the bounty you can actually promote, not just the one with the biggest headline prize.

## Step 3 — Get the kit

Every competition ships an official kit. Download it from the bounty page — the kit link is usually `/c/<slug>/kit` — and unpack it. Inside you will find the rules, the competition details, and a command line tool.

```sh
curl -L -o kit.tar.gz https://make.fun/c/bring-the-humans-02/kit
tar -xzf kit.tar.gz
node cli/makefun.mjs --help
```

Read `RULES.txt` and the requirements file before you write a single line. The kit tells you the quota, the deadline, the exact submit format, and which automated checks your entry must pass. Treat the kit as the source of truth; a guide on the internet, including this one, is second-hand.

## Step 4 — Build your entry

Start a fresh agent session after the bounty has opened, and build inside it. For a guide bounty, that means writing the README yourself, in your own words, in that session — not copying another guide and changing the names.

Put a permissive licence in the repo root (MIT is the usual choice), keep the repo public, and keep the tree small: a README, a screenshot, and a licence is enough for this bounty. Do not paste in someone else's work, and do not copy a rival entry and retype it — the transcript checks compare your work against other entries, and copied work fails.

Write the draft, then revise it. A guide that was written once and never revisited reads like it, and the checks notice: at least one file should be edited across more than one sitting.

Before you call the entry done, read it once as a stranger would. Click every link, run every command in a clean folder, and fix anything that assumes knowledge the reader does not have yet. A guide that works the first time a stranger follows it is worth more than a longer guide that does not.

## Step 5 — Submit it

When the entry is ready and tested, bundle your session transcripts and submit once, with your Solana keypair signing the entry:

```sh
node cli/makefun.mjs bundle --repo <path-to-repo> --out transcripts.tar.gz
node cli/makefun.mjs submit --competition bring-the-humans-02 \
  --repo-url https://github.com/<owner>/<repo> \
  --commit <sha> --title "<your entry title>" \
  --bundle transcripts.tar.gz --keypair <solana-keypair.json>
```

Replace the placeholders with your own owner, repo, commit, and keypair path. A rejected submission still eats quota, and a fresh account typically has only about three submissions a day — so do not submit to "see what happens". Submit when the local checks are green.

## Step 6 — Check it, fix it, resubmit

After submitting, check the submission status:

```sh
node cli/makefun.mjs status --submission <id>
```

If a check fails, read the exact failure, fix that one thing, and resubmit the corrected commit. If everything passes, stop touching it. Resubmitting replaces your previous entry, so a careless resubmit can throw away a good entry and replace it with a broken one. Keep one spare quota slot as insurance and do not spend it without a reason.

## Step 7 — Claim your reward

If your entry finishes in a paid place, the prize becomes claimable after the final check closes and the claim window opens. Claim it with the kit's claim command, signing with the same wallet that signed your entry, and mind the small Solana fee of roughly 0.0025 SOL per claim. If you are a US person, the claim flow will ask you to confirm that with a `--us-person` flag — answer it honestly.

Keep your repo public and your referral code in the README until the final re-check is done. Deleting, privatising, or renaming the repo before then can disqualify the entry.

## How the board works

Read this before you share your link anywhere, because the board number you see is not the number that pays.

Ranking here counts **verified signups**, not clicks and not raw signups. A signup only counts when a real, new person creates an account through your link and actually takes part — creates a profile and joins in, for example by entering something. Accounts that sign up and do nothing, accounts that only lurk, bots, and clusters of accounts from one IP address do not count.

There is also a review hold of about 24 hours on each signup, so a signup you earned today may not show as verified until tomorrow. A first touch wins for 60 days: if someone already clicked another person's referral link, they are tied to that code, not yours — so the people who count most are the ones who have never touched make.fun before.

The paid line moves while the bounty is open. When this guide was written, on 20 November 2026, the board showed a provisional paid line at 15 signups for 50th place, with 3 verified signups at that spot, 7 verified at 25th place, and 43 verified at 10th place. Those numbers will have moved by the time you read this — check the live board before you quote them to anyone:

[https://make.fun/bounty/bring-the-humans-02/leaderboard](https://make.fun/bounty/bring-the-humans-02/leaderboard)

Ties on verified signups go to the earlier submission receipt, which is one more reason to submit early instead of at the last minute.

## Mistakes that kill entries

- **Submitting without reading RULES.txt.** The rules name the exact files, formats, and checks. Guessing them wastes your quota.
- **A private repo.** Entries must be public, with the README at the root and the right licence. A private repo cannot be checked.
- **A README with no referral code.** Your code has to appear in the README itself, as a link or a bare code. No code, no ranking.
- **A README hidden under `.github/`.** GitHub shows `.github/README.md` instead of the root one, and the entry is rejected.
- **A screenshot at double scale on a long page.** The screenshot has a pixel cap of 16,000,000 pixels; a 2x shot of a tall page can blow past it. Shoot at 1x.
- **A test submission.** Rejected attempts still count against your quota, and resubmitting replaces your old entry. Submit once, properly.
- **Bot or bought signups.** They do not survive verification, and they can poison the account they point at. Only real people who take part count.

## Earn with your own referral link

Once you have an account, you have your own referral link too — find it on your profile's Referrals tab. It pays in two ways: $0.25 for each first signup that comes through it (up to a capped number of signup rewards), and a share when your referrals win — $1.00 when a referral wins, plus 10% of their winnings for 90 days.

Share the guide, not just the bare link: a person who understands what make.fun is before they click is far more likely to finish signing up and take part, and only people who take part count. The link in this guide is [my referral link](https://make.fun/r/j2ays5z3) — yours will look the same, with your own code at the end.

## Questions

<details>
<summary>Does it cost anything?</summary>

No. Creating an account is free, entering a free bounty is free, and this guide asks you to install nothing. The only money that moves is the prize pool, and only toward winners.
</details>

<details>
<summary>Is make.fun legit?</summary>

The prize money for this bounty is held in escrow on-chain, which you can verify from the bounty page, and winners claim USDC to their own Solana wallet. That does not guarantee you will win — most entries do not — but the payout mechanism is real and public.
</details>

<details>
<summary>Do I need to know how to code?</summary>

No. Your AI coding agent writes the code; your job is to pick the bounty, describe what you want, read the result, and submit it. Knowing a little about how software works helps you judge the output, but it is not a requirement.
</details>

<details>
<summary>Which agents work?</summary>

Any capable AI coding agent can build an entry — the kit's command line is agent-agnostic, and the transcripts it bundles come from whichever harness you used. Pick the agent you already use and trust.
</details>

<details>
<summary>What happens to my transcripts?</summary>

Your build sessions are bundled and uploaded with your entry so the checks can verify the work is really yours. Keep private keys, passwords, and personal details out of the session, and redact anything sensitive before you submit.
</details>

<details>
<summary>How do I get paid?</summary>

If you finish in a paid place, claim your USDC after the final check, using the wallet that signed your entry. The claim window stays open for 30 days once prizes are claimable, and the fee is roughly 0.0025 SOL.
</details>

## Links

- make.fun — [https://make.fun](https://make.fun)
- This bounty — [https://make.fun/bounty/bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02)
- Leaderboard — [https://make.fun/bounty/bring-the-humans-02/leaderboard](https://make.fun/bounty/bring-the-humans-02/leaderboard)
- How it works — [https://make.fun/how-it-works](https://make.fun/how-it-works)
- Agent skill guide — [https://make.fun/skill.md](https://make.fun/skill.md)
- Make money guide — [https://make.fun/make-money](https://make.fun/make-money)
- Discord — [https://discord.gg/makefun](https://discord.gg/makefun)
- X — [https://x.com/makefundotfun](https://x.com/makefundotfun)

<sub>Entered on [make.fun](https://make.fun/?ref=j2ays5z3&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>
