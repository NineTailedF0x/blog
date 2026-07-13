---
title: "Can we *really* automate with AI?"
subtitle: "P0: Why am I writing this"
date: 2026-07-13
draft: false
tags: ["AI", "pentesting", "rant"]
summary: "Kicking off a series on whether AI can actually replace web pentesters — who I am, why I'm writing this, and what's coming in P1-P3."
---

AI this, AI that and after that comes "Cybersecurity is DEAD, it will be replaced with AI in X years!". But does this *really* stand? I just want to write a big series about what is currently doable and whats not, and, generally, why are we *far* off from AI replacing pentesters (and specifically web pentesters as myself).

### Who am I

If youre not coming from my [linkedin](https://www.linkedin.com/in/yehor-ulianov/) — nice to meet you. I am a web application pentester by <span class="gloss" tabindex="0" data-tip="Go check out other cool blogposts there!">[r-tec](https://www.r-tec.net)</span>, *just* shy of 2 years in the company, with a lot of experience before this in CTFs and Bug Bounty.

My niche? Probably weird <span class="gloss" tabindex="0" data-tip="WSTG-speak for client-side and input validation issues">CLNT/INPV-01</span> vulns and a lot of <span class="gloss" tabindex="0" data-tip="Authorization testing">ATHZ</span> (Another blogpost about this is Coming_soon_TM). Also browser exploitation (I hope I will get the chance to publish my dirty work in the future).

The last couple of months I was really digging deep into doing LLM-Driven (Local AND Claude) [WSTG](https://owasp.org/www-project-web-security-testing-guide/v42/)-Coverage projects (so yeah, Im not going to tell you about <span class="gloss" tabindex="0" data-tip="Just prompting an AI and trusting whatever it spits out, no real methodology behind it">VIBEHACKING</span> here, the point was to really cover the whole app from A to Z), and well, I am here to tell you my journey and why AI-Apocalypse is certainly not coming yet.

### Why now?

Well, the answer is really simple — Im just tired of explaining each and every time to all my friends and not-so-techy people why my work is not DONE. Im certainly not an AI hater, but I want to give a realistic view on things as I see it right now.

### What I am planning on covering

- **P1:** Current landscape. Mostly me ranting about how I hate whats populated in the current "Automatic Pentests with AI" trend and why it is certainly NOT the way.
- **P2:** Whats working right now. My experience playing around with AI and what it *can* do (or, at least, what is working good enough from my perspective).
- **P3:** Whats **NOT** working. Other side of the battlefield and the main point — what is not working and probably will never really work. Again, with my hands-on experience and maybe some snippets here and there.

First one (P1) should be up in about a week. Expect some code and prompt snippets along the way — but not *a lot*, I am not going to dump my whole internal infra on you.

And NO, its not another AI-written slop (well, it will proofread for me, but the content IS mine), so I hope it will be somewhat interesting to read. These are my ideas and my discoveries, and I am always open to discuss what I am writing about and correct myself where I am wrong.

If you want to yell at me, correct me, or just say hi — my [linkedin](https://www.linkedin.com/in/yehor-ulianov/) is open. Also you can always write a comment or reach me per email **Nin3TailedF0x@protonmail.com**. See you in P1.