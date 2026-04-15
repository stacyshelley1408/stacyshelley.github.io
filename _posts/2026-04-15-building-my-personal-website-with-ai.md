---
layout: post
title: "Building My Personal Website with AI"
date: 2026-04-15
category: AI
excerpt: "I spent 15 years marketing other people's products. Here's what happened when I finally got around to marketing myself."
description: "How I used Claude to build a personal website from scratch while learning hands-on AI skills in the process. What worked, what I'd skip, and what actually surprised me."
tags: [ai, personal brand, jekyll, claude]
---

For most of my career, personal brand was an afterthought.

I was focused on Secureworks. Then PhishLabs. Then Fortra. Those brands were the priority. My own? Something I'd get to eventually.

Eventually arrived when I started looking for my next leadership role.

As fellow SecureWorks alum Andrew Milne wrote on his blog a few weeks ago, I was a ["Marketer Who Forgot to Market Themselves."](https://archismarketing.blog/2026/03/19/the-marketer-who-forgot-to-market-themselves/)

It was time to start changing that. I had two goals going in. One was obvious: I wanted a stronger platform for my own brand that wasn't just LinkedIn. The other was less obvious: I wanted hands-on AI experience. Not YouTube tutorials, online courses, or webinars. I wanted to use AI tools to build something of value for myself.

Building a personal website checked both boxes.

I've built websites before, but it's been over a decade. I was rusty to say the least. The stack I landed on — Jekyll and GitHub Pages — wasn't something I'd have set up quickly on my own. That's where Claude came in.

I started with Claude Chat, which walked me through every decision: which hosting platform, how to structure the Jekyll project, how to migrate a single HTML file into a proper site with an About page and a blog. I still had to make judgment calls. I still hit errors I had to work through. But the time to get from "I want a site" to "I have a live site" was a fraction of what it would have been otherwise.

The bigger unlock was Cowork. Instead of passing files back and forth in a chat window, I automated practically every task in the pipeline except pushing code live. Building, editing, debugging, security checks, all of it. It wasn't as simple as handing things to a web agency, but it did allow me to test and iterate and explore different possibilities in an incredibly short amount of time.

Bug hunting and basic security checks especially. I didn't have to run tools myself or go digging around. I described what I wanted to review, Claude ran the checks, and then implemented the fixes. Huge caveat that my personal site is *basic*. There is not a lot of ground to cover or complexity that would require more advanced tools for bug and vuln hunting.

## A few things I'd tell someone starting the same project

**You probably don't need a CMS.** I spent time evaluating CloudCannon, Decap, and [Prose.io](https://prose.io). At one point my site was running on Netlify with Decap. But publishing content was trivial with AI. I could draft in Google Docs and just hand it over to Claude. It handled the coding and file management. From there, all I needed to do was review it on the local server and push it live. Dropping the CMS simplified the entire stack.

**Iteration speed really changed things.** I spent a few hours a week on this in between other projects and commitments. The site evolved much faster than I expected because every change, even big ones like changing up the entire design systems, took minutes instead of hours. The cost of iterating until I really liked something was very low. Once I grasped that, I was able to be more free, move faster, and take more creative risks.

**AI helps with structure, not substance.** My writing is my writing. I used Claude for light editing and to break content into formats that work better in the design context of the site. It didn't generate my thinking or my voice. It handled the plumbing, giving me more time to work on the substance.

Here's my site by the way: [stacyshelley.com](https://stacyshelley.com) (super creative domain, I know...). If I thought of my site as a product, I'd say it's v1. I'm happy with it (for now at least) and I look forward to publishing there for years to come. Plus, I learned some genuinely useful things about using AI in the process.

Not a bad trade for a few hours a week.
