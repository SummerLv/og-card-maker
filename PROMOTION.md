# OG Card Maker - Social Media Promotion Plan

> **Goal:** Drive traffic and get at least 1 person to tip $1 via Buy Me a Coffee within 2 days.
> **URL:** https://og-card-maker.vercel.app
> **Target Audience:** Overseas developers, indie hackers, designers, content creators

---

## 1. Reddit Posts

### 1.1 r/InternetIsBeautiful (17M subscribers)

> Style: Clean, factual, "here's a useful thing". No hype.

**Title:** A free browser tool that generates social media preview cards in seconds — no signup, no watermark, no data uploaded

**Body:**

Hey! I built a simple tool that generates Open Graph / social media preview images right in your browser.

**What it does:**
- Pick from 16+ gradient themes and 8 texture patterns
- Add your title, subtitle, and an emoji icon
- Choose a size: OG (1200x630), Twitter (1200x675), or Square (1080x1080)
- One-click copy to clipboard or download as PNG

**What it doesn't do:**
- No signup or account needed
- No watermark
- No data leaves your browser (100% client-side)
- No cost — completely free

I built this in one evening because I was tired of opening Figma every time I needed a quick preview image for a blog post or project. Everything runs on Canvas API in your browser.

Link: https://og-card-maker.vercel.app

Hope someone else finds it useful!

---

### 1.2 r/SideProject (200K+ subscribers)

> Style: Build-in-public, storytelling, journey-focused. BMC mention is acceptable here.

**Title:** I built a free OG image generator in one evening — $0 to run, solves a 20-minute problem in 10 seconds

**Body:**

Hey r/SideProject! Sharing a tiny tool I shipped last night.

**The itch I was scratching:**

Every time I launched a project or wrote a blog post, I'd spend 15-20 minutes in Figma making the social preview image. Pick colors, align text, export at 1200x630, realize Twitter needs 1200x675, re-export... It felt absurd for something people glance at for half a second.

**What I built:**

