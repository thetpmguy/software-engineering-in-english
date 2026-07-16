# 🔐 Module 14 — Security: Locks, Keys & Digital Self-Defense

> **What you'll learn:** how attackers actually operate (less Hollywood, more
> burglars trying door handles), why password length beats cleverness, how
> encryption really works in three friendly analogies, the handful of scams behind
> most real-world damage, and what engineers do all day to keep you safe.
>
> **Why it matters:** this is the one module you can act on *today*. By the end of
> the lab, your real accounts will be measurably harder to break into than most
> people's. Not fear — self-defense skills.

---

## 🧠 Burglars, not master spies

Have you ever skipped a "change your password" prompt thinking, *"who would bother
hacking me?"* Here's the reframe this whole module rests on: **almost nobody is
targeting you personally — and that's exactly why you're at risk.**

Security is locks on doors. And most digital attackers aren't master lockpickers
studying *your* house. They're burglars walking down an infinite street, trying
every door handle by machine, millions per hour. They don't care whose door opens.
They care that *some* doors are unlocked — reused passwords, skipped updates, no
second lock. The good news follows directly: you don't need unpickable locks. You
need to not be the unlocked door. That's an afternoon of work, and it's this
module's lab.

## 🎫 Two questions at every door

Every secure system asks two different questions, and mixing them up causes real
confusion, so let's split them cleanly.

**Authentication** is proving *who you are*. There are only three kinds of proof:
something you **know** (a password), something you **have** (your phone), and
something you **are** (your fingerprint or face).

**Authorization** is what you're *allowed to do* once you're in.

> 🌉 **Analogy:** A hotel. At the front desk you show ID — that's authentication.
> The keycard you receive opens *your* room, the gym, and the pool — but not other
> guests' rooms and not the manager's office. That's authorization.
>
> **Where the analogy breaks down:** hotel staff might wave through a familiar
> face. Computers re-check the keycard at every single door, every single time —
> no familiarity, no exceptions.

Keep the pair in mind; the whole module hangs on it. Passwords and fingerprints are
about the front desk. "Why can't this app see my files?" is about the keycard.

## 🔑 Passwords: length beats cleverness

Which password is stronger: `P@ssw0rd1` or `purple tortoise umbrella daylight`?

Nearly everyone picks the first — it looks like what websites demand. The second is
*enormously* stronger, and here's why in plain words. Password-cracking machines try
guesses at absurd speed — **billions per second** — and they try the likely things
first: dictionary words, names, dates, and all the classic substitutions. Swapping
"a" for "@" is not clever to a machine; it's literally on page one of the guessing
playbook. `P@ssw0rd1` falls in minutes.

