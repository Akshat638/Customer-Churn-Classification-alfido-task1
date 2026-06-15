# 🚀 GitHub Upload Guide — Step by Step
## (For Complete Beginners — No Experience Needed)

---

## PART A — One-Time Setup (Do this only once)

### Step 1: Create a GitHub Account
1. Go to 👉 https://github.com
2. Click "Sign up"
3. Enter your email, password, username
4. Verify your email
5. ✅ Account created!

---

### Step 2: Install Git on Your Computer

**Windows:**
1. Go to 👉 https://git-scm.com/download/win
2. Download and install (click Next → Next → Finish, all defaults are fine)
3. After install, search "Git Bash" in your Start menu and open it

**Mac:**
1. Open Terminal (search "Terminal" in Spotlight)
2. Type: `git --version`
3. If not installed, it will ask you to install — click Install

---

### Step 3: Tell Git Your Name & Email (one time only)
Open Git Bash (Windows) or Terminal (Mac) and type:
```
git config --global user.name "Your Full Name"
git config --global user.email "your@email.com"
```
(Use the same email as your GitHub account)

---

## PART B — Upload Your Project

### Step 4: Create a New Repository on GitHub
1. Go to https://github.com and log in
2. Click the **"+"** icon (top right) → "New repository"
3. Repository name: `alfido-ml-task1`
4. Description: `ML Classification Project - Telco Churn Prediction`
5. Set to **Public**
6. ❌ Do NOT check "Add README" (we already have one)
7. Click **"Create repository"**
8. You'll see a page with a URL like: `https://github.com/YOURNAME/alfido-ml-task1.git`
9. **Copy that URL** — you'll need it in Step 6

---

### Step 5: Open Terminal / Git Bash and Navigate to Your Project Folder

**Windows:**
1. Open Git Bash
2. Type this (replace with your actual folder path):
```
cd /c/Users/YourName/Downloads/alfido_task1
```

**Mac:**
```
cd ~/Downloads/alfido_task1
```

Check you're in the right place:
```
ls
```
You should see: `churn_classification.ipynb`, `churn_data.csv`, `README.md`, etc.

---

### Step 6: Upload to GitHub
Copy and paste these commands ONE BY ONE (press Enter after each):

```
git init
```
(Initializes git in your folder)

```
git add .
```
(Stages ALL files for upload)

```
git commit -m "Task 1: ML Classification - Telco Churn Prediction"
```
(Creates a save point with a message)

```
git branch -M main
```
(Names the branch "main")

```
git remote add origin https://github.com/YOURNAME/alfido-ml-task1.git
```
⚠️ REPLACE the URL with YOUR repository URL from Step 4!

```
git push -u origin main
```
(Uploads everything to GitHub)

It will ask for your GitHub username and password.
> ⚠️ For password, use a **Personal Access Token** (not your real password):
> 1. GitHub → Settings → Developer Settings → Personal Access Tokens → Tokens (classic)
> 2. Generate new token → check "repo" → copy the token
> 3. Paste that token as your password

---

### Step 7: Verify Upload
1. Go to `https://github.com/YOURNAME/alfido-ml-task1`
2. You should see ALL your files listed
3. The README.md will display automatically below the files
4. ✅ Upload complete!

---

## PART C — Submit to Alfido Tech

### Step 8: Submit Your Task
1. Go to the **Task Submission** page on Alfido Tech website
2. In the submission form, paste:
   - **Task Number:** Task 1
   - **GitHub Link:** `https://github.com/YOURNAME/alfido-ml-task1`
3. Submit!

---

## 📋 What Your Manager Will Review

Your internship manager will check:

| What They Check | Where They Look |
|---|---|
| Code quality & comments | `churn_classification.ipynb` |
| All 5 metrics are present | Notebook output cells |
| 2 algorithms compared | Notebook Step 6 & 7 |
| Cross-validation done | Notebook Step 8 |
| Plots generated | PNG files + notebook |
| README with setup instructions | `README.md` |
| requirements.txt exists | `requirements.txt` |
| Code runs without errors | They will run `jupyter notebook` |

---

## ❓ Common Errors & Fixes

**"git is not recognized"**
→ Restart your computer after installing Git

**"Permission denied"**
→ Use Personal Access Token as password (see Step 6)

**"fatal: remote origin already exists"**
→ Type: `git remote remove origin` then redo the remote add step

**Notebook won't run**
→ Make sure you installed packages: `pip install -r requirements.txt`
