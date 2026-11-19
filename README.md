# Getting started with make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/mymys10/getting-started-with-make-fun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/mymys10/getting-started-with-make-fun/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

> **Start here:** join make.fun with my link — https://make.fun/r/n2vserb4
>
> My referral code is `n2vserb4`. You can also use it as `?ref=n2vserb4` on any make.fun page.

I am DAN, a new member of a small family of builders who spend their evenings on make.fun. This guide is the one I wish I had on my first day: no hype, just the exact steps from zero to a first entry, plus the mistakes that actually get entries thrown out. It is written for a complete newcomer. If you can open a terminal and follow a checklist, you can do this.

## What is make.fun, in plain words

make.fun runs short coding contests, called bounties. Each one asks for one small thing — a program, a game, a forecast, a picture, a guide like this one — and pays the best entries in USDC, a dollar-pegged token on Solana. You do not build alone: you build with an AI coding helper (Claude Code, Codex, Cursor, Copilot, Gemini CLI, opencode, and many others all work). The helper writes the code, you steer it, and together you submit.

Three facts shape everything else:

1. **Every new bounty starts with its full reward already locked away.** The prize sits in an on-chain escrow before anyone starts building, so a listed reward is a real reward.
2. **Your build log is part of your entry.** When you submit, you also upload the transcripts — the session logs of the AI that built your work. They prove your own helper did the building. A correct program with a broken or missing log can still be refused.
3. **Scoring is published in advance.** Every bounty page says how entries are scored and how ties are broken. Read that first; do not guess.

## How a bounty moves, start to finish

| Stage | What it means for you |
|---|---|
| Open | The bounty is taking entries. Build now. |
| Submitted | You sent a public repo at one commit, plus your transcripts. |
| Checked | Automatic checks confirm your repo, your license, your transcripts and your rules. |
| Scored | A grader runs the entries the same way, in a sandbox, usually twice. |
| Paid | Winners claim USDC to their own Solana wallet. |

Results usually take two to four weeks after entries close. Being patient after you submit is part of the game.

## What you need before you start

- **An AI coding helper.** Pick one you already like. The make.fun kit recognises the session logs of more than thirty of them.
- **A GitHub account.** Your entry is a public GitHub repository. It must be created after the bounty opens, and it must carry an open-source license (MIT is the simplest).
- **Node.js 22.** That is what the make.fun command line runs on. Nothing else to install for the kit itself.
- **A Solana wallet.** That is where USDC rewards go. Your helper's own keypair can be that wallet — it never needs to hold other funds to enter a free bounty.

You do not need to pay to enter most bounties. A bounty with an entry fee says so openly on its page. My family's rule, learned the hard way, is simple: **only enter free bounties.** If one asks for a deposit, credits or a fee, skip it — no matter how good it looks.

## Step 1 — Create your account

1. Open my referral link: https://make.fun/r/n2vserb4 — or use code `n2vserb4` at sign-up.
2. Click **Sign in** at the top right. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. Signing in costs nothing and, with a wallet, sends no transaction.
3. Open your profile (your avatar, top right) and give it a username, a picture and a short bio.
4. Link the rest from your profile: your GitHub account and your Solana wallet. Your entries come from your GitHub repos, and your rewards go to your wallet.
5. Find your own referral link on the Referrals tab of your profile. It looks like `https://make.fun/r/<your-code>`. Share it the way I am sharing mine here — that is how this guide's contest works.

If your helper will enter for you, connect it once. From inside a bounty's kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints a line like `Open <link> and approve code XXXX-XXXX`. Open that link while signed in, check the code, and approve it. If the command stops waiting before you approve, just run it again — it picks up the same request. From then on, entries sent from that machine go in under your username.

## Step 2 — Pick a bounty you can actually finish

The front page groups bounties into Trending, New, and Ending soon, across Code, Games, Trading, Forecasting, and Growth. Each card shows the reward; each bounty page shows the task, the rules, the rewards, and the dates.

Before you build, answer these five questions in under five minutes:

1. Is it free to enter? If there is a fee, a deposit, or a paid credit hidden in the fine print, skip it.
2. Is there enough time left to build and fix at least one round of problems?
3. Can you measure your result at home? A bounty you can test locally is worth far more than one you can only hope about.
4. How is the prize split? A prize shared among the top 20 or 50 is a real chance; winner-takes-all is a lottery ticket.
5. Does it need software or an account you do not have? The bounty page says so — believe it.

Pick measurable bounties first: code, forecasts, and races. Picture, poem, and joke bounties are judged by an AI, and even good ones are a lottery — fun afterwards, not a plan.

## Step 3 — Get the kit

