# OG Card Maker - Social Media Promotion Plan

> Goal: Drive traffic via social media and get at least 1 person to tip $1 on Buy Me a Coffee within 2 days.
> URL: https://og-card-maker.vercel.app

---

## 1. Reddit Posts

### r/InternetIsBeautiful (17M subscribers)

**Title:** I made a free tool that generates beautiful social media preview images in your browser - no signup, no watermark

**Body:**

Hey everyone! I built this little tool called OG Card Maker that lets you create Open Graph / social media preview images directly in your browser.

**What it does:**
- Generate preview cards for Twitter, Facebook, LinkedIn, etc.
- 16+ gradient themes and 8 texture patterns to choose from
- Supports emoji icons
- Multiple sizes: OG (1200x630), Twitter (1200x675), Square (1080x1080)
- One-click copy to clipboard

**What it doesn't do:**
- No signup required
- No watermark
- No data collection (everything runs in your browser)
- No cost

Link: https://og-card-maker.vercel.app

I built this in one evening because I was tired of firing up Figma every time I needed a quick OG image for a blog post. Hope someone else finds it useful too!

---

### r/SideProject (200K+ subscribers)

**Title:** Built a free OG image generator in one evening - here's what I learned shipping fast

**Body:**

Hey r/SideProject! Wanted to share something I built last night.

**The problem:** Every time I published a blog post or shared a link, I needed a social preview image. Opening Figma, picking colors, exporting... it felt like overkill for something that should take 30 seconds.

