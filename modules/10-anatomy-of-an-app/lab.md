# 🔧 Lab 10 — Look Behind the Curtain

> **Goal:** see frontend, backend, and APIs with your own eyes — on real, live
> websites — using a professional tool that's been hiding in your browser all along.
>
> **You'll need:** a **laptop or desktop browser** for Parts 1–2 (Chrome, Edge, Firefox,
> or Safari — the tool we need is awkward on phones). Part 3 works on anything,
> including a phone. Time: 40–60 minutes.

> ⚠️ **Watch out:** browsers move their menus around, and every website's internals look
> different. We describe *intents* ("find the option to inspect the page"), not exact
> pixels. Nothing in this lab can harm anything — you'll see why in Part 1, and it's the
> best lesson of the day.

---

## Part 1 — Edit a famous website (yes, really) (15 minutes)

Every major browser includes **DevTools** — a panel of instruments made for frontend
engineers, free inside the browser you already have. First stop: the **Elements** view,
which shows the live HTML skeleton of any page you're on.

1. On your laptop, visit a big news website — any famous one with headlines.
2. Open DevTools. Any of these works:
   - Press **F12**, or
   - Press **Ctrl+Shift+I** (Windows) / **Cmd+Option+I** (Mac), or
   - **Right-click any headline** and choose **Inspect** (on Safari, first enable the
     Develop menu in Settings → Advanced).
3. A busy panel opens (side or bottom). Don't panic — you already know what you're
   looking at: that dense nested text is **HTML**, the skeleton from the lesson. Find
   the tags: `<h1>`, `<p>`, `<a>`.
4. If you right-clicked a headline and chose Inspect, one line is highlighted — that
   *is* the headline, as the browser sees it. (Otherwise: click the little
   arrow-in-a-box icon in DevTools' corner, then click a headline on the page.)
5. Now the magic: **double-click the headline text inside the DevTools panel**, type
   your own words — *"Local Reader Discovers Websites Are Made of Text"* — and press
   Enter.
6. Look at the page.

**✅ What you should see:** the real page, showing *your* headline. On the actual famous
website.

Now the teachable moment — three questions before Part 2:

- **Did you hack the site?** No. Refresh the page (F5). Your headline vanishes and the
  real one returns. You edited **your copy** of the dining room — the frontend that was
  sent to *your* device. The kitchen (their servers) never heard about it. Every visitor
  gets their own copy of the dining room; redecorating yours changes nobody else's.
- **Why does this matter beyond fun?** It's the proof of a core lesson idea: *the
  frontend is in the user's hands and cannot be trusted with anything important.* You
  changed their headline in ten seconds. This is exactly why "did the payment succeed?"
  must be decided in the backend.
- **A wise habit:** screenshots of "edited" webpages are exactly this cheap. Someone
  showing you a screenshot of a shocking headline or a huge bank balance… now you know
  a ten-second way it can be faked.

**Bonus poke:** in Elements, find the **Styles** area (usually beside the HTML). That's
the **CSS** — the clothing. Click a color value and change it; watch the page change.
Refresh to undo everything.

---

## Part 2 — Watch the waiters run: the Network tab (15 minutes)

Now let's *see* API requests — the waiters — in motion.

1. Stay on any busy site, or open a new one (a weather site is ideal). In DevTools,
   find the **Network** tab.
2. It may be empty — it only records while open. **Refresh the page** and watch: a
   waterfall of rows floods in. *Every row is one request* your browser made — one
   waiter dispatched. The page itself, each image, the CSS, the JavaScript, and the API
   calls. A typical page fires dozens to hundreds. (Feel free to gasp; everyone does.)
3. Now interact: search for a city on the weather site, scroll a feed, click around.
   New rows appear *as you act* — those are frontend-to-backend orders being placed in
   real time, exactly step 3 of the lesson's Like-button journey.
4. Let's read one waiter's tray. Find the filter row in the Network tab and click
   **Fetch/XHR** — this hides images and decorations, showing (mostly) API calls.
5. Click any row, then find its **Response** (or **Preview**) tab. Many responses look
   like this:

   ```
   { "city": "Lisbon", "temperature": 24, "condition": "sunny" }
   ```

   That format is **JSON** — the simple labeled-values format most APIs use to send
   data, readable by machines *and* by you. Labels, colons, values, braces. Take a
   moment: you are reading the actual message a backend kitchen sent to your dining
   room. This is what the internet's waiters actually carry.

**✅ What you should see:** a stream of requests appearing as you interact, and at least
one JSON response you can partly read and partly guess at. Weird extra fields you don't
understand? Wonderful — those are the kitchen's own notes; nobody reads *all* of them.

---

## Part 3 — Order from a kitchen yourself: call a real API (10 minutes)

Time to be your own frontend. You'll place an API order by hand, with no app in
between — from the browser's address bar. We'll use **Open-Meteo**, a well-known free
weather API that requires no account and no key.

1. Copy this into your address bar (one line, then Enter):

   ```
   https://api.open-meteo.com/v1/forecast?latitude=48.85&longitude=2.35&current_weather=true
   ```

2. Read what you just ordered, in the URL itself: *from the kitchen at
   api.open-meteo.com, the dish called "forecast", for latitude 48.85, longitude 2.35
   (that's Paris), current weather please.* The part after the `?` is the order's
   details — like "no onions" on a ticket.

**✅ What you should see:** no webpage — no dining room at all! — but raw JSON, exactly
as in Part 2, containing something like `"temperature"` and `"windspeed"` for Paris
right now. You skipped the frontend and spoke to a backend directly. That's all an API
call is.

3. Change the order: edit the latitude/longitude in the address bar to your own city
   (search "my city latitude longitude" to find them) and press Enter. Fresh JSON, your
   weather.

**If it doesn't work:** typos in long URLs are the usual suspect (every `&` and `=`
matters — machines are literal, as ever). Still stuck? Search for "open-meteo docs",
where the same URL pattern is shown copy-pasteable; or try it on another network —
some office/school networks block unfamiliar addresses.

---

## Part 4 — Dissect your favorite app on paper (10 minutes)

Last, prove the anatomy generalizes — no computer needed.

1. Take a screenshot of your favorite app's main screen (or sketch it by hand —
   printing works too, hence "label a printed screenshot").
2. Draw arrows and label at least:
   - **Three frontend things** — anything you can see or touch: a button, the layout,
     the colors, an animation.
   - **Three things that must come from the backend** — anything the app couldn't know
     by itself: other people's posts, your account balance, today's weather, search
     results, prices.
   - **One arrow labeled "API request"** from a touchable thing to a backend thing,
     with a one-line guess at the order: *"get the latest messages in this chat"*.
3. The test for every label: **"Could my phone know this all by itself, even in
   airplane mode?"** If yes → frontend. If no → it arrived from a kitchen, by waiter.

**✅ What you should see:** a labeled diagram — congratulations, it's an architecture
sketch of an app you use every day, drawn from the outside by pure deduction. This is
genuinely how engineers reason about unfamiliar systems.

---

## 🎉 Done!

Today you edited a famous website's frontend (harmlessly), watched real API traffic,
read JSON off the wire, called a live backend by hand, and drew an architecture
diagram. The next time an app misbehaves, you may catch yourself wondering *"hmm —
dining room problem, or kitchen problem?"* That question is the whole module, installed
permanently in your head.
