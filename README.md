# 🤖 Auto Commit Bot

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)
![Shell Script](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)

<div align="center">
  <img src="https://i.imgur.com/4uHz4zO.gif" alt="Auto Commit Bot" width="450px">
  <h3>Stay motivated with daily auto commits and inspirational quotes!</h3>
</div>

## 📚 Table of Contents

- [🌟 Features](#-features)
- [🚀 Getting Started](#-getting-started)
- [⚙️ Configuration](#️-configuration)
- [📊 Understanding the Output](#-understanding-the-output)
- [👤 Contributing](#-contributing)
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
   - Go to your repository settings > Secrets > Actions
   - Create a new secret named `PAT_TOKEN` with your personal access token

3. **Enable the workflow**
   - Go to the Actions tab in your repository
   - Enable GitHub Actions workflows if they're disabled
   - Select the "Auto Commit" workflow

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

To customize the quotes and emojis used by the bot, edit the arrays in the workflow file:

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
42. 🚀 Commit on 2025-06-14 08:53:04 (Saturday): Success doesn't just find you. You have to go out and get it.
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

</details>

## 🤝 Try It Now!

<div align="center">
  
  **Click the button below to manually trigger a commit right now!**
  
  [<img src="https://img.shields.io/badge/RUN_WORKFLOW-2088FF?style=for-the-badge&logoColor=white" alt="Run Workflow">](../../actions/workflows/auto-commit.yml)

</div>

## 👤 Contributing

<details>
<summary><b>Click to expand/collapse</b></summary>

Contributions are welcome! Here are some ways you can contribute:

- 🐛 Report bugs
- 💡 Suggest new features
- 🛠️ Submit pull requests

Please feel free to customize this bot for your own needs!

</details>

## 👨‍💻 Author

<div align="center">
  <a href="https://github.com/goutham-shankar">
    <img src="https://github.com/goutham-shankar.png" width="100px;" alt="Author Avatar"/><br>
    <sub><b>Goutham Shankar</b></sub>
  </a>
  <br>
  <a href="https://github.com/goutham-shankar">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  </a>
</div>

## 📊 Live Stats

Current streak: View the `commit_log.txt` file to see your current streak!

<div align="center">
  <img src="https://media.giphy.com/media/5xaOcLGm3mKRSpTYGDm/giphy.gif" width="300px">
  <h3>Keep up the great work! 💪</h3>
</div>