[OG Card Maker](https://og-card-maker.vercel.app) — a browser-based tool that generates social media preview cards instantly.

- 16+ gradient themes (carefully picked color combos that just work)
- 8 texture overlays (dots, grid, waves, diagonal lines, etc.)
- Emoji icon support
- Three export sizes: OG, Twitter, Square
- One-click copy to clipboard
- Pure frontend — no backend, no auth, no database

**Tech:** Vanilla HTML/CSS/JS + Canvas API. Deployed on Vercel free tier. Total monthly cost: $0.

**Build time:** About 4 hours from "I'm annoyed" to "it's live."

**What I learned shipping this:**
1. The Canvas API is criminally underused for tools like this — most people reach for Puppeteer/headless Chrome, but you can do so much client-side
2. A two-color gradient + subtle texture looks more "designed" than complex graphics
3. Shipping something complete in one evening beats polishing something for two weeks

**What's next:** Custom color picker, font options, and maybe saved templates if people actually use it.

It's completely free and always will be (it literally costs nothing to host). If it saves you time and you want to fuel more late-night build sessions, there's a [Buy Me a Coffee](https://buymeacoffee.com/) link on the site — but zero pressure, genuinely just happy if it's useful.

Would love feedback — what themes or features would make this better for your workflow?

---

### 1.3 r/webdev (2.4M subscribers)

> Style: Technical, educational, share implementation details. Must provide value beyond just "look at my tool."

**Title:** I replaced my Figma OG image workflow with a Canvas API tool — here's the technical approach (no backend, no dependencies)

**Body:**

Hey r/webdev — sharing a tool I built for myself that other devs might find useful, plus some technical details on the approach.

**The tool:** [OG Card Maker](https://og-card-maker.vercel.app) — generates Open Graph / social media preview images entirely client-side.

**Why client-side over the usual Puppeteer approach?**

Most OG image generators use server-side rendering (Vercel's `@vercel/og`, Cloudinary, headless Chrome, etc.). They work great, but for a simple "gradient + text" card, spinning up a server felt like overkill. I wanted:
- Zero hosting costs (no serverless cold starts)
- No rate limits or API keys
- Data stays in user's browser
- Works offline once loaded

**Technical implementation:**

```
Architecture: Single HTML file → Canvas 2D Context → toBlob() → Clipboard API
```

Key Canvas API patterns I used:

1. **Gradients:** Recreated CSS-like gradients using `createLinearGradient()` with angle math. Each theme is defined as `{ angle, stops: [{color, position}] }`.

2. **Textures:** Drew patterns procedurally (no external images). Dots use `arc()`, grids use `moveTo()/lineTo()`, waves use `quadraticCurveTo()`. Applied with `globalAlpha` for subtle overlay effect.

3. **Text rendering:** This was the trickiest part. Canvas has no built-in multiline text support, so I had to:
   - Use `measureText()` to calculate line widths
   - Implement word-wrapping by measuring word-by-word
   - Handle vertical centering manually
   - Scale font size down if text overflows

4. **Copy to clipboard:** `canvas.toBlob('image/png')` → `new ClipboardItem({'image/png': blob})` → `navigator.clipboard.write()`. Falls back to download if Clipboard API isn't available.

5. **Emoji rendering:** Canvas renders emoji via the system font stack. Set `font-family` to include emoji fonts, then `fillText()` handles the rest. Cross-platform rendering varies slightly but works well enough.

**What the tool offers:**
- 16+ gradient presets with texture overlays
- Three sizes: 1200x630 (OG/Facebook), 1200x675 (Twitter), 1080x1080 (Square/Instagram)
- One-click copy or download
- No signup, no watermark

**Performance:** The entire page is ~50KB. No frameworks, no build step, no node_modules. First paint is essentially instant on Vercel's CDN.

**Limitations I'm aware of:**
- No custom fonts (system stack only, for now)
- No image/logo upload
- Preset colors only (custom picker coming)
- Emoji rendering differs across OS

Happy to discuss the Canvas rendering approach, text measurement quirks, or gradient math if anyone's interested. Source is vanilla JS if you want to peek or fork.

Free to use: https://og-card-maker.vercel.app

---

## 2. Twitter/X Thread (7 tweets)

### Tweet 1 (Hook — include a screenshot/GIF)

I built a free OG image generator in one evening.

No signup.
No watermark.
No data uploaded.
Runs 100% in your browser.

→ 16+ themes
→ 8 textures
→ 3 export sizes
→ One-click copy

Here's the tool + the story 🧵

https://og-card-maker.vercel.app

---

### Tweet 2 (Problem)

The problem:

Every side project, every blog post, every shared link needs an OG image.

My old workflow:
1. Open Figma
2. Create 1200x630 artboard
3. Pick gradient colors
4. Add text, align everything
5. Export PNG
6. Upload somewhere

Time: 15-20 minutes for something people see for 0.5 seconds.

---

### Tweet 3 (Solution)

The new workflow:

1. Open OG Card Maker
2. Type title + subtitle
3. Pick a theme
4. Click "Copy"

Time: 10 seconds.

That's it. That's the whole tool.

---

### Tweet 4 (Features)

What's inside:

🎨 16+ gradient themes (curated, not random)
🔲 8 texture patterns (dots, grid, waves, lines...)
😀 Emoji icons
📐 3 sizes: OG (1200x630), Twitter (1200x675), Square (1080x1080)
📋 One-click copy to clipboard
💰 Cost: $0. Forever.

---

### Tweet 5 (Technical / Build in Public)

Technical details:

• Vanilla JS — no React, no framework
• Canvas API for rendering
• Textures drawn programmatically (no external assets)
• Clipboard API for native copy
• Single HTML file, ~50KB total
• Deployed on Vercel free tier
• Build time: ~4 hours one evening

Sometimes the simplest solution is the best one.

---

### Tweet 6 (Use Cases + Soft CTA)

Who it's for:

• Indie hackers launching products
• Bloggers who hate making thumbnails
• Devs with GitHub repos that need social cards
• Newsletter writers
• Anyone who shares links and wants them to look good

It's free, it'll stay free.

If it saves you time, you can buy me a coffee ☕ (link on the site)
But honestly just a "this is useful" reply makes my day.

---

### Tweet 7 (Engagement + Hashtags)

What should I build next?

Thinking about:
□ Custom color picker
□ Font selection
□ Logo/image upload
□ Saved templates
□ API for automation

What would be most useful? Reply below 👇

#buildinpublic #indiehackers #webdev #devtools #sideproject #ogimage #freetools

---

## 3. Hacker News — Show HN

**Title:**

```
Show HN: OG Card Maker – Free browser-based social media preview image generator
```

**First comment (post immediately after submission):**

Hi HN! I built this because my OG image workflow felt disproportionately heavy for what it produced.

The problem: Every blog post / side project / shared link needs a social preview image (Open Graph). The standard options are:
- Figma (manual, 15-20 min each time)
- Vercel's @vercel/og (requires backend/API route)
- Cloudinary overlays (requires account + API key)
- Canva (requires signup, adds watermark on free tier)

I wanted something where I could type a title, pick a style, and get a 1200x630 PNG in under 10 seconds. With nothing uploaded anywhere.

Technical approach:
- Canvas 2D API for all rendering
- Gradients computed with angle math → createLinearGradient()
- Textures drawn procedurally (arc, lineTo, quadraticCurveTo) — no external assets
- Text wrapping via measureText() word-by-word (Canvas has no native multiline support)
- Export via canvas.toBlob() → Clipboard API
- Static deploy on Vercel, zero running costs

Current limitations (being honest):
- System fonts only (no custom font upload yet)
- Preset themes only (no custom color picker yet)
- No image/logo support
- Emoji rendering varies by OS

The tool outputs standard sizes: 1200x630 (OG/Facebook/LinkedIn), 1200x675 (Twitter), 1080x1080 (Instagram/Square).

I intentionally kept scope minimal to ship in one evening. Happy to iterate based on what people actually need.

Would particularly appreciate feedback on:
1. Are the preset themes varied enough, or is a custom color picker essential?
2. Would anyone use an API/CLI version of this?
3. Any sizes I'm missing for specific platforms?

---

## 4. Product Hunt Preparation

**Tagline (under 60 chars):**

```
Beautiful social preview images in 10 seconds. Free forever.
```

**Description:**

OG Card Maker is a free, browser-based tool for creating social media preview images (Open Graph cards) instantly.

Stop spending 20 minutes in Figma for a social card. Pick a gradient theme, add a texture overlay, type your title, and copy to clipboard. Done in 10 seconds.

**Features:**
- 16+ curated gradient themes
- 8 texture/pattern overlays
- Emoji icon support
- Multiple sizes: OG (1200x630), Twitter (1200x675), Square (1080x1080)
- One-click copy to clipboard
- 100% client-side — your data never leaves your browser
- No signup, no watermark, no cost

Built for indie hackers, developers, bloggers, and anyone who ships things and needs OG images that don't look like an afterthought.

**Topics/Categories:** Design Tools, Developer Tools, Productivity, Open Source

**First Comment (Maker Comment):**

Hey Product Hunt! 👋

I'm the maker of OG Card Maker. Here's the honest backstory:

I have a bunch of side projects, and the most annoying part of every launch is always the OG image. Not hard — just tedious. Open Figma, pick colors that look decent together, position text, export at the right dimensions, remember that Twitter uses different dimensions than Facebook...

One evening I thought: "What if I just built a tool that does this in 10 seconds?"

Four hours later, OG Card Maker was live. It uses the Canvas API to render everything client-side — no server, no uploads, no accounts needed. Pick a theme, type your text, copy to clipboard. That's the whole product.

**Why free?** It costs me $0 to run (static files on Vercel's free tier). I can't justify charging for it.

**Why no signup?** Because generating a preview image doesn't require my email address, so I'm not going to ask for yours.

I plan to add a custom color picker, font options, and maybe saved templates based on feedback. If you have ideas for what would make this more useful for your workflow, I'm all ears!

And if it saves you time on your next launch day — a coffee fuels the next late-night build session ☕ (link on the site). But genuinely, just knowing people use it is reward enough.

Happy launching! 🚀

---

## 5. Posting Time Recommendations

All times in **US Eastern Time (ET)** — optimized for US + EU overlap.

| Platform | Best Days | Best Time (ET) | Reasoning |
|----------|-----------|-----------------|-----------|
| r/InternetIsBeautiful | Tue–Thu | 7:00–9:00 AM | US morning browsing + EU still online in afternoon |
| r/SideProject | Mon–Wed | 8:00–10:00 AM | Indie hackers check feeds early in the week |
| r/webdev | Tue–Thu | 9:00–11:00 AM | Devs browse before entering deep work |
| Twitter/X | Tue–Wed | 8:00–10:00 AM | Peak tech Twitter engagement window |
| Hacker News | Tue–Thu | 8:30–10:00 AM | US waking up + EU afternoon = maximum eyeballs |
| Product Hunt | Tue–Thu | 12:01 AM PT (3:01 AM ET) | PH resets at midnight PT; early = maximum voting time |

### Recommended 2-Day Execution Schedule

**Day 1 (Tuesday):**

| Time (ET) | Action |
|-----------|--------|
| 8:00 AM | Post Hacker News (Show HN) — immediately post your first comment |
| 8:15 AM | Post Twitter/X thread — include screenshot in first tweet |
| 9:00 AM | Post r/InternetIsBeautiful |
| 9:00 AM–12:00 PM | Actively respond to ALL comments on HN and Twitter |
| 2:00 PM | Post r/webdev |
| 2:00–5:00 PM | Continue engaging with comments everywhere |

**Day 2 (Wednesday):**

| Time (ET) | Action |
|-----------|--------|
| 8:00 AM | Post r/SideProject |
| 8:30 AM | Quote-tweet your original thread with a "Day 2 update" |
| 9:00 AM–12:00 PM | Engage with Day 1 comments + new Day 2 comments |
| 12:00 PM | Check HN — if it's still on the front page, keep responding |
| 3:00 PM | If reception is good, share in relevant Discord/Slack communities |

**Day 3+ (if needed):**
- Product Hunt launch (prep the night before, launch at 12:01 AM PT Tuesday)
- Only do PH after you have some social proof (comments, tweets, etc.)

---

## 6. Platform Rules & Anti-Deletion Tips

### Reddit — Universal Rules

| Do | Don't |
|----|-------|
| ✅ Engage genuinely with every comment | ❌ Post the same link to multiple subs within 2-3 hours |
| ✅ Have non-promotional comment history (10+ comments in other subs first) | ❌ Use URL shorteners |
| ✅ Vary your wording significantly across subreddits | ❌ Ask for upvotes anywhere |
| ✅ Stay active for 2-3 hours after posting | ❌ Mention "upvote" or "viral" |
| ✅ Your account should be 30+ days old with positive karma | ❌ Copy-paste identical text across subs |
| ✅ Respond to critical comments gracefully | ❌ Delete and repost if it doesn't take off immediately |

### r/InternetIsBeautiful — Specific Rules
- The site must be **interactive** — a static landing page will be removed
- Prefer factual, descriptive titles (not "I made the BEST tool ever")
- Some mods prefer link posts (URL as the post) over text posts — check current top posts
- The tool must be **free to use** (✓ we qualify)
- Don't include your "journey" or "story" — just describe what the tool does
- Avoid "I" in the title if possible (but "I made" is sometimes allowed — check recent posts)

### r/SideProject — Specific Rules
- Text posts with storytelling do best here
- Build-in-public narrative is welcomed and expected
- You CAN mention Buy Me a Coffee — this community supports makers
- Share numbers (build time, cost, etc.) — transparency wins here
- Asking for feedback at the end is expected
- Flair your post correctly

### r/webdev — Specific Rules
- **Must provide technical value** — a pure promo post will be removed
- Include code snippets, architecture decisions, or technical learnings
- Frame it as "here's an interesting technical approach" not "look at my product"
- Alternative: Post in the weekly "Showoff Saturday" thread if your standalone post gets removed
- Don't use marketing language ("revolutionary", "game-changing")

### Hacker News — Rules & Culture
- Title format must be: `Show HN: [Name] – [factual description]`
- **Post your explanatory comment immediately** (within 60 seconds of submission)
- Never ask for upvotes (anywhere — not on Twitter, not in DMs, nowhere)
- Be honest about limitations — HN respects intellectual honesty
- Respond to every comment, especially skeptical/critical ones
- Don't use superlatives or marketing language
- If flagged/killed, email dang@ycombinator.com — don't repost
- Having a live demo + source code significantly increases trust
- HN audience values "does one thing well" — don't oversell scope

### Twitter/X — Best Practices
- First tweet must be self-contained (many won't click "Show more")
- **Include a screenshot or GIF in tweet 1** (2-3x engagement boost)
- Keep hashtags to 2-3 max in the first tweet; dump the rest in the final tweet
- Pin the thread to your profile
- Don't put the BMC link in the main thread — add it as a reply or in your bio
- Engage with replies within the first hour (algorithm rewards early engagement)
- Quote-tweet > plain retweet for your own content

### Product Hunt — Rules & Strategy
- Best days: Tuesday, Wednesday, Thursday
- Launch at 12:01 AM PT to maximize voting time
- Have all assets ready: logo (240x240), gallery images (1270x760), GIF/video
- Reply to every comment within 30 minutes
- Get 3-5 supporters to leave genuine (not generic) comments early
- Self-hunting is fine (you don't need an external hunter)
- Don't ask for upvotes in DMs — PH penalizes this
- One launch per product — make it count

---

## 7. Buy Me a Coffee — Integration Strategy

### On the Tool Itself (Critical)
- Place a small, non-intrusive "☕ Buy me a coffee" button in the footer
- **Best placement:** Show it AFTER user has copied/downloaded their first image (they've received value first)
- Alternative: Subtle floating badge in bottom-right corner
- Copy suggestion: `"Made in one evening with ☕ — Buy me a coffee if this saved you time"`
- Don't make it a popup or modal — that kills goodwill

### Per Platform — When to Mention BMC

| Platform | BMC Strategy |
|----------|--------------|
| r/InternetIsBeautiful | ❌ Never mention in post. Let them find it on the site. |
| r/SideProject | ✅ Casual mention at the end is fine ("if you want to fuel more builds...") |
| r/webdev | ❌ Don't mention. Focus on technical value. |
| Twitter/X | ⚠️ Mention in tweet 6 casually, or add as a reply to the thread |
| Hacker News | ❌ Never mention. HN will downvote promotional content. |
| Product Hunt | ✅ Brief mention in maker comment ("coffee fuels late-night builds") |

### Psychology Tips
- People tip when they feel **grateful** and **connected** — not when they feel pressured
- The "one evening build" story creates relatability
- "$0 to run" makes people think "this person isn't making money, I should support them"
- Responding to comments personally makes people more likely to support

---

## 8. Engagement Response Templates

### When someone says "cool tool!" or "this is useful":
> Thanks! Curious — what are you using it for? Blog posts, project launches, something else? Always love hearing use cases I haven't thought of.

### When someone asks for a feature:
> Great idea! Adding it to the list. What's your workflow — are you making OG images for a blog, social posts, or something else? Helps me prioritize.

### When someone compares it to Canva/Figma/other tools:
> Totally — [tool] is great for complex designs! I built this for the specific case where you just need a clean OG card in 10 seconds without signing up for anything. Different tools for different moments.

### When someone asks about the tech:
> Vanilla JS + Canvas API, no dependencies. The trickiest part was text wrapping — Canvas has no built-in multiline support, so you have to measure word-by-word with measureText() and manually break lines. Surprisingly fun to implement though.

### When someone asks "why free?":
> Honestly, it costs me $0/month to run (static files on Vercel free tier). I can't justify charging for something this simple. If it saves you time and you want to toss me a coffee, there's a link on the site — but genuinely no pressure.

### When someone is skeptical ("yet another OG tool"):
> Fair point — there are a lot of these! The difference here is: no signup, no watermark, no upload, runs entirely in your browser. I built it because the existing options all had at least one of those friction points. But yeah, if your current workflow works for you, no need to switch.

### When a post gets unexpected traction:
> Edit: Wow, wasn't expecting this response! A few common questions I'm seeing:
>
> **Q: Is it open source?** [Answer]
> **Q: Can I add custom colors?** Coming soon!
> **Q: Does it work on mobile?** Yes!
>
> Thanks for all the feedback — shipping updates tonight based on what I'm hearing here.

---

## 9. Pre-Launch Checklist

### Before Posting Anywhere:

- [ ] Tool is live and fully functional at https://og-card-maker.vercel.app
- [ ] Tested on mobile (many will click from phone)
- [ ] Buy Me a Coffee link is visible on the site (footer or post-export)
- [ ] BMC page is set up with a friendly message and $1 minimum option
- [ ] Site loads fast (test on WebPageTest or Lighthouse)
- [ ] All 3 export sizes work correctly
- [ ] Copy-to-clipboard works in Chrome, Firefox, Safari
- [ ] Screenshot/GIF prepared showing the tool in action
- [ ] Reddit account has 10+ non-promotional comments in last month
- [ ] Twitter bio mentions building tools/side projects
- [ ] You have 2-3 hours blocked for engagement after each post
- [ ] GitHub repo is public (if applicable) — increases trust on HN

### Screenshots to Prepare:
1. The tool with a beautiful gradient selected (hero shot)
2. Before/after: blank form → finished OG card
3. The copy-to-clipboard success state
4. A real OG card being used in a Twitter card preview

---

## 10. Measuring Success

### Key Metrics to Track:
- **Vercel Analytics:** Unique visitors per day (if enabled)
- **Buy Me a Coffee:** Tips received (the goal!)
- **Reddit:** Upvotes, comment engagement, crosspost shares
- **Twitter:** Impressions, link clicks, retweets, thread views
- **HN:** Points, rank position, time on front page
- **Direct:** People mentioning the tool organically

### If Things Aren't Working After Day 1:
1. Check if posts were silently removed (Reddit spam filter)
2. Try a different angle in r/SideProject (more personal story)
3. Reply to relevant tweets with your tool as a helpful suggestion (don't spam)
4. Share in niche Discord communities (Indie Hackers, WIP, etc.)
5. Post in relevant dev.to or Hashnode communities

---

*Last updated: May 2026*
*Remember: Authenticity > marketing. People support makers they like, not products they admire.*
