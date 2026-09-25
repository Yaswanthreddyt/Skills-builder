# Runway

A study planner for people trying to break into tech, or level up once they're in.

Pick a role like Cloud Engineer, Data Analyst, or Frontend Developer, tell it how many hours a week you can actually give it, and it builds you a day by day plan: what to learn, in what order, with real lessons and real resources attached. Not a generic "here's a roadmap" image. An actual schedule you can check off.

## What it does

- Covers 24 roles and skills across three areas: general tech (frontend, backend, product, design, security), cloud (AWS/Azure/GCP roles, DevOps, SRE), and data (analytics, engineering, ML, BI)
- Builds a realistic schedule based on your hours per week and target date, and if you don't have enough time for everything it tells you honestly what got cut and why
- Every topic has a real lesson, a practice task, and links to actual free or well known resources (MDN, freeCodeCamp, Kaggle Learn, AWS docs, that kind of thing), not made up links
- Lists real certifications for each role, and is upfront about when a certificate actually matters versus when a portfolio project would serve you better
- Tracks your job applications too: company, role, status, follow up dates
- The whole site changes its look depending on which world you're in. Cloud roles get a sky and flight theme, data roles get a console/notebook theme, everything else gets an airport departure board theme. It's a small thing but it makes the site feel less like a spreadsheet

## Design details

I spent some real time on the interface itself, not just the functionality:

- Frosted glass header and dialogs, with a subtle highlight along the top edge so they read as an actual translucent material rather than a flat panel
- Motion runs on `transform` and `opacity` wherever possible so it stays smooth even on modest hardware, and it respects `prefers-reduced-motion`, `prefers-reduced-transparency`, and `prefers-contrast` if your system has any of those turned on
- Type uses tighter letter spacing on big headings and normal spacing on body text, which is a small detail but it's the kind of thing that makes text feel considered instead of just dumped on the page
- The icons are minimal, single color, line based artwork drawn specifically for this project

## Accounts and your data

This version runs with its own login (email and password) and its own database, so your plan and progress follow you across devices instead of living in one browser. Nobody else can see your data, not even whoever's running the site. If you'd rather not sign up, it still works fine, your progress just stays in that one browser instead of syncing anywhere.

## Running it yourself

It's one HTML file. No build step, no npm install. Open `index.html` in a browser, or drop it on any static host (GitHub Pages, Netlify, Vercel, wherever).

## Why I built this

Most "learn to code" roadmaps are either a wall of links with no structure, or a course that assumes you have unlimited time. I wanted something that takes your actual constraints (a job, a family, whatever else is going on) and gives you a plan you can realistically stick to, with the boring parts (which resource, in what order, how long each session should be) already figured out.

If you find it useful, or find something broken, feel free to open an issue.
