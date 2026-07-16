# 🔧 Lab 17 — The Software Safari, at Home

> **Goal:** spot every species from the lesson living in your own house: compare one
> service across its many bodies, unmask a desktop app in a browser costume, count your
> hidden computers, and watch responsive design reshape a page under your fingers. No
> installs, no sign-ups, no cost.
>
> **Time:** 45–60 minutes. Parts 1, 3, and 4 work on a phone; Part 2 needs a desktop or
> laptop (skip it if you don't have one — the rest still works).

---

## Part 1 — Web-app safari: one service, three bodies (15 minutes)

Pick a service you use that exists everywhere — **YouTube** is perfect (Spotify or Gmail
also work). You'll visit the same kitchen through three dining rooms.

1. **Body 1 — desktop/laptop browser** (or your phone's browser with "Desktop site"
   turned on): go to **youtube.com**.
2. **Body 2 — the phone app**: open the YouTube app you already have.
3. **Body 3 — the phone browser**: open **youtube.com** in your phone's browser
   *without* letting it bounce you into the app (if it nags, look for "continue in
   browser").
4. Now hunt for **five differences** between the bodies. Prompts: Where does search
   live? What happens when you swipe? Which one sends notifications? Which one can
   download videos for offline? Do videos keep playing when you switch away? How do
   comments look?
5. Write your five down. Then guess: **which bodies share one codebase?**

**What you should see:** the phone app feels smoothest and has powers the browser
versions lack (downloads, notifications) — it's the native suit. The two browser
versions look different from each other but behave like siblings — same web codebase,
responsively reshaped. And your account, subscriptions, and history are identical
everywhere: one kitchen, three dining rooms.

## Part 2 — Unmask the Electron app (10 minutes, desktop only)

The lesson claimed your chat or music app might be a browser in a costume. Let's check.

1. Pick a desktop app you have installed — chat apps and music apps are prime suspects.
2. Try these unmaskings, in order, until one works:
   - **The web-address test:** does the exact same app exist as a website you can log
     into in a browser, looking nearly identical? Strong evidence of a shared web
     codebase.
   - **The right-click test:** inside the app, right-click on some text or empty space.
     If you see options like **"Inspect"** or **"Copy link address"** — those are
     *browser* menu items. Costume detected.
   - **The memory test:** open your system's process list (Windows: press
     Ctrl+Shift+Esc for Task Manager; Mac: open Activity Monitor from Applications →
     Utilities). Find your app. Is one "app" actually **several processes** using
     hundreds of megabytes each — sometimes with "Helper" or "Renderer" in the name?
     That's the hidden browser breathing.
3. Verdict: browser in a costume, or true desktop native?

**What you should see:** most modern chat apps fail at least two tests — congratulations,
you've unmasked an Electron app. Now you know where your memory goes, and why the
company chose it anyway: build once, run everywhere.

## Part 3 — Census of the hidden computers (15 minutes)

The lesson claimed you own dozens of computers. Time for a census. **Target: 20 or
more.**

1. Walk through your home (and to your car, if you have one) with a notes app.
2. List every object that contains a computer — a clue: anything with a screen, a menu,
   a timer you can program, a sensor, or a connection. Starters: TV, washing machine,
   microwave, car (that one's worth several), thermostat, printer, router, watch, game
   console, e-reader, doorbell, speaker, camera, toothbrush, kitchen scale, headphones
   (yes — wireless ones have a chip running code).
3. For each, mark two columns: **WiFi?** (is it connected — is it IoT?) and
   **Updates?** (does it ever receive new software?).

**What you should see:** you'll likely blow past 20. Then study your columns — they
split your home into the lesson's three groups: classic embedded (microwave: no WiFi,
no updates, totally fine), IoT (smart speaker: WiFi, frequent updates), and the
interesting middle (a smart TV that *has* WiFi but *stopped* getting updates — the
honest worry from the lesson, sitting in your living room).

## Part 4 — Watch responsive design work (10 minutes)

1. On a desktop browser, open a major news site (or wikipedia.org).
2. Make the window narrow — drag the edge **slowly** — then widen it again. Watch the
   layout *reshape itself*: three columns fold to two, then one; menus collapse into a
   ☰ button; images resize.
3. Bonus tour (desktop): press **F12** (or right-click → Inspect) to open **DevTools**
   — the browser's built-in X-ray machine you may remember from earlier labs. Find the
   **device toolbar** button (it looks like a small phone-and-tablet icon, or press
   Ctrl+Shift+M / Cmd+Shift+M on Mac). Your page is now wearing a phone costume — pick
   different phones from the dropdown and watch the page refit itself to each one.
4. Phone-only alternative: rotate your phone between portrait and landscape on the same
   site — that reshaping is the same responsive design responding.

**What you should see:** one single web page fluidly refitting itself to every screen
you throw at it. Nobody built a "narrow version" — the page carries rules for
rearranging itself. This is exactly how one web codebase serves your laptop and your
phone, which is the economic secret behind half the choices in this module.

---

## ✅ Lab complete — what you proved

- One service really does live as many bodies — and you can tell the native suit from
  the web dining rooms by what each can do.
- Your desktop apps may be websites in costumes, and you now have three unmasking
  tests.
- You own far more computers than you thought, and you can now sort them: embedded,
  IoT, or "connected but abandoned."
- Responsive design isn't magic — you watched one page refit itself to every screen,
  live.