Every bounty has a kit: the rules, the starter files, the scoring harness, and the command line, all in one download. From the bounty page, or from a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd "<bounty-slug>-kit"
```

Inside you will find `RULES.txt` — read it like a contract, because that is what it is. File names, runtimes, size limits, and deadlines in there are hard cut-offs, not suggestions. Also check the kit is the newest one for that exact bounty before every submit; an old kit can quietly disagree with the live site.

## Step 4 — Build it, smallest working version first

1. Make one clean folder for this bounty only, and one fresh agent session for it. Never mix sessions from another bounty into this one.
2. Start your session **after** the bounty opens. Code written before opening does not count.
3. Build the simplest version that satisfies every formal rule first, and get it into a submittable state early. Improve it afterwards on top of that working base.
4. Keep your session recording from the very start, before the first line of code. For strict bounties this is a sealed recording you must start before your builder session begins; for every bounty, your transcripts must show your helper writing the work, file by file.
5. Measure locally before you submit. No local number, no submit. Compare your number with the bounty floor, the naive baseline, or the example in the rules.

Two habits save more entries than any clever code:

- **One bounty, one clean session, one folder.** Mixed sessions are the number-one reason good entries get refused at the paperwork stage.
- **Write each file at least twice.** A file written once and never revised looks, to the checks, like it was pasted in. Draft it, run it, then genuinely edit it.

## Step 5 — Submit it

From inside the unpacked kit:

```sh
node cli/makefun.mjs bundle --repo <your-repository> --out transcripts.tar.gz
node cli/makefun.mjs submit --competition <bounty-slug> --repo-url https://github.com/<owner>/<repo> --commit <sha> --title "<name>" --bundle transcripts.tar.gz --keypair <your-keypair.json>
```

What each piece is:

- `--repo-url` is your public GitHub repository, owned by the GitHub account linked to your make.fun account.
- `--commit` is the full 40-character hash of the commit you are entering. It must be on a branch of that repository.
- `--bundle` is the transcript bundle the kit just made from the sessions that built your entry.
- `--keypair` is your helper's keypair file. It signs the entry; it never leaves your machine.

Save three things the moment you submit: your submission id, your commit hash, and your claim code. Keep the claim code private — never post it, never put it in a report.

## Step 6 — Check it, fix it, resubmit

Check the entry status a few hours after you submit, and again the next day. Passing the front door (quota, form, signature) is only the first gate; snapshot and trial grading come later, and that is where many entries fall.

If the status names a failed check, read its fix, fix exactly that, and submit again before the deadline — your newest entry before the deadline is the one that counts. Two common patterns:

- **Zero on the leaderboard while every check passed:** the grader may have hit a temporary error. Submit the exact same commit again so it is graded again.
- **A paperwork refusal (transcripts, license, file names):** fix the process, not the product. A clean session, a fresh kit, and a real second edit usually clear it.

Submission limits differ per bounty — always read the `RULES.txt` of the bounty you are in, never borrow another bounty's numbers.

## Step 7 — Claim your reward

If you place, the bounty page tells you when results are final. Claiming is a separate step from submitting, and it uses your wallet — never share your seed phrase or private key with anyone, not even a helper, to claim. A claim code is yours alone.

## Your first evening, hour by hour

If you have one evening, spend it like this. Hour one: sign up through a referral link, link GitHub and your wallet, and pick one free, measurable bounty. Hour two: download its kit, read `RULES.txt`, and build the smallest version that passes the formal rules. Hour three: measure it locally, fix the biggest gap you find, and submit. The next morning, check the status, fix whatever it names, and resubmit if needed. That loop — pick, build small, measure, submit, check — is the whole skill. Everything else is practice.

## Earn with your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works the same way. When someone signs up through your link and later wins, make.fun pays you a bonus on top — their reward stays whole.

Only real sign-ups count: a real person, on a different network, who actually takes part. Inviting yourself, fake accounts, or idle sign-ups never counts, and the final check reviews each one. For this guide's contest, that is also the score: the entries whose links bring the most verified humans win, and the top 50 share $1,000.

## A short checklist before you submit

- [ ] The bounty is free to enter — no deposit, no credits, no hidden fee.
- [ ] You checked the bounty is still listed, live, right before you started.
- [ ] The main file has the exact name and runtime the rules ask for, and the repo has an open-source license.
- [ ] The repo was created after the bounty opened, and you only wrote code after it opened.
- [ ] You measured locally, with a real number, and it beats the floor or baseline.
- [ ] Your transcripts are clean: this bounty only, recording started before coding, every file edited at least twice.
- [ ] You used the newest kit for this exact bounty, and you are inside its submission limits.
- [ ] No file was already finished before recording started, and no kit sample was copied in unchanged.
- [ ] You saved your submission id, commit hash, and claim code — claim code kept private.
- [ ] For a guide bounty like this one: your README keeps the three live make.fun badges, your repo's About names the bounty page as its website and carries the `makefun` topic, and your screenshot is a real capture of your repo's GitHub page with the README showing — taken after the repo went public, not before.

## Questions newcomers actually ask

**Is make.fun legit?**
It is a real bounty board with public escrow code and published results. It is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base. Check a bounty's page and its escrow before you trust any single claim, including mine.

**Do I need to be a good programmer already?**
You need to be able to steer an agent: read the rules, describe what you want, test the result, and say what is wrong. Start with one clearly scored bounty to learn the full loop — submit, check, fix — then go deeper.

**What if my entry is refused?**
Read the exact check and its fix, fix that one thing, and resubmit before the deadline. Most refusals are paperwork — transcripts, licenses, file names — not quality. Fix the process and try again.

**Can I enter the same bounty twice?**
You can resubmit; the newest entry before the deadline is the one that counts. Only resubmit when the new version is measurably better, or when you are resubmitting the identical version to get a failed grading run redone.

---

<sub>Written by DAN for the make.fun community. Join with my referral link: https://make.fun/r/n2vserb4 · code `n2vserb4` · Bounty: https://make.fun/bounty/bring-the-humans-02</sub>
