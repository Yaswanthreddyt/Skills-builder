# Runway

A study planner for people trying to break into tech, or level up once they're in.

Pick a role like Cloud Engineer, Data Analyst, or Frontend Developer, tell it how many hours a week you can actually give it, and it builds you a day by day plan: what to learn, in what order, with real lessons and real resources attached. Not a generic "here's a roadmap" image. An actual schedule you can check off.

## What it does

- Covers 24 roles and skills across three areas: general tech (frontend, backend, product, design, security), cloud (AWS/Azure/GCP roles, DevOps, SRE), and data (analytics, engineering, ML, BI)
- A skill check lets you rate yourself on each topic across seven levels, from New to Mastery, instead of one vague overall guess. This actually drives the plan: a topic you're strong in gets a light touch, a topic you're new to gets real time
- A skill gap view shows current level next to the level this role actually needs, why that topic matters, and a specific next step pointing at a real resource, not just a chart for its own sake
- A stage tracker shows where you actually are in the bigger picture: Foundations, Core skills, Advanced skills, Practical challenges, Project, Role ready
- Your personalized roadmap sits right in your profile once you pick a skill: a day by day schedule with every topic laid out as a connected, expandable timeline. Tap any topic to preview its lesson and practice task inline, no dialog needed, or open the full lesson when you want it
- You can run more than one journey at once. Start a plan for Cloud Engineer, then later start one for Data Engineer without losing the first, and switch between them from a small pill row on your profile
- If two of your journeys share real topic overlap, Runway shows you what carries over and what's new, built from your actual curated content rather than a guess
- A skill map for each role shows which topics are core, which are important, and which are bonus depth, and roughly what order they build on each other. Tap any topic on the map to jump straight to its lesson
- Search any skill in the Library to see which roles actually use it, and how it's described differently in each one
- Cloud Engineer has a set of real practical challenges: scenario-based problems (a broken VPC route, an over-permissioned IAM policy, a cost spike, a timing-out function) rather than more quiz questions. Other roles don't have this yet; we'd rather say so than fill the space with generic filler
- Builds a realistic schedule based on your hours per week and target date, and if you don't have enough time for everything it tells you honestly what got cut and why
- Every topic has a real lesson, a practice task, and links to actual free or well known resources (MDN, freeCodeCamp, Kaggle Learn, AWS docs, that kind of thing), not made up links
- Suggested projects, generated from your actual chosen topics rather than a generic list, so what you're asked to build is tied to what you're actually learning
- Lists real certifications for each role, and is upfront about when a certificate actually matters versus when a portfolio project would serve you better
- Tracks your job applications too: company, role, status, follow up dates
- The whole site changes its look depending on which world you're in. Cloud roles get a sky and flight theme, data roles get a console/notebook theme, everything else gets an airport departure board theme. It's a small thing but it makes the site feel less like a spreadsheet

## Design details

I spent some real time on the interface itself, not just the functionality:

- Frosted glass header and dialogs, with a subtle highlight along the top edge so they read as an actual translucent material rather than a flat panel
- Motion runs on `transform` and `opacity` wherever possible so it stays smooth even on modest hardware, and it respects `prefers-reduced-motion`, `prefers-reduced-transparency`, and `prefers-contrast` if your system has any of those turned on
- Type uses tighter letter spacing on big headings and normal spacing on body text, which is a small detail but it's the kind of thing that makes text feel considered instead of just dumped on the page
- The icons are minimal, single color, line based artwork drawn specifically for this project

## Where things live

Everything about you and your plan sits under the **Profile** tab: who you are, which skills you're working toward, and the whole personalized roadmap (skill gaps, the day by day timeline, suggested projects, certifications). Library is for browsing lessons without committing to a schedule, and Applications is your separate job tracker.

## Multiple journeys

You're not locked into one role at a time. Start a plan for Cloud Engineer, then later start one for Data Engineer without losing the first. A small switcher at the top of your Profile lets you jump between them, each with its own schedule, progress, and skill assessment. If a topic name overlaps between two of your journeys, Runway shows you what carries over and what's genuinely new when you compare them.

## Accounts and your data

This version runs with its own login (email and password) and its own database, so your plan and progress follow you across devices instead of living in one browser. Nobody else can see your data, not even whoever's running the site. If you'd rather not sign up, it still works fine, your progress just stays in that one browser instead of syncing anywhere.

## Running it yourself

It's one HTML file. No build step, no npm install. Open `index.html` in a browser, or drop it on any static host (GitHub Pages, Netlify, Vercel, wherever).

## Why I built this

Most "learn to code" roadmaps are either a wall of links with no structure, or a course that assumes you have unlimited time. I wanted something that takes your actual constraints (a job, a family, whatever else is going on) and gives you a plan you can realistically stick to, with the boring parts (which resource, in what order, how long each session should be) already figured out.

If you find it useful, or find something broken, feel free to open an issue.
