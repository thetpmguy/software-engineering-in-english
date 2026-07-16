# 🔧 Lab 14 — Your Personal Security Audit

> **Goal:** not a simulation this time. By the end of this lab, your real accounts
> will be genuinely harder to break into than they were an hour ago. Work through
> the checkboxes in order — each one closes a door from the lesson.
>
> **Time:** 60–90 minutes. Item 5 can run overnight.

Print this page or keep it open, and tick the boxes as you go:

- [ ] 1. Checked my email for breaches
- [ ] 2. Turned on 2FA for my most important account
- [ ] 3. Set up a password manager (or fixed my top 3 passwords)
- [ ] 4. Passed a phishing-spotting quiz
- [ ] 5. Ran all pending updates

---

## 🔍 Step 1 — Have you been in a breach?

1. Go to **[haveibeenpwned.com](https://haveibeenpwned.com)**.
2. Type your email address and press the button.

**Wait — is it safe to type my email into a random site?** Fair question; you've
been paying attention. This one, yes: it's a famous, long-running free service made
by a respected security professional, is recommended by governments and
password-manager companies, and asks only for your email address — a thing that's
already semi-public (everyone you've ever emailed has it). It never asks for a
password. The general rule stands — be suspicious — and this is a vetted exception.

3. Read your results. Each entry is a company that suffered a breach *while holding
   your data*, with a list of what leaked.

**✅ What you should see:** most email addresses that have lived a few years appear
in several breaches — the average is well above zero, so don't panic. **Act:** for
every breached site where you still remember the password — and *especially* if you
reused it anywhere — that password's turn comes in Step 3. If it guarded your email
or bank, fix it today, first.

## 🔑 Step 2 — Turn on 2FA where it hurts most

Protect your single most important account first. For most people that's their
**email** — because "reset password" links for everything else land there. Google
steps below; other providers are near-identical.

1. Go to your Google Account (myaccount.google.com) → **Security**.
2. Find **2-Step Verification** and click **Turn on**.
3. Follow the prompts — you'll confirm your phone. Prefer the **authenticator app**
   or the "prompt on your phone" option over SMS if offered (the lesson's one-line
   reason: phone numbers can be hijacked; apps can't be, from afar).
4. **Save the backup codes** it offers you — print them or write them down, and
   store them where you keep passports. They're your spare key if the phone is
   lost.

**✅ What you should see:** logging in on a new device now demands your password
*and* your phone. A password thief on another continent now holds half a key.

## 🗄️ Step 3 — The vault (or at least the three big doors)

**Preferred: set up a password manager.**

1. Pick one: your browser's built-in manager (already on your device, free, fine)
   or a dedicated app — Bitwarden is a well-regarded free option; 1Password is a
   popular paid one.
2. Create your **master passphrase** using the lesson's rule — length beats
   cleverness: four or more random common words, like `staple garden thunder
   biscuit`. Write it down on paper and store it with your passports until it's
   memorized. (Paper at home beats weak-but-memorable — burglars trying a billion
   passwords per second aren't in your kitchen drawer.)
3. Change your three most important passwords — email, bank, main social — letting
   the manager *generate* long random ones. You'll never type them; the vault
   fills them in.

**Minimum version (no manager today):** change those same three passwords by hand
to long passphrases — four random words each, a *different* four for each account.
Reuse is the killer; three doors, three different keys.

**✅ What you should see:** your three most valuable accounts now have long, unique
keys — and if you chose the manager, adding every other account is now a
when-you-touch-it habit, not a project.

## 🎣 Step 4 — Can you spot the fake bank branch?

1. Go to **[phishingquiz.withgoogle.com](https://phishingquiz.withgoogle.com)** —
   a free quiz by Google that shows you realistic emails, some genuine, some
   phishing. (Use a made-up name and email when it asks — it's for the examples.)
2. For each message, decide: legitimate or phishing? Use the lesson's three tells —
   **urgency**, **links** (hover or long-press to reveal the true address),
   **sender** (almost-right is wrong).
3. Read every explanation, especially for the ones you get wrong — those are the
   exact tricks currently in the wild.

**✅ What you should see:** most people miss at least one — the fakes are *good*.
The takeaway habit beats any score: never log in through a link that came to you.
Go to the site yourself, every time.

## 🩹 Step 5 — Update everything night

The lesson's point made real: patches fix holes that burglars already have the memo
about. Tonight:

1. **Phone:** Settings → check for system updates → install. Then update all apps
   (App Store / Play Store → update all). Turn ON automatic updates while you're
   there.
2. **Computer:** Windows Update / Software Update (Mac) → install everything →
   restart — actually restart, tonight, not "later".
3. **Browser:** menu → Help/About → it updates as the page opens.
4. **The forgotten one:** your router. If Lab 13's safari found a firmware-update
   button on the admin page, run it — routers are the most neglected devices in
   the house.

**✅ What you should see:** every device restarted, zero pending updates, automatic
updates on. Every published hole in your home: patched.

---

## 🎉 Done — and this one actually counts

Look at your checklist: breach awareness, a second lock on the most important door,
long unique keys, trained phishing eyes, and zero known-broken locks. That is
genuinely more than most people ever do, and you understood the *why* of every
step. One suggestion: put a yearly reminder in your calendar to re-run this lab —
security is a habit, not an event. Then, on to the [quiz](quiz.md).
