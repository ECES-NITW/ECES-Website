# SOP to follow for making changes

## 1. One-Time Setup

### 1.1 Fork & Clone
1. Fork the main repository to your GitHub account.
2. Clone your fork:
```
git clone git@github.com:<your-username>/ECES-Website.git
cd ECES-Website
```
### 1.2 Add Upstream 
```
git remote add upstream git@github.com:ECES-NITW/ECES-Website.git
git remote -v
```

## 2. Keeping Your Fork Updated

Before starting any work:
```
git checkout main
git pull upstream main
git push origin main
```

## 3. Working on a Change
### 3.1 Create a New Branch

Create a new branch for every change:

```git checkout -b feature/<short-description>```


Examples:
```
feature/event-card
feature/events-page
data/add-event-jan-2026
docs/update-sop
```

### 3.2 Implement Changes

- Make only one logical change per branch
- Follow repo structure and SOPs
- Do not modify unrelated files


## 4. Local Testing (Mandatory)

### Before pushing:
```
npm install
npm run dev
npm run build
```

### Proceed only if:

- App runs locally
- Build succeeds
- No console errors

## 5. Commit & Push
```
git status
git add .
git commit -m "Clear, descriptive message"
git push origin feature/<short-description>
```
## 6. Open Pull Request (PR)

Open PR from your branch → main of the original repo


## 7. Merge + Steps after
```
git checkout main
git pull upstream main
git push origin main
```
Delete your feature branch.

## 8. Hard Rules

- Never push directly to ```main```
- Never mix multiple features in one PR
- Never skip local build before PR
