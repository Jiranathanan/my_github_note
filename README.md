# 💡 Using GitHub on Multiple Computers without Setting Up SSH Keys

Sometimes you want to code on multiple machines (like PC and Mac) but still commit under the same GitHub account (e.g., `jiranathanan`) **without setting up SSH keys** on each device. Here's a simple method using a Personal Access Token (PAT) via HTTPS.

---

## 🔑 Cloning with a Personal Access Token (PAT)

Instead of using SSH or logging in with GitHub CLI, you can clone directly using this pattern:

```bash
git clone https://<username>:<github_token>@github.com/<username>/<repositoryname>.git
```

## Setting up Git Identity (for green squares!)
### To make your commits count toward your contribution graph:
```bash
cd /path/to/your/repo
git config user.name "Jiranathanan Siripun"
git config user.email "jiranathanan@email.com"
```
#### Use the email associated with your GitHub account.

# Changing the Remote URL (optional)
## If you already cloned the repo without the token, just update the remote:
```bash
git remote set-url origin https://<username>:<github_token>@github.com/<username>/<repositoryname>.git
```

# Example
```bash
git clone https://Jiranathanan:ghp_AbCdEfGhIjKlMnOpQrStUvWxYz1234567890@github.com/jiranathanan/my-repo.git
cd my-repo
git config user.name "Jiranathanan Siripun"
git config user.email "jiranathanan@example.com"
```


