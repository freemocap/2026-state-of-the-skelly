---
marp: true
theme: default
paginate: true
style: |
  @import url('https://fonts.googleapis.com/css2?family=Dosis:wght@200;600&family=Roboto:wght@300;400;500&display=swap');
  
  :root {
    --dark-teal: #254342;
    --medium-teal: #365d5f;
    --coral-decorative: #d95157;
    --coral-heading: #f07a7f;      /* 3.98:1 - AA large text */
    --coral-text: #ff8a8a;         /* 4.72:1 - AA normal text */
    --light-cyan: #a4d6d9;         /* 6.73:1 - AA normal text */
  }
  
  section {
    background-color: var(--dark-teal);
    color: #ffffff;
    font-family: 'Roboto', sans-serif;
    font-weight: 300;
  }
  
  h1 {
    font-family: 'Dosis', sans-serif;
    font-weight: 600;
    color: var(--light-cyan);
    letter-spacing: 0.05em;
  }
  
  h2 {
    font-family: 'Dosis', sans-serif;
    font-weight: 200;
    color: var(--coral-heading);
    letter-spacing: 0.05em;
  }
  
  h3 {
    font-family: 'Dosis', sans-serif;
    font-weight: 600;
    color: var(--light-cyan);
  }
  
  a {
    color: var(--coral-text);
  }
  
  strong {
    color: var(--coral-text);
  }
  
  code {
    background-color: var(--medium-teal);
    color: var(--light-cyan);
  }
  
  blockquote {
    border-left: 4px solid var(--coral-text);
    background-color: var(--medium-teal);
    padding: 0.5em 1em;
    color: #ffffff;
    font-style: normal;
  }
  
  blockquote em {
    color: var(--light-cyan);
    font-style: italic;
  }
  
  table {
    font-size: 0.9em;
  }
  
  th {
    background-color: var(--medium-teal);
    color: var(--light-cyan);
  }
  
  td {
    background-color: var(--light-cyan);
    color: var(--dark-teal);
  }
  
  section.title {
    text-align: center;
    justify-content: center;
    padding-bottom: 120px;
  }
  
  section.title h1 {
    font-size: 2.8em;
  }
  
  section.invert {
    background-color: var(--light-cyan);
    color: var(--dark-teal);
  }
  
  section.invert h1,
  section.invert h3 {
    color: var(--dark-teal);
  }
  
  section.invert strong,
  section.invert a {
    color: var(--dark-teal);
    font-weight: 500;
  }
  
  img[alt~="center"] {
    display: block;
    margin: 0 auto;
  }
  
  /* Section progress indicator */
  section::after {
    font-family: 'Dosis', sans-serif;
    font-size: 0.7em;
    color: var(--light-cyan);
    opacity: 0.6;
    position: absolute;
    top: 20px;
    right: 30px;
  }
  
  section.part-background::after { content: "Background"; }
  section.part-current::after { content: "Current State"; }
  section.part-future::after { content: "Future Plans"; }
  

  /* Video container styling */
  .video-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 1em;
  }
  
  .video-container video {
    border-radius: 8px;
    box-shadow: 0 4px 20px rgba(0,0,0,0.3);
  }
  
  .video-container iframe {
    border-radius: 8px;
    box-shadow: 0 4px 20px rgba(0,0,0,0.3);
  }
  
  /* Impact stats styling */
  .impact-stats {
    display: flex;
    justify-content: space-around;
    margin-top: 1em;
    font-size: 0.85em;
  }
  
  .stat-box {
    text-align: center;
    padding: 0.5em 1em;
    background-color: var(--medium-teal);
    border-radius: 8px;
  }
  
  .stat-number {
    font-size: 1.5em;
    font-weight: 600;
    color: var(--coral-text);
  }
  
  .stat-label {
    color: var(--light-cyan);
    font-size: 0.8em;
  }
---

<!--
BUILD INSTRUCTIONS
==================
npm install -g @marp-team/marp-cli

HTML (for presenting, supports video embeds):
  marp freemocap-2026-state-of-the-skelly.md -o slides.html --html

PDF (for sharing, no video):
  marp freemocap-2026-state-of-the-skelly.md -o slides.pdf --html --allow-local-files

Live preview:
  marp -w freemocap-2026-state-of-the-skelly.md --html

Presenting: Open HTML in browser, F=fullscreen, P=presenter view

VIDEO TIME CONTROLS:
===================
YouTube iframe:  ?start=SECONDS (e.g. ?start=90 for 1:30)
                 ?start=30&end=120 (play 0:30 to 2:00)
                 
Local video:     #t=START,END (e.g. #t=30,120)
                 #t=45 (just start at 45 seconds)

