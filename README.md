<h1 align="center">🤖 Auto Commit Bot</h1>

<p align="center">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions">
  <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  <img src="https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white" alt="Shell Script">
  <img src="https://img.shields.io/badge/Last_Update-2025--06--14-brightgreen?style=for-the-badge" alt="Last Update">
</p>

<div align="center">


  <h3>🚀 Keep your GitHub contribution graph active with daily motivational commits</h3>
</div>

## 📚 Table of Contents

- [🌟 Features](#-features)
- [🚀 Getting Started](#-getting-started)
- [⚙️ Configuration](#️-configuration)
- [📊 Understanding the Output](#-understanding-the-output)
- [🎮 Interactive Usage](#-interactive-usage)
- [👨‍💻 Author](#-author)

## 🌟 Features

<details open>
<summary><b>Click to expand/collapse</b></summary>

- ⏰ **Automated daily commits** - Keeps your GitHub activity green
- 💬 **Random inspirational quotes** - Stay motivated with a new quote every day
- 😄 **Random emojis** - Adds fun visual elements to your commits
- 📈 **Progress tracking** - Counts and tracks your commit streak
- 🏆 **Milestone summaries** - Special files created every 10th commit to celebrate progress
- 📅 **Weekly summaries** - Added to your log every 7th commit
- 🎮 **Interactive manual triggers** - Run the workflow on-demand with custom messages
- 🔄 **Smart log rotation** - Automatically archives logs when they get too large

</details>

## 🚀 Getting Started

<details>
<summary><b>Click to expand/collapse</b></summary>

### Prerequisites

- A GitHub account
- A personal access token (PAT) with `repo` scope

### Setup Instructions

1. **Fork or clone this repository**

2. **Set up the PAT_TOKEN secret**
   ```
   Repository Settings → Secrets → Actions → New Repository Secret
   Name: PAT_TOKEN
   Value: [your personal access token]
   ```

3. **Enable the workflow**
   ```
   Actions tab → "I understand my workflows, go ahead and enable them"
   ```

4. **First run**
   - Manually trigger your first run by clicking "Run workflow"
   - The bot will create your first commit and start tracking!

5. **Sit back and watch**
   - The bot will now commit daily at 07:00 UTC
   - Your GitHub contribution graph will stay active!

</details>

## ⚙️ Configuration

<details>
<summary><b>Click to expand/collapse</b></summary>

### Schedule

The bot is configured to run daily at 07:00 UTC. To change this schedule, edit the cron expression in `.github/workflows/auto-commit.yml`:

```yaml
on:
  schedule:
    - cron: '0 7 * * *'  # Format: minute hour day_month month day_week
```

### Manual Trigger Options

When manually triggering the workflow, you can customize:

| Option | Description |
|--------|-------------|
| Custom message | Add a personal note to your commit |
| Skip quote | Choose not to include a motivational quote |
| Extra emoji | Specify a custom emoji instead of using a random one |

### Customizing Quotes and Emojis

To add your own inspirational quotes or favorite emojis, edit these arrays in the workflow file:

```yaml
EMOJIS=("🎯" "🔥" "💪" "📅" "🧠" "🚀" "💻" "✅" "🌟" "⚡" "🏆" "🔄" "🌈" "🎨" "📊" "🔍")
QUOTES=(
  "Push yourself, because no one else is going to do it for you."
  "Stay positive, work hard, make it happen."
  # Add your favorite quotes here!
)
```

</details>

## 📊 Understanding the Output

<details>
<summary><b>Click to expand/collapse</b></summary>

### Commit Log Format

Each entry in your `commit_log.txt` will look like:

```
42. 🚀 Commit on 2025-06-14 08:55:55 (Saturday): Success doesn't just find you. You have to go out and get it.
```

### Weekly Summaries

Every 7th commit adds a weekly summary to your log:

```
---- Weekly Summary (Commit #7) ----
✨ Total commits this week: 7
📆 Days left in year: 200
🎯 Keep the streak going!
-----------------------------------
```

### Milestone Summaries

Every 10th commit creates a special markdown file (`milestone_summary_XX.md`) that contains:

- A congratulatory header
- Current statistics (date, time, day of week)
- Recent commit history

Example milestone summary:

```markdown
# Milestone Reached: Commit #50 🎉

Congratulations on reaching 50 daily commits!

## Stats
- Date: 2025-06-14
- Time: 08:55:55
- Day of week: Saturday
- Days left in year: 200

## Recent Commits
[Last 10 entries from your commit_log.txt]
```

</details>

## 🎮 Interactive Usage

<details>
<summary><b>Click to expand/collapse</b></summary>

### Manual Trigger

To manually trigger a commit:

1. Go to the **Actions** tab in your repository
2. Select the **Auto Commit** workflow
3. Click **Run workflow**
4. (Optional) Fill in the custom options:
   - Add a custom message
   - Choose a specific emoji
   - Opt to skip the motivational quote

### Example Custom Commits

<table>
<tr>
<th>Purpose</th>
<th>Custom Message</th>
<th>Emoji</th>
<th>Result</th>
</tr>
<tr>
<td>Celebrate</td>
<td>Reached 1000 stars!</td>
<td>🎉</td>
<td><code>chore: 🎉 Auto commit #42 - Reached 1000 stars! (manual trigger)</code></td>
</tr>
<tr>
<td>Project update</td>
<td>Updated Node.js version</td>
<td>📦</td>
<td><code>chore: 📦 Auto commit #43 - Updated Node.js version (manual trigger)</code></td>
</tr>
<tr>
<td>Daily reminder</td>
<td>Remember to update docs</td>
<td>📝</td>
<td><code>chore: 📝 Auto commit #44 - Remember to update docs (manual trigger)</code></td>
</tr>
</table>

</details>

## 👨‍💻 Author

<div align="center">
  <h3>Goutham Shankar</h3>
  <p>
    <a href="https://github.com/goutham-shankar">
      <img src="https://img.shields.io/badge/GitHub-goutham--shankar-blue?style=for-the-badge&logo=github" alt="GitHub">
    </a>
  </p>
  
  <p>
    <i>Stay committed to your goals, one auto-commit at a time.</i>
  </p>
</div>

---

<div align="center">
  
### 📈 Live Commit Stats

Current streak: Check `commit_log.txt` to see your active streak!

```
 ____  _              _____                            _   
/ ___|| |_ __ _ _   _|_   _|__ _ __ ___  _ __ ___  ___| |_ 
\___ \| __/ _` | | | | | |/ _ \ '_ ` _ \| '__/ _ \/ __| __|
 ___) | || (_| | |_| | | |  __/ | | | | | | |  __/ (__| |_ 
|____/ \__\__,_|\__, | |_|\___|_| |_| |_|_|  \___|\___|\__|
                |___/                                      
```

**Last updated: 2025-06-14 08:55:55**

</div>

<p align="center">
  <a href="../../actions/workflows/auto-commit.yml">
    <img src="https://img.shields.io/badge/TRIGGER_NOW-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="Trigger Now">
  </a>
</p>