Now do the math in words for the second one. Each *additional character* multiplies
the number of possible passwords by dozens — every letter you add makes the guessing
job dozens of times bigger. A few extra characters means thousands of times more
work; going from 9 characters to 30 makes the pile of possibilities grow past
billions of billions of billions. At that size, "billions of guesses per second"
stops being scary: the machine needs longer than the universe has existed. A short,
"clever" password loses to a long, boring one every time. **Length beats
cleverness.** (This idea is affectionately known online as the "correct horse
battery staple" principle, after a famous comic — four random common words make a
passphrase you can remember and machines can't guess.)

### The real killer: reuse

Here's the part the movies never show. Attackers rarely *guess* your password —
they **reuse** it. Websites get breached; lists of emails and passwords leak and
get traded. Attackers then take those leaked pairs and try them on *everything
else* — your email, your bank, your socials — by machine, at scale. The polite
industry name is **credential stuffing**: trying keys stolen from one door on
thousands of other doors.

> 🌉 **Analogy:** If one key opens your house, your car, your office, and your
> safe, then a thief who steals a copy from *any* of those places — even the gym
> locker — now owns your whole life. Reuse means your security equals the security
> of the sloppiest website you ever signed up for.
>
> **Where the analogy breaks down:** a physical thief tries one door at a time.
> Credential stuffing tries your stolen key on ten thousand doors before lunch.

### The fix: a vault and a second lock

Nobody can memorize a hundred long, unique passphrases. You're not supposed to. A
**password manager** is an app that generates long random passwords for every site
and stores them all in an encrypted vault, protected by one strong master
passphrase — the only one you memorize. One vault, one great key, hundreds of
unpickable doors. This course's plain recommendation: use one. The lab sets it up.

Then add the second lock. **Two-factor authentication (2FA)** means a login
requires proof from two *different* categories — something you know plus something
you have. Your bank already thinks this way: the card **and** the PIN; either alone
is useless. With 2FA, a thief who has your password still can't get in without
your phone. One nuance worth one line: codes from an authenticator *app* beat codes
sent by SMS, because phone numbers can be hijacked from the phone company by a
smooth-talking attacker — but SMS 2FA still beats no 2FA, comfortably.

> ✅ **Check yourself**
> 1. Why is `Tr0ub4dor&3` weaker than `correct horse battery staple`?
> 2. A shopping site you used once gets breached. Why might your email account be
>    in danger the same day?
>
> <details><summary>Show answers</summary>
>
> 1. Length beats cleverness: machines try substitutions like 0-for-o first, so
>    the short "clever" one falls quickly, while every extra character in the long
>    one multiplies the guessing work by dozens of times.
> 2. Credential stuffing: attackers take the leaked email+password pairs and try
>    them on every major service by machine. If you reused that password on your
>    email, the stolen key fits your most important door.
> </details>

## ✉️ Encryption: scrambling with a key

Time for the beautiful ideas underneath the padlock icon. **Encryption** is
scrambling a message with a key so that only someone holding the right key can
unscramble it. Anyone else sees meaningless noise. Three flavors matter, each with
its own friendly picture.

**The lockbox (symmetric encryption).** One key both locks and unlocks the box.
Fast and strong — with one catch: you and your friend must both have the key, and
how do you hand over a key... securely... when eavesdroppers watch every channel?
That "key delivery problem" stumped humanity for centuries. Then came a genuinely
lovely trick.

**The padlock mailbox (public-key encryption).** Imagine you manufacture padlocks —
thousands of *open* padlocks, all snapping shut with a finger, all openable only by
the single key that never leaves your pocket. You hand open padlocks to anyone.
Now *anyone* can put a message in a box, snap YOUR padlock shut on it, and mail it —
and from that instant, not even the sender can reopen it. Only you can.

> 🌉 **Analogy — where it breaks down:** with real padlocks, a machinist could study
> one and file a matching key. Public-key encryption rests on math problems that
> are effortless to do forward and (as far as anyone on Earth knows) hopeless to
> reverse — studying the padlock genuinely doesn't reveal the key.

This is what **HTTPS** — Module 03's padlock icon — actually does. Your browser
receives the website's open padlock, uses it to lock up a fresh lockbox key, and
mails it back; only the real site can open that box. From then on, both sides chat
quickly using the shared lockbox. Public-key handshake first, symmetric speed
after. You've done this thousands of times today.

**End-to-end encryption** pushes it one step further: only the sender and the
receiver hold keys — *not even the company that carries the message* can read it.
WhatsApp and Signal work this way: your message is locked with the recipient's
padlock on your phone, and the company relays a sealed box it cannot open.

### Hashing: a fingerprint for data

One more tool, often confused with encryption but delightfully different.
**Hashing** turns any data into a short, fixed-size fingerprint, with two
properties: the same input always yields the same fingerprint, and there is no way
to reconstruct the input from it. Encryption is a locked box you can open with a
key; a hash is a fingerprint — you can't rebuild the finger from the print.

Why it matters to you: honest websites never store your password. They store its
**hash**. At login, they hash whatever you typed and compare fingerprints. If
thieves steal the database, they get fingerprints, not passwords. Which hands you a
red flag for life: **any site that can email you your actual password is storing
it un-hashed — leave.** ("Reset your password" links are fine; that's them
admitting, correctly, that they can't know it.)

> ✅ **Check yourself**
> 1. In the padlock-mailbox scheme, what's public and what's private?
> 2. Why is "we'll email you your password" a red flag?
>
> <details><summary>Show answers</summary>
>
> 1. The padlocks (locking) are public — anyone can have one and snap it shut. The
>    key (unlocking) is private and never leaves the owner.
> 2. It proves they stored your actual password instead of its hash. A breach
>    there leaks the real thing — which, if you reuse passwords, opens your other
>    doors too.
> </details>

## 🎭 The actual attacks (less Hollywood, more con artist)

**Phishing — the fake bank branch.** Someone builds a perfect copy of a login page,
then sends you an urgent message steering you to it: "your account is locked, sign
in immediately." You type your password into their copy; now they have it. This is
the **#1 real-world attack**, responsible for more damage than every Hollywood
technique combined — because it doesn't pick locks, it asks *you* to hand over the
key. The tells: **urgency** (fear is the tool — "24 hours or your account closes"),
**links** (the button says your bank; the actual address is a stranger's — hover,
or long-press on a phone, to see the truth), and **senders** (the address is
almost-right: `support@yourbank-security.com` is not your bank). One habit defeats
most of it: never log in via a link that came *to* you — go to the site yourself.

**Malware and ransomware.** **Malware** is any software built to harm — the burglar
who got inside, usually because something untrustworthy got installed.
**Ransomware** is its nastiest business model: it encrypts *your own files* and
sells you the key — a burglar who changes your locks and offers you your own house
back for a fee. Backups (Module 12's museum copies) turn this catastrophe into an
annoyance.

**SQL injection — one fun paragraph for the road.** Remember Module 12's librarian,
who does exactly what SQL says? Some careless apps paste whatever users type
directly into their SQL. So a prankster types, into an ordinary web form, something
that *ends the expected query and starts a new command* — and the librarian,
meticulous and literal, obeys. Programmers joke about a boy named "Robert'); DROP
TABLE Students;--" — "little Bobby Tables" — whose school database deleted itself
upon enrolling him. The moral is the deepest rule in security: **never trust
input.** Well-built apps treat everything a user types as data, never as
instructions.

**Data breaches.** Sometimes the burglars hit the company vault instead of your
door, and millions of accounts leak at once. You can't prevent that — but you can
find out fast: **[haveibeenpwned.com](https://haveibeenpwned.com)** is a free,
respected service that tells you which known breaches include your email. It's in
the lab.

## 🩹 Updates ARE security

That "restart to update" prompt you keep postponing? Here's what it usually is.
When a security hole is discovered, vendors ship a **patch** — a fix — and publish
that they've done so. Burglars read those announcements too, and immediately go
looking for doors not yet fixed. An unpatched device is a door whose broken lock
has been *published*. "Remind me later" is you leaving it broken another night,
after the burglars got the memo. Enable automatic updates everywhere; it's the
best security-effort ratio in this entire module.

## 🧰 What the professionals do

Two habits of security engineers, worth knowing because they're useful in ordinary
life too. **Threat modeling** means asking, before anything ships: *what would a
burglar try here, and what's worth stealing?* — then defending the doors that
matter instead of everything equally. And **least privilege**: every person and
program gets the *minimum* access needed for its job — the intern doesn't get the
vault key, and (connecting to Module 13) the flashlight app doesn't get your
contacts. When you deny a nosy app permission, you're practicing least privilege
like a professional.

> ✅ **Check yourself**
> 1. What are the three classic tells of a phishing message?
> 2. Why do published security patches make updating *more* urgent, not less?
>
> <details><summary>Show answers</summary>
>
> 1. Urgency ("act within 24 hours!"), links that don't truly lead where they claim
>    (hover to check), and sender addresses that are almost-but-not-quite right.
> 2. Because the patch announcement tells attackers exactly where the hole is.
>    Every unpatched device is now a door with a publicly documented broken lock.
> </details>

## 🎁 Recap

- Attackers are burglars trying every handle at scale, not spies targeting you.
  Don't be the unlocked door.
- **Authentication** = the front desk (know / have / are); **authorization** = the
  keycard's reach.
- **Length beats cleverness** in passwords; **reuse** is the real killer
  (credential stuffing); a **password manager** plus **2FA** (app codes over SMS)
  closes both holes.
- **Encryption**: lockbox (symmetric), padlock mailbox (public-key → HTTPS),
  end-to-end (not even the company). **Hashing** = fingerprints; "we'll email you
  your password" = leave.
- Real attacks: **phishing** (#1 — urgency, links, senders), **ransomware** (your
  locks, sold back to you), **SQL injection** (never trust input), **breaches**
  (haveibeenpwned.com).
- **Updates are patches for published holes.** Engineers practice **threat
  modeling** and **least privilege** — and now, so do you.

## ➡️ Where next?

That completes Part 4 — the computer science canon, minus the scary math. You now
speak algorithm, database, operating system, network, and security. Part 5 takes
everything you've learned and asks a very modern question: why does almost none of
this run in your house anymore? Whose computers is everything on — and what did
"the cloud" do to the entire software industry?

**Next up:** [Module 15 — The Cloud: Renting Other People's Computers](../15-the-cloud/README.md)
