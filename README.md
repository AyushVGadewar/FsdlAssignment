# FsdlAssignment

**Full Stack Development Lab Assignment**

## Aim
To learn and demonstrate version control using Git and a remote repository (GitHub).  
This assignment shows repository initialization, commits, branching, pushing, pulling, and merging.

## Objectives
1. Introduce the concepts and software behind version control (Git).  
2. Learn how to use clone, commit, push, pull, branch, and merge.  
3. Demonstrate collaborative workflow with a remote repository on GitHub.

## Files in this repository
- `README.md` — this file  
- `feature.txt` — file added in `feature1` branch and merged to `main`

## Commands I ran (step-by-step)
```bash
# created/entered repo (local)
mkdir FsdlAssignment
cd FsdlAssignment
git init

# created README and initial commit
echo "Full Stack Development Lab Assignment" > README.md
git add .
git commit -m "Initial commit for FSDL Assignment"

# set remote and push main
git remote add origin https://github.com/AyushVGadewar/FsdlAssignment.git
git branch -M main
git push -u origin main

# create feature branch, commit, push
git checkout -b feature1
echo "This file is created in feature branch" > feature.txt
git add feature.txt
git commit -m "Added feature file in feature1 branch"
git push origin feature1

# merge branch into main and push
git checkout main
git merge feature1
git push origin main

# verify history
git log --oneline