REQUIRED LOCAL FILES:
====================
- skelly-logo.png
- skellycam-logo.png
- freemocap-github-star-history.png
- freemocap-user-dashboard.png

VIDEOS TO DOWNLOAD (use yt-dlp):
================================
- first-public-post-2021-01-19.mp4    (from x.com/JonMatthis/status/1351531974364688385)
- meowmaline-2021-07-21.mp4           (from x.com/JonMatthis/status/1417864732749582337)
- purple-monkey-2022-03-11.mp4        (optional - can use YouTube embed)
- rough-cut-tutorial-2022-11.mp4      (optional - can use YouTube embed)
- v2-announcement-2026.mp4            (from x.com/freemocap/status/2010845786007875659)

TODO - FILL IN METRICS:
======================
Search "[FILL:" in this file to find placeholders for:
- Twitter/X engagement stats (views, likes, retweets, replies)
- YouTube video stats (views)
- Get these from Twitter Analytics and YouTube Studio
-->

<!-- _class: title -->

<div style="padding-top: 60px;">

![w:200 center](media/images/skelly-logo.png)

# 2026 State of the Skelly Address

## FreeMoCap Foundation

</div>

<div style="margin-top: 80px; font-size: 0.9em;">

*Start: 6:30 PM  ·  Talk: 45-60 min  ·  Q&A to follow*

</div>

---

# Agenda

1. **Background** — An abbreviated history
2. **Current State** — Numbers, financials, clients
3. **Future Plans** — v2, curriculum, shop, FDA, Blender

![bg right:40% contain opacity:0.15](media/images/skelly-logo.png)

---

<!-- _class: title -->

# Part I
## Background

---
<!-- _class: part-background -->

# 2017 — OpenPose Happens

![bg right:25% contain opacity:0.1](media/images/skelly-logo.png)

<!-- Add local video here: openpose-ut-video.mp4 -->

---
<!-- _class: part-background -->

# 2019 — Northeastern

Started at Northeastern University

*One year of regular professorship before...*

![bg right:25% contain opacity:0.1](media/images/skelly-logo.png)

<!-- Video options: retinal-optic-flow.mp4, trents-argp.mp4 -->

---
<!-- _class: part-background -->

# 2020 — COVID!

### March 2020 - Quarantine!

### August 2020 - Lost faith in the scientific/academic/educational process

*...whoops!*

![bg right:25% contain opacity:0.1](media/images/skelly-logo.png)

---
<!-- _class: part-background -->

# 2021 — Academic to FOSS Zealot

> *"The Open Source community is what the scientific community pretends to be"*

![bg right:25% contain opacity:0.1](media/images/skelly-logo.png)

---
<!-- _class: part-background -->

# 2021 Jan 19 — First Public Post

<div class="video-container">
  <video src="media/videos/first-public-post-2021-01-19.mp4" controls style="max-height: 45vh;"></video>
</div>


Source:  https://twitter.com/JonMatthis/status/1351531974364688385

---
<!-- _class: part-background -->

# 2021 July 21 — Meowmaline 🐱

<div class="video-container">
  <video src="media/videos/meowmaline-2021-07-21.mp4#t=0" controls style="max-height: 45vh;"></video>
</div>


Source: https://twitter.com/JonMatthis/status/1417864732749582337 

---
<!-- _class: part-background -->

# 2022 March 11 — "This is FreeMoCap"

The purple monkey video 🐒

<div class="video-container">
  <iframe 
    width="560" 
    height="315" 
    src="https://www.youtube.com/embed/WW_WpMcbzns?start=0" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
  </iframe>
</div>




---
<!-- _class: part-background -->

# 2022 November — Rough Cut Tutorial

<div class="video-container">
  <iframe 
    width="560" 
    height="315" 
    src="https://www.youtube.com/embed/GxKmyKdnTy0?start=0" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
  </iframe>
</div>

<div style="text-align: center; margin-top: 0.5em; font-size: 0.8em; color: var(--light-cyan);">
  <strong>[FILL: XX,XXX]</strong> views
</div>

<!-- Change ?start=0 to desired start time in seconds -->

---
<!-- _class: part-background -->

# 2023 November — v1.0 Release! 🎉

The first official stable release

![bg right:25% contain opacity:0.1](media/images/skelly-logo.png)

---
<!-- _class: part-background -->

# 2024-2025 — Public Pause to slow growth

### Strategy: Circle the Wagons

- Worried we were growing to fast
- De-emphasized public posting to slow the growth curve 
- Focused energy on Discord community

![bg right:45% contain opacity:1](media/images/freemocap-github-star-history.png)

---
<!-- _class: part-background -->

# 2026 — Re-Emergence!

v2 is coming! 🚀

<div class="video-container">
  <video src="media/videos/recent_treadmill_vid.mp4" controls style="max-height: 45vh;"></video>
