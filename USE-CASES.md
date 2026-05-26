# JavClaw: What Problem It Solves, and Who It's Actually For

Most "what tool should I use" guides give you a feature matrix and tell you to pick. That's not very useful when the question you actually want to ask is *"Will this tool fix the specific thing that's annoying me right now?"* This is a use-case guide for JavClaw — written from the angle of which problems it's actually built to solve, and which kinds of users it fits. There's a broader field guide ([GUIDE.md](./GUIDE.md)) and a full tool comparison ([README](./README.md)) in this repo if you're starting earlier in the decision.

## The problems JavClaw is built to solve

**1. Filenames you can't search through.**
A collection that grew over years usually has filenames in three or four different conventions: bare codes, code + studio + ripper tag, full Japanese title with prefixes, and the occasional `final_REAL.mp4`. The filesystem search box stops being useful around the 300-file mark. JavClaw's first job is to read the code out of whatever-the-filename-looks-like and attach proper metadata to it, so you stop searching strings and start searching attributes.

**2. "Find by actress" being impossible on a flat folder.**
Folders are one-dimensional. You can sort by name, date, or size. You can't filter to "all videos by actress X with tag Y, sorted by year." That requires an index. JavClaw builds a local searchable index over your existing files — meaning the same file on disk shows up under whichever actress, studio, or tag you query for, without you having to physically reorganize anything.

**3. Privacy that doesn't depend on trusting a vendor.**
Anything cloud-based, including web-scrapers that phone home, has a privacy story that ultimately reduces to "trust us." JavClaw is local-first: the index lives on your machine, the files stay on your machine, nothing is uploaded. This isn't a marketing claim — it's why the tool exists as a desktop app rather than a web service.

**4. The gap between "processing tool" and "daily app."**
Javinizer (the free standard) is excellent at renaming and sorting once. It is not a thing you open every day to browse. There's a real gap between "I've run my files through a scraper" and "I have an app I actually use to find what I want to watch tonight." JavClaw is built for the second job, not the first. If you've already run Javinizer and now want somewhere to live in the library, that's the gap it fills.

**5. Setup cost.**
Stash is more powerful, but the setup is a project — Docker, scrapers, scheduled scans, the whole self-hosting routine. PowerShell-based tools assume you're comfortable in a shell. JavClaw assumes you can install a desktop app and point it at a folder. That's the whole onboarding.

## Who this actually fits

**The "library grew on its own" user.** You have somewhere between a few hundred and a few thousand files, accumulated over years, in inconsistent naming. You don't want to spend a weekend renaming things by hand or learning PowerShell. You want a thing that reads what's there and gives you a usable interface over it. This is the core fit.

**The Mac user.** Most well-built JAV organizers are Windows-first. JavLuv is Windows-only. Javinizer runs cross-platform but is terminal-centric. If you're on a Mac and want a real app, the options narrow fast.

**The "I'll pay once but not subscribe" user.** Single-purchase, no recurring fee. If you're tired of every piece of software charging $5/month forever, this pricing model matters.

**The privacy-conscious user.** If the idea of any of this metadata leaving your machine bothers you, local-first is the only design that actually solves that. JavClaw doesn't have a server side, so there's no server-side breach risk to worry about.

**The "I've already processed, now I need to live in it" user.** A surprising number of people run Javinizer once for the rename pass and then have no real app to browse the result. JavClaw is what slots in after the processing step.

## Who this doesn't fit

This is the part most tool pages skip, so:

- **You love the terminal.** Javinizer is free, more flexible, and rewards a PowerShell user. Don't pay $10 to lose your CLI workflow.
- **You want remote access from anywhere.** JavClaw is a desktop app, not a self-hosted server. If you want to browse your library from your phone over Tailscale or a VPN, Stash is the right answer.
- **Your collection is small.** Under a hundred files, the filesystem is fine. Don't introduce a tool to solve a problem you don't have yet.
- **You refuse closed-source software on principle.** JavClaw is paid and closed-source. That's a legitimate dealbreaker for some people, and you should respect your own preferences here.
- **You're on Linux.** No Linux build today. Stash is your best bet.

## A short framing

The honest framing is: JavClaw isn't the most powerful tool in the comparison, and it isn't the cheapest. It's the one that gets a non-technical user from "messy folder" to "browsable library" in the shortest path on Mac or Windows, without monthly fees, without exposing files to a cloud service, and without a weekend of configuration. If that specific tradeoff matches what you actually want, it's a good fit. If it doesn't, the [README](./README.md) lays out the alternatives without hedging.

---

*See also: [GUIDE.md](./GUIDE.md) — the broader field guide to organizing a large JAV collection in 2026, and [README](./README.md) — the full tool comparison.*
