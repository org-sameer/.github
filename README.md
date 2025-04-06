# PR Quality Enforcer 🔍  
Automatically checks if PRs include **screenshots** and follow your template.  

## 🚀 Quick Setup  
1. **Add the workflow** to your org/repo:  
   - Copy [`.github/workflows/check-pr-info.yml`](.github/workflows/pr-screenshot-check.yml) to your repo.  
2. **Set up a branch protection rule**:  
   - Go to **Repo Settings → Branches → Add Rule**.  
   - Require the `pr-screenshot-check` status check to pass before merging.  
3. **Optional**: Customize the PR template in `PULL_REQUEST_TEMPLATE.md`.  

## ✨ Features  
- Blocks PRs without screenshots (or warns via comment).  
- Enforces PR descriptions via templates.  
- Works with any GitHub repo.  

## 🎥 Demo  
![GIF showing the check failing/passing](https://your-link-here.gif)  

## 🤖 How It Works  
The GitHub Action:  
1. Triggers on `pull_request`.  
2. Scans the PR body for `![image]()` or `<img>` tags.  
3. Passes/fails the check based on your rules.  

## 📌 Example PR Template  
```markdown  
### Changes  
- [ ] Screenshot attached  
- [ ] Description of changes  

<!-- Drag & drop screenshots below -->  
