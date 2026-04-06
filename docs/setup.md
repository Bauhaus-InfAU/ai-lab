# Setup Guide

Complete these 6 steps before the workshop so we can jump straight into building.

**Time needed:** ~30 minutes

---

### Step 1: Install Git

Git tracks changes to your files. Claude Code also needs it to run.

**Windows:** https://git-scm.com/downloads/win — use the default settings during installation.

**Mac:** Open Terminal and run `git --version`. If Git isn't installed, macOS will prompt you to install it automatically.

> **Verify:** Open a terminal and run `git --version` — you should see a version number.

---

### Step 2: Install VS Code

VS Code is a free code editor. We'll use it to view and edit the files that Claude creates for us.

**Download:** https://code.visualstudio.com/download

> **Verify:** You can open VS Code from your Start menu (Windows) or Applications folder (Mac).

---

### Step 3: Install Node.js

Node.js runs JavaScript outside the browser. We need it to create and run our web app. Download the **LTS** (Long Term Support) version.

**Download:** https://nodejs.org/

> **Important:** After installing, close and reopen your terminal so it picks up the new `node` command.

> **Verify:** Open a fresh terminal and run `node --version` — you should see something like `v22.x.x` (any recent version is fine).

---

### Step 4: Install Claude Code

Claude Code is the AI coding tool we'll use throughout the workshop. It runs in your terminal and writes code for you.

**Windows (PowerShell):**

```powershell
irm https://claude.ai/install.ps1 | iex
```

If you get an error about "execution policy", run this first, then retry the command above:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

**Windows (CMD) — if you don't have PowerShell:**

```cmd
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd
```

**Mac:**

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

> **Verify:** Run `claude --version` — you should see a version number.

---

### Step 5: Sign Up for Claude

Claude Code requires a paid Claude account. You need either:

- **Pro** — $20/month (plenty for the workshop)
- **Max** — $100/month (more usage, not needed today)

**Sign up:** https://claude.ai/pricing

> Free accounts don't include Claude Code access. You need Pro or Max.

After subscribing, open a terminal and run `claude` to log in and link your account. Follow the prompts — it will open a browser window for authentication.

---

### Step 6: Create a GitHub Account

GitHub is where we'll publish your finished app so anyone can see it with a link. It's free.

**Sign up:** https://github.com/signup

> **Verify:** You can log in at https://github.com and see your profile.

---

## All set!

That's everything. We'll do the rest together at the workshop.

**Having trouble?** Bring your laptop to the workshop and we'll help you sort it out.
