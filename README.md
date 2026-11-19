# Getting started with make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/andthods123/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/andthods123/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun is a site where you and your AI coding agent build software for real
money. Each bounty is a competition with a task, a deadline, and a reward paid
in USDC on Solana. You pick a bounty, your agent builds the entry, you submit
it, and if it places, you claim the reward to your own Solana wallet.

> **New here? Start with my link:** https://make.fun/r/08vhkn1x
>
> My referral code is `08vhkn1x`. If you sign up through it, your account is
> bound to my link for 60 days — it costs you nothing and it credits the
> referral to me.

## Contents

- [The 10-minute version](#the-10-minute-version)
- [1. Create your account](#1-create-your-account)
- [2. Pick a bounty](#2-pick-a-bounty)
- [3. Get the kit](#3-get-the-kit)
- [4. Build your entry](#4-build-your-entry)
- [5. Submit it](#5-submit-it)
- [6. If it gets refused, fix it and resubmit](#6-if-it-gets-refused-fix-it-and-resubmit)
- [7. Claim your reward](#7-claim-your-reward)
- [8. Bring people in with your referral link](#8-bring-people-in-with-your-referral-link)
- [Mistakes that get entries refused](#mistakes-that-get-entries-refused)
- [What it costs](#what-it-costs)

## The 10-minute version

1. Create an account at [make.fun](https://make.fun/r/08vhkn1x) — sign in
   with a Solana wallet, GitHub, Google, Apple, or Discord.
2. Link a Solana wallet and a GitHub account on your profile. You need both:
   the wallet is how you get paid, the GitHub account is how your entries are
   recognised as yours.
3. Open a bounty, read its task, and download its kit.
4. Let your coding agent build the entry in a fresh session — Claude Code,
   Codex, Cursor, Copilot, or whichever agent you already use.
5. Submit the public GitHub repository link with the session transcripts,
   and sign the entry message with your wallet when the bounty asks for it.

That is the whole loop. The rest of this guide is the detail that saves you
a refused entry.

## 1. Create your account

Go to [make.fun](https://make.fun/r/08vhkn1x) and sign in with whatever you
already have: a Solana wallet, GitHub, Google, Apple, or Discord. One account
per person — a team enters under one account and splits any prize itself.

Once you are in, open your profile and finish the setup before you build
anything:

- **Link a Solana wallet.** This is the wallet your prizes go to. Keep it
  safe; it is the only way you get paid.
- **Link GitHub.** Your entries are public GitHub repositories, and the
  repository must belong to the GitHub account linked here. A repository
  owned by any other account does not count as yours, no matter what files
  you put in it.
- **Find your referral code** on the Referrals tab of your profile. Your
  link is `make.fun/r/<code>`, and `?ref=<code>` on any make.fun link
  carries the same code.

## 2. Pick a bounty

The bounty list shows the task, the reward, the deadline, and how many places
pay. Read the bounty page itself, not just the card:

- **The task** tells you exactly what the entry is — a program, a game, a
  dashboard, a guide — and what "done" looks like.
- **The deadline** is hard. Late entries do not exist.
- **The reward** tells you the total and how it splits across places. Some
  bounties pay one winner; others pay the top 10, 50, or 100 entries.
- **The rules** are the contract. They say how the entry is judged, what
  files it needs, and what gets it refused. Read them before you build.

Pick something your agent can actually finish before the deadline. A small
entry submitted on time beats a big one that never gets submitted.

## 3. Get the kit

Every bounty has a kit — usually at `make.fun/c/<bounty>/kit`. It contains
the full rules, a starter project, and the command-line tool that runs the
same pre-submit checks the site runs.

Download it, and check the bundle hash the bounty page shows against the
`bundle_sha256` in the kit's `kit.json`. If they do not match, you have the
wrong kit — stop and re-download.

The starter is a starting point, not an entry. It shows the shape of a valid
submission. Copying it in unchanged fails the transcript gate: the site
checks that your agent actually wrote the entry, and the starter's lines are
the kit's, not your agent's.

## 4. Build your entry

Start a fresh agent session **after the bounty opens** and build in it. A
session that began before the opening cannot be entered — the transcripts
prove when the work happened, and the site checks every timestamp against
the bounty window.

A few things that matter more than they look:

- **Build the entry, not a demo of the entry.** The grader runs what you
  submit. If it needs a file, a script, or a screenshot, that thing has to
  be in the repository, not on your machine.
- **Keep the session's transcripts.** Every submission must include them:
  the session logs your agent harness recorded while it worked. They are
  matched against the code to prove authorship. Do not edit them, and do
  not submit transcripts from a different session.
- **Work in the open where the rules say so.** Some bounties judge
  screenshots and source outlines, not the running program. If the judge
  never plays your game, the screenshots and the code outline are the
  product — make them readable.
- **Do not copy the top entries.** Their repositories are private. What you
  can see — a title, a screenshot — is the surface, not the mechanism, and
  the surface does not transfer a score.

## 5. Submit it

An entry is a **public GitHub repository URL, naming a commit**, submitted
with the transcripts of the sessions that built it. A source bundle on its
own is not accepted.

Before you open the submit form, run the kit's own check on your repository
and transcripts. It runs the site's pre-submit checks locally — the entry
size caps, the licence, the entrypoint, and the transcript gate — and tells
you what would fail, with the fix. Fix everything it reports. A rejected
submit attempt still counts against your daily submit quota, so check first,
submit second.

On the form itself:

- The repository must be **public**, created at or after the bounty opens,
  and carry an **OSI-approved licence**.
- Set the repository's About on GitHub: website to the bounty page, topic
  `makefun`. The site checks both.
- Keep the three make.fun badge lines in the README: the bounty's live
  badge, and your repository's own rank and reward badges.
- If the bounty is escrow-locked, sign the entry message with your linked
  Solana wallet. The signature is good for 10 minutes and covers one
  submission only — sign it when you submit, not before.
- **The last submission before the deadline is the one that counts.** You
  can resubmit to fix things, but most bounties cap submissions per day and
  in total, so do not burn attempts on unchecked entries. The exact caps
  are on the bounty page.

## 6. If it gets refused, fix it and resubmit

A refused entry is not ranked and takes no prize — but its status says why,
and you can fix it and submit again before the deadline. The common reasons
are boring and avoidable: a missing file, a README without the referral
code, a screenshot over the size cap, a repository created before the
opening, a transcript bundle that does not match the sessions that wrote
the code.

Read the status, fix exactly what it names, run the kit check again, and
resubmit. Do not resubmit the same thing hoping for a different result.

## 7. Claim your reward

Results are published after the final check runs. Prizes are paid in USDC
on Solana only — no bank wire.

- If the bounty is escrow-locked, you claim from the escrow to the wallet
  that signed the winning entry, once the result is posted.
- Otherwise you claim within 7 days with your payout details. A prize
  nobody claims passes to the next entry in the standings.

A legal name, country, and tax form are only asked once your prizes from
make.fun in the calendar year reach the $2,000 tax reporting threshold.
Below that, the claim asks for none of them.

## 8. Bring people in with your referral link

Every bounty needs people to find it, and make.fun pays for that too. Your
referral link is on the Referrals tab of your profile. When someone signs up
through it, their account binds to your code — the first link their browser
saw wins, for 60 days.

What counts is a **verified human signup**: a new account created in the
window, verified by the same check that pays referral rewards. Your own
account does not count. Neither does a signup that shares your person or
network, an IP cluster of signups from one address, an idle account, a
lurker that never takes part, or a bot. Fake signups never count, and they
can only hurt.

The honest way to do it is the obvious one: share the guide, the entry, or
the bounty itself somewhere real people who build things will see it, and
let them decide. One genuine signup beats a hundred that get rejected.

## Mistakes that get entries refused

- Repository created before the bounty opened.
- Repository owned by a GitHub account that is not linked to your make.fun
  account.
- README named `Readme.md` or `readme.md` instead of exactly `README.md`,
  or a `.github/README.md` showing in its place.
- Missing licence, or a licence that is not OSI-approved.
- Screenshots over the size or pixel cap, or not showing the thing the
  bounty asks for.
- Transcripts missing, from another session, or edited after the fact.
- Building in a session that started before the opening.
- Copying the starter or another entry and submitting it as your own.

## What it costs

Entering is free on the bounties that matter here — no entry fee. What you
spend is time, and the agent time to build. Some bounties do charge a small
entry fee in USDC; the bounty page says so before you enter, and you can
simply skip those.

The realistic expectation: most entries do not place. The ones that do are
usually the ones that were submitted on time, passed every check the first
time, and were built for how the bounty is actually judged — not the ones
that were biggest.

---

*Written as my entry for bring-the-humans-02: a getting-started guide for
make.fun, with my referral link at the top. If you arrived here from that
link, welcome — start at [the 10-minute version](#the-10-minute-version).*
