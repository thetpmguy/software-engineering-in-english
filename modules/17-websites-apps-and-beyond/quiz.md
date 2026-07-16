# ✅ Quiz 17 — Websites, Apps & Everything Else

Answer first, then open the fold. Wrong answers are arrows pointing at the section worth
rereading.

---

**1. The module organizes all software by one question. What is it, and why is it so
useful?**

<details><summary>Show answer</summary>

"Where does the code run?" — in the browser, on the phone, on the desktop, inside a
device, or across all of them. It's useful because the habitat determines almost
everything: what the software can do, how it's built, what it costs, and how it reaches
users.
</details>

**2. Website vs. web app: what's the difference, and which is Wikipedia vs. Google
Docs?**

<details><summary>Show answer</summary>

A website presents information you mostly read (the brochure); a web app is an
interactive tool running in the browser (the workshop). Wikipedia = website/brochure;
Google Docs = web app/workshop. Same building — the browser — different purposes.
</details>

**3. Why did the lesson call the browser "a universal app-player"?**

<details><summary>Show answer</summary>

Because any browser on any device can run any web page — so software built for the
browser instantly reaches everyone, with no installs, no app store review, and no
per-platform rebuild. That reach is the web's superpower.
</details>

**4. Your startup wants a "perfect-feeling" app on both iPhone and Android. What's the
tailor-shop version of your options and costs?**

<details><summary>Show answer</summary>

Native = tailor-made suits: Swift for iPhone, Kotlin for Android — perfect fit, but two
suits means two codebases and roughly double the cost, forever. Cross-platform (React
Native/Flutter) = one pattern producing two suits: much cheaper, very good fit, small
compromises. The budget conversation is choosing between those two tailors.
</details>

**5. Name two things app stores take from developers and one thing they give.**

<details><summary>Show answer</summary>

They take: a 15–30% commission on in-app sales, and control — every app must pass their
review, with delays and possible rejection. They give: distribution to billions of
phones plus a safety screening that makes users willing to install. Landlords: rent and
rules, but a location you can't match on your own.
</details>

**6. How can you tell a desktop app might be "a website in a costume," and why do
companies build them that way?**

<details><summary>Show answer</summary>

Clues: a near-identical browser version exists; right-clicking reveals browser menu
items like "Inspect"; the process list shows several memory-hungry helper processes.
That's Electron — a web app shipped inside a stripped-down browser. Why: build once,
run on Windows/Mac/Linux — one team instead of four. The cost lands on you, in memory.
</details>

**7. Roughly how much code runs a modern car, and what does that say about where most
software lives?**

<details><summary>Show answer</summary>

On the order of 100+ million lines. It says the biggest habitat is the invisible one:
embedded software in cars, appliances, medical devices, and infrastructure. By count of
running programs, most of the world's software is code you'll never see on a screen.
</details>

**8. Your microwave never gets software updates. Fine or scary? And what about a car?**

<details><summary>Show answer</summary>

The microwave: fine — one job, no network connection, nothing for an attacker to reach;
it'll run its code flawlessly for twenty years. A car (or pacemaker): a different
conversation — high stakes and, increasingly, network connections — which is why those
industries build and test to far stricter standards, and why modern cars *do* get
updates.
</details>

**9. Give one honest upside and two honest downsides of a "smart" (IoT) lightbulb.**

<details><summary>Show answer</summary>

Upside: real convenience — control from bed, schedules, automation. Downsides (any
two): it's a tiny networked computer that can be hacked; it may die or go dumb when the
maker's cloud service shuts down; it may report your usage habits to someone's
database. "Smart" means connected — and connected cuts both ways.
</details>

**10. Why are games "the everything-discipline," and what problem do Unity and Unreal
solve?**

<details><summary>Show answer</summary>

A game must run physics, 3D graphics, character AI, audio, networking, and input all at
once, redrawing the world about 60 times per second. Unity and Unreal are game engines
— pre-built movie studios providing the cameras, lighting, and sound stages — so
creators build the game (script and vision) instead of rebuilding the machinery for
every title.
</details>

**11. A charity asks you: "We have a tiny budget and need everyone — on any device — to
reach our tool *this month*." Which habitat, and why? What would change your answer?**

<details><summary>Show answer</summary>

Web app. Maximum reach (the browser is the universal app-player), one codebase, no app
store review, ships fast — the exact fit for small budget + broad audience + short
timeline. You'd reconsider if they needed phone superpowers: offline use in the field,
camera-heavy workflows, or push notifications — that pushes toward native or
cross-platform, at real extra cost.
</details>

**12. 🗣️ Explain it to a friend.** A friend asks: "How can WhatsApp be on my phone, my
boyfriend's iPhone, my laptop browser, *and* a desktop app — and my chats are the same
everywhere? Did they build it four times?" Give a two-minute answer using the
restaurant analogy from Module 10.

<details><summary>Show a sample answer (read only after trying!)</summary>

"Sort of four times — but only the part you can see. Think of WhatsApp as a restaurant.
There's one kitchen — their servers, where every message and contact actually lives —
and several dining rooms: an Android room, an iPhone room, a browser room, a desktop
room. Each dining room was built separately, tailored to its building, which is why
they cost real money to make and feel slightly different. But every one of them sends
orders to the same kitchen. When you send a message from your phone, it goes to the
kitchen — so when you open your laptop, the same kitchen serves the same conversation.
They built the dining rooms four times; the restaurant's heart exists once. That's why
your chats follow you everywhere."
</details>
