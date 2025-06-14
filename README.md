# 🤖 Auto Commit GitHub Action Bot

Boost your GitHub contributions automatically! This GitHub Action **adds a fresh commit every day** to your repo by appending a motivational quote with fun emojis to `commit_log.txt`. Watch your contribution calendar light up effortlessly! ✨

---

## 🚀 What Does It Do?

- Runs **daily at 7:00 UTC** (you can customize the schedule).  
- Adds a new motivational quote + emoji to `commit_log.txt`.  
- Commits and **pushes directly to your `main` branch** — no pull requests needed!  
- Helps increase your GitHub contribution activity in a meaningful, automated way.

---

## 🛠️ How to Set It Up (Step-by-Step)

### 1. Create a Personal Access Token (PAT)

🔑 Head over to your GitHub [Developer Settings → Personal Access Tokens](https://github.com/settings/tokens) and:

- Click **Generate new token** (classic token).
- Give it a meaningful name like `Auto Commit Bot Token`.
- Select these scopes:
  - ✅ `repo` (for repository access and push permissions)
  - (Optional) `workflow` (if you want advanced workflow controls)
- Click **Generate token**, then **copy** it NOW — you won’t see it again!

---

### 2. Add the PAT as a Secret in Your Repository

- Go to your repo on GitHub → **Settings → Secrets and variables → Actions**.  
- Click **New repository secret**.  
- Name it exactly: `PAT_TOKEN`  
- Paste the token you copied, then click **Add secret**.

---

### 3. Configure the Workflow

- Open `.github/workflows/auto-commit.yml` in your repo.
- Replace:
  ```yaml
  git config --global user.name "your-username"
  git config --global user.email "your-email@example.com"
