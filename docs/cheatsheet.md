# Cheatsheet

Quick reference for the key concepts you'll encounter during the lab.

## Terminal & Tooling

- **Terminal** — a text-based window where you type commands instead of clicking buttons
- **npm** — a tool that downloads and manages code libraries (packages) your project depends on
- **`npm install`** — downloads all packages listed in `package.json`
- **`npm run dev`** — starts a local dev server so you can preview your app in the browser
- **localhost** — your own computer acting as a web server (e.g. `http://localhost:5173`)
- **Hot reload** — when you save a file, the browser updates automatically

## Git & GitHub

- **Git** — a version control system that tracks changes to your files (like "undo history" for your whole project)
- **GitHub** — a website that stores your Git project online so others can see it
- **Clone** — download a copy of a GitHub project to your computer (`git clone <url>`)
- **Commit** — save a snapshot of your current changes (`git commit`)
- **Push** — upload your commits to GitHub (`git push`)
- **GitHub Pages** — a free service that turns your repo into a live website

The basic cycle: make changes → commit → push → your site updates automatically.

## Project Structure

- **`package.json`** — your project's ingredient list (name, dependencies, scripts)
- **`node_modules/`** — where npm puts all the downloaded packages (never edit this)
- **`src/`** — where your actual code lives
- **`index.html`** — the starting point of your web app
- **`main.jsx`** → **`App.jsx`** — the entry chain: `index.html` loads `main.jsx`, which renders `App.jsx`
- **`public/`** — static files (images, data) that get served as-is

## Web Basics

- **HTML** — the structure of a page (headings, paragraphs, buttons)
- **CSS** — the styling (colors, spacing, layout)
- **JavaScript (JS)** — the behavior (what happens when you click something)
- **React** — a JS library that lets you build UIs out of reusable **components**
- **Component** — a building block (like a LEGO brick) that combines HTML + JS into one piece, e.g. a map panel or a button
- **JSX** — HTML-like syntax you write inside JavaScript files (React's way of mixing structure and logic)

## Claude Code

- **`claude`** — the command to start Claude Code in your terminal
- **`CLAUDE.md`** — a file in your project root that tells Claude how to behave (like a briefing note it reads every time it starts)
- **Slash commands** — shortcuts you type in Claude Code that start with `/`, e.g. `/commit` to create a git commit, `/help` for help
- **Skills** — packaged workflows Claude Code can use (e.g. a skill for committing code, creating PRs, or researching a topic); triggered by slash commands or automatically
- **MCP (Model Context Protocol)** — a standard that lets Claude Code connect to external services (like Notion, Google Calendar, or custom APIs) so it can read and write data beyond your local files
- **MCP server** — a plugin that provides a specific connection (e.g. a Notion MCP server lets Claude read your Notion pages)
- **Tools** — individual actions Claude Code can perform (read a file, run a command, search the web); MCP servers add extra tools
- **Plan mode** — press `Shift+Tab` to toggle; Claude will research and write a plan but won't change any files until you approve. Use it when you want to think through a bigger change before committing to it
- **Context window** — the amount of text Claude can "see" at once; very long conversations may get compressed, so starting fresh sometimes helps
- **Permissions** — Claude Code asks before running commands or editing files; you approve or deny each action

## Working with AI

- **Be specific** — "add a button that toggles the isovist layer" works better than "make it better"
- **Iterate** — start simple, then refine ("now make the polygon semi-transparent")
- **Paste errors** — if something breaks, copy the error message and send it to Claude (or use mcp "playwright" so claude could evalute your browser window by itself)
- **Ask why** — if you don't understand what Claude did, ask it to explain
- **One thing at a time** — small requests are easier to review and undo than big ones

### When your project grows: RPI — Research, Plan, Implement

Once your codebase has many files, don't just ask Claude to "add X". Use this workflow instead:

1. **Research** — don't code yet. Let Claude scan the relevant files first to understand what's actually there (docs can be outdated, code is the truth)
2. **Plan** — the most important step. Have Claude write a step-by-step plan. Review and approve the *plan*, not just the code. This keeps you in control of the thinking
3. **Implement** — execute the approved plan, ideally in a fresh context window

**Tip: keep conversations short.** Long chats make Claude less sharp. When things get complex, ask Claude to summarize the current state, then start a new conversation with that summary.

## Domain Concepts

- **OSM (OpenStreetMap)** — a free, open map database built by volunteers (like Wikipedia for maps)
- **Overpass API** — a service that lets you query OSM data (e.g. "give me all buildings in Weimar")
- **GeoJSON** — a standard format for geographic shapes (points, lines, polygons) as JSON data