**The solution:** [OG Card Maker](https://og-card-maker.vercel.app) - a browser-based tool that generates social media preview cards instantly.

**Features:**
- 16+ gradient themes
- 8 texture patterns
- Emoji support for icons
- Multiple export sizes (OG, Twitter, Square)
- Copy to clipboard with one click
- Pure frontend - no backend, no auth, no BS

**Tech stack:** Plain HTML/CSS/JS, deployed on Vercel (free tier). Total cost: $0.

**What I learned:**
1. Canvas API is surprisingly powerful for this kind of thing
2. Shipping something small but complete feels way better than sitting on a half-finished "big" project
3. Gradients + subtle textures = instant "designed" look without actual design skills

It's 100% free, no signup, no watermark. If you find it useful and want to support more tools like this, I have a [Buy Me a Coffee](https://buymeacoffee.com/) page, but zero pressure.

Would love to hear feedback - what templates or features would make this more useful for you?

---

### r/webdev (2.4M subscribers)

**Title:** I built a client-side OG image generator using Canvas API - no backend needed

**Body:**

Hey r/webdev! I wanted to share a small tool I built that might save you some time: [OG Card Maker](https://og-card-maker.vercel.app)

**The idea:** Generate Open Graph images entirely in the browser using the Canvas API. No server-side rendering, no Puppeteer, no headless Chrome.

**Why client-side?**
- Zero hosting costs (static deploy on Vercel)
- No cold starts or rate limits
- User data never leaves the browser
- Works offline once loaded

**How it works:**
- Canvas 2D context for rendering
- CSS gradients recreated on canvas with linear/radial gradient fills
- Pattern overlays using createPattern()
- Text measurement with measureText() for responsive layouts
- toBlob() + Clipboard API for one-click copy

**Features:**
- 16+ gradient themes with texture overlays
- Emoji rendering on canvas
- Multiple aspect ratios: 1200x630 (OG), 1200x675 (Twitter), 1080x1080 (Square)
- Export as PNG or copy directly to clipboard

It supports the standard OG image sizes that platforms expect, so you can just drop the exported image into your meta tags or upload it directly.

Built it in one evening because I got tired of the Figma -> export -> upload workflow for every blog post. The code is pretty straightforward if anyone wants to build something similar.

Free to use, no signup, no watermark: https://og-card-maker.vercel.app

Happy to discuss the Canvas API approach if anyone has questions!

---

## 2. Twitter/X Thread

**Tweet 1 (Hook):**

I got tired of opening Figma every time I needed a social preview image.

So I built a free tool that generates beautiful OG cards in 30 seconds.

No signup. No watermark. Runs entirely in your browser.

https://og-card-maker.vercel.app

🧵 Here's what it does:

---

**Tweet 2 (Features):**

What you get:

🎨 16+ gradient themes
🔲 8 texture patterns
😀 Emoji icon support
📐 Multiple sizes (OG, Twitter, Square)
📋 One-click copy to clipboard

Everything renders client-side. Your data never touches a server.

---

**Tweet 3 (Problem/Solution):**

The problem I was solving:

Every blog post, every project launch, every shared link needs an OG image.

The old workflow: Open Figma → pick colors → add text → export → upload

The new workflow: Type title → pick theme → copy. Done.

---

**Tweet 4 (Technical):**

Built this in one evening with:

- Pure HTML/CSS/JS
- Canvas API for rendering
- Clipboard API for one-click copy
- Deployed on Vercel (free tier)

Total cost to run: $0/month
Total time to build: ~4 hours

Sometimes the best tool is the simplest one.

---

**Tweet 5 (Use Cases):**

Perfect for:

→ Blog post preview images
→ GitHub repo social cards
→ Newsletter header images
→ Tweet preview cards
→ Product launch announcements
→ Portfolio project cards

Basically any link you want to look good when shared.

---

**Tweet 6 (Social Proof / CTA):**

Already using it for all my own projects.

If you find it useful:
⭐ Bookmark it for later
🔄 RT so others can find it
☕ Buy me a coffee if it saved you time

https://og-card-maker.vercel.app

---

**Tweet 7 (Engagement):**

What theme/feature should I add next?

Thinking about:
- Dark mode themes
- Custom color picker
- Logo/image upload
- Template presets for specific platforms

Drop your ideas below 👇

#buildinpublic #webdev #indiedev #sideproject #ogimage #freetools #devtools

---

## 3. Hacker News - Show HN

**Title:**

Show HN: OG Card Maker - Free browser-based social media preview image generator

**First comment (by you, right after posting):**

Hey HN! I built this because the OG image workflow always felt unnecessarily heavy for what should be a simple task.

Most solutions I found either:
- Required signup/accounts
- Added watermarks on the free tier
- Needed a backend (Puppeteer, headless Chrome, etc.)
- Were part of a larger paid service

OG Card Maker runs entirely in the browser using Canvas API. Pick a gradient, add your title and subtitle, choose a size, and copy it to your clipboard. That's it.

Technical details:
- Pure client-side rendering with Canvas 2D
- Gradient + texture compositing for visual variety
- measureText() for responsive text layout
- toBlob() + Clipboard API for native copy
- Static deploy on Vercel, zero running costs

Limitations I'm aware of:
- No custom font upload yet (uses system fonts)
- No custom color picker (choosing from presets for now)
- No image/logo upload

Would love feedback on what would make this more useful. I intentionally kept it minimal to ship fast, but happy to iterate based on what people actually need.

---

## 4. Product Hunt Preparation

**Tagline (60 chars max):**

Beautiful social preview images in 30 seconds. Free forever.

**Description:**

OG Card Maker is a free, browser-based tool for generating social media preview images (Open Graph cards). No signup, no watermark, no backend.

Choose from 16+ gradient themes and 8 texture patterns, add your title and subtitle with emoji icons, select your target size (OG 1200x630, Twitter 1200x675, or Square 1080x1080), and copy the result to your clipboard with one click.

Everything runs in your browser - your content never touches a server. Built for developers, designers, and content creators who need great-looking preview images without the Figma/Canva overhead.

**Topics:** Design Tools, Open Source, Developer Tools, Productivity

**First Comment (Maker Comment):**

Hey Product Hunt! 👋

I'm the maker of OG Card Maker. I built this in one evening out of pure frustration.

Every time I shipped a side project or published a blog post, I'd spend 15-20 minutes in Figma just to create the OG image. It felt ridiculous for something that's essentially "gradient + text + export."

So I made a tool that does exactly that - nothing more, nothing less.

**Why free?** Because it costs me literally $0 to run (static files on Vercel's free tier). There's no reason to charge for it.

**Why no signup?** Because generating a preview image shouldn't require giving away your email.

**What's next?** I'm thinking about adding custom colors, logo upload, and maybe a template gallery. Would love to hear what features would make this more useful for you!

If you find it helpful and want to support future tools like this, I have a Buy Me a Coffee page linked on the site. But honestly, an upvote and feedback means just as much. 🙏

---

## 5. Posting Time Recommendations

All times in **US Eastern Time (ET)** since the primary audience is US-based developers/designers.

| Platform | Best Day | Best Time (ET) | Why |
|----------|----------|-----------------|-----|
| Reddit (r/InternetIsBeautiful) | Tuesday or Wednesday | 8:00 - 9:00 AM | Catches morning browsing; mid-week = higher engagement |
| Reddit (r/SideProject) | Monday or Thursday | 9:00 - 11:00 AM | Builders are active early week |
| Reddit (r/webdev) | Tuesday or Wednesday | 10:00 - 12:00 PM | Devs browse during work breaks |
| Twitter/X | Tuesday - Thursday | 8:00 - 10:00 AM | Morning scroll; avoid weekends for tech content |
| Hacker News | Tuesday or Wednesday | 8:00 - 9:00 AM | Catches US morning + European afternoon |
| Product Hunt | Tuesday - Thursday | 12:01 AM PT (3:01 AM ET) | PH day starts at midnight PT; early launch = full day of voting |

**Posting Strategy for 2-day Sprint:**

- **Day 1 Morning:** Post Hacker News (Show HN) + Twitter thread + Reddit r/webdev
- **Day 1 Afternoon:** Post Reddit r/InternetIsBeautiful
- **Day 2 Morning:** Post Reddit r/SideProject + engage with all comments from Day 1
- **Day 2:** Save Product Hunt for a separate day (it deserves its own launch day, and you'll have social proof from other platforms by then)

**Time Zone Tip:** Schedule posts to hit when US East Coast is waking up (7-9 AM ET). This catches both US users and European users still online in the afternoon.

---

## 6. Platform Rules & Tips to Avoid Deletion

### Reddit General Rules:
- ✅ DO engage with every comment genuinely
- ✅ DO have some non-promotional post history before posting (comment on other posts first)
- ✅ DO use Reddit's "OC" or link flair if available
- ❌ DON'T post to multiple subreddits within the same hour (looks spammy)
- ❌ DON'T use URL shorteners
- ❌ DON'T ask for upvotes
- ❌ DON'T mention monetization in the title

### r/InternetIsBeautiful Specific:
- Must be a direct link post (URL as the post link, not a text post with link inside)
- Site must be interactive/useful, not just a landing page
- No "app" or "tool I made" in the title - frame it as the thing itself
- Keep title factual, not clickbaity

### r/SideProject Specific:
- Text posts perform better here
- Share the story/journey, not just the tool
- Mention it's free/open - this community respects generosity
- Asking for feedback is well-received here

### r/webdev Specific:
- Technical depth is expected - share implementation details
- "Show off Saturday" thread is an alternative if direct posts get removed
- Don't make it sound like an ad - frame it as a technical discussion
- Flair your post appropriately (usually "Showoff Saturday" or "Resource")

### Twitter/X Tips:
- First tweet needs a hook (problem statement or bold claim)
- Include a screenshot or screen recording in first tweet
- Thread should be 5-7 tweets max
- Use hashtags only in the last tweet (cleaner look)
- Pin the thread to your profile
- Reply to yourself with the Buy Me a Coffee link (not in the main thread)

### Hacker News Tips:
- Title format: "Show HN: [Name] – [one-line description]"
- Don't use superlatives ("best", "amazing", "revolutionary")
- Post your explanatory comment immediately after submitting
- Be honest about limitations
- Respond to every comment, especially critical ones
- Don't ask people to upvote (instant death)
- HN audience values simplicity and "does one thing well"

### Product Hunt Tips:
- Launch on Tuesday-Thursday for best results
- Have a GIF/video showing the tool in action
- Respond to every comment within minutes
- Get 3-5 friends to leave genuine comments early
- Hunter vs Maker: Launch as maker (self-hunt is fine now)
- Thumbnail should be clean with readable text

### General Anti-Spam Tips:
- Space out your posts: minimum 2-3 hours between platforms
- Don't copy-paste the exact same text across platforms
- Engage authentically in comments (not just "thanks!")
- If a post gets removed, don't repost immediately - message mods first
- Your account should not look like it was created just to promote

---

## 7. Quick Reference: Buy Me a Coffee Integration

**How to subtly include BMC without being pushy:**

- On Reddit: Mention it only if someone asks "how can I support?" or put it in an edit after positive reception
- On Twitter: Add BMC link as a reply to the thread, not in the main tweets. Or put it in bio.
- On HN: Don't mention it at all in the post. It should be discoverable on the site itself.
- On Product Hunt: Mention it naturally in maker comment ("if you want to support future tools...")

**On the tool itself:**
- Small, non-intrusive "Buy Me a Coffee ☕" link in footer or corner
- Only show it after the user has successfully generated/copied an image (they've gotten value first)
- A subtle "Made with ❤️ by [name] | Support this project" works well

---

## 8. Engagement Templates

**When someone says "this is cool":**
> Thanks! What would make it even more useful for your workflow? I'm planning to add more features based on feedback.

**When someone asks about the tech:**
> Built with vanilla JS + Canvas API, deployed on Vercel free tier. The whole thing is client-side so your data never leaves your browser. Happy to go deeper on any part!

**When someone asks "why free?":**
> Honestly, it costs me $0 to run (static site on Vercel's free tier) and it only took one evening to build. Felt wrong to charge for something this simple. If you want to support future tools, there's a Buy Me a Coffee link on the site, but zero pressure.

**When someone suggests a feature:**
> Great idea! Added to my list. If you want to follow along, I'm building in public on Twitter [@handle]. That kind of feedback is exactly what helps me prioritize.

**When a post gets traction:**
> Edit: Wow, didn't expect this response! For everyone asking about [common question] - [answer]. And if you hit any bugs, let me know in the comments. Shipping fixes tonight.

---

## Checklist Before Posting

- [ ] Tool is live and working (test the URL)
- [ ] Buy Me a Coffee link is visible on the site
- [ ] Your Reddit account has recent non-promotional activity
- [ ] Your Twitter bio mentions you build tools/side projects
- [ ] Screenshots/GIFs are ready for Twitter and Product Hunt
- [ ] You have 2-3 hours blocked to respond to comments after posting
- [ ] Mobile experience works (many users will click from phone)
- [ ] The site loads fast (Vercel CDN should handle this)

---

*Last updated: May 2026*