</div>


Source: https://twitter.com/freemocap/status/2010845786007875659 

---

<!-- _class: title -->

# Part II
## Current State

---
<!-- _class: part-current -->

# By the Numbers

| Metric | Count |
|--------|-------|
| ⭐ GitHub Stars | 4,533 |
| 💬 Discord Members | 3,387 |
| 🌐 Global Users | 10,222+ |
| 🗺️ Countries Reached | 140 |

![bg right:40% contain](freemocap-github-star-history.png)

![bg right:40% contain](freemocap-user-dashboard.png)

- A field trip to Dataland - https://freemocap.org/data.html
---
<!-- _class: part-current -->

# Financials
- Doing Ok
- Will survive past the 2026 June 30 Scary Cliff
- ...but will we thrive??

![bg right:35% contain opacity:0.15](media/images/skelly-logo.png)

---
<!-- _class: part-current -->

# Clients

### Current Research Partners

- Ben Scholl - Colorado University, Denver Anschutz Campus   - Developmental Laser Ferrets  - 


- Diego Fernandez - Cincinati Children's Hospital Medical College - Mouse eye tracker and all-day Pupilometry 
<div class="video-container">
  <iframe 
    width="560" 
    height="315" 
    src="https://www.youtube.com/watch?v=haRITKNkGQw" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
  </iframe>
</div>


![bg right:40% contain opacity:0.2](media/images/skelly-logo.png)

---
<!-- _class: part-current -->

# Now Offering Paid Service Contracts

**Knowledge is Free, Labor is unbelievable expensive** 

Contact us for: 
- Contract or consultant work: https://freemocap.org/services
- Bronze/Silver/Gold/Corporate Sponsorship (a la Blender): https://opencollective.com/freemocap-foundation

![bg right:35% contain opacity:0.15](media/images/skelly-logo.png)

---

<!-- _class: title -->

# Part III
## Future Plans

https://github.com/orgs/freemocap/projects/34

---
<!-- _class: part-future -->

# v2 Transition 🚀

![bg right:40% contain opacity:0.15](media/images/skellycam-logo.png)

- On the `/development` branches of `freemocap` and sub-skellies (see https://github.com/freemocap )

### Release Plan
- **Pre-Alpha** - Known busted 
    - (My bad UI - `freemocap/freemocap-ui`)
- **Alpha** —  Possibly working 
    - (Pooya's good ui! https://freemocap.vercel.app)
- **Beta** — Potentially working
- **Full Release** — Probably working!


---
<!-- _class: part-future -->

# v2 Data Model Plans

### SkEP #1: Tidy Data CSVs + Parquet db

(SkEP: "Skelly Enhancement Proposal")

![bg right:35% contain opacity:0.15](media/images/skelly-logo.png)

---
<!-- _class: part-future -->

# Documentation Overhaul, aka... 
### FreeMoCap University 🎓

- Multi-track curriculum with micro-certificatiions
- AI Slop version available here: https://github.com/freemocap/university

---
<!-- _class: part-future -->

# Skellybot Coming soon to a server near you

https://github.com/freemocap/skellybot

<div style="display: flex; gap: 2em; align-items: center; justify-content: center; margin-top: 1em;">
  <img src="media/images/skellybot_stats_hmn25.png" style="height: 280px;">
    <img src="media/images/skellybot-logo.png" style="height: 280px;">
</div>


---
<!-- _class: part-future -->

# SkellyShop 🛒

### Charuco Boards

- Available now — print-on-demand
- Annoying, slow, expensive system, but it exists!
![bg right:65% contain ](media/images/freemocap-cheatsheet.png)
https://shop.freemocap.org

### Cameras and other hardware

Coming soon!

![bg right:40% contain opacity:0.2](media/images/skellycam-logo.png)

---
<!-- _class: part-future -->

# FreeMoCap Validation

### Aaron's Dissertation - Defending Soon!
👇 watch this space
https://aaroncherian.github.io/freemocap_validation/ 
https://github.com/freemocap/freemocap_validation



### FDA 510(k) Certification from there... 


![bg right:35% contain opacity:0.15](media/images/skelly-logo.png)

---
<!-- _class: part-future -->

# Blender Addon

### Rebranding

`FreeMoCap Blender Addon` → **SkellyBlender**

### Official Distribution

🎯 Goal: Be Available in Blender's official Extension page

https://github.com/freemocap/freemocap_blender_addon/issues/45

![bg right:35% contain opacity:0.15](media/images/skelly-logo.png)

---

<!-- _class: title -->

![w:180 center](media/images/skelly-logo.png)

# Thank You!

## Questions?
info åt freemocap.org

🌐 freemocap.org  ·  💻 github.com/freemocap  ·  💬 discord.gg/freemocap