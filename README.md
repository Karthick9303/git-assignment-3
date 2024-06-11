# Create and navigate to directory
mkdir git_project
cd git_project

# Initialize Git repository
git init

# Create branches
git checkout -b develop
git checkout -b f1
git checkout -b f2

# Commit main.txt to master
git checkout master
echo "This is the main file" > main.txt
git add main.txt
git commit -m "Add main.txt to master branch"

# Add develop.txt to develop branch
git checkout develop
echo "This is the develop file" > develop.txt
git add develop.txt
git commit -m "Add develop.txt to develop branch"

# Add f1.txt to f1 branch
git checkout f1
echo "This is the f1 file" > f1.txt
git add f1.txt
git commit -m "Add f1.txt to f1 branch"

# Add f2.txt to f2 branch
git checkout f2
echo "This is the f2 file" > f2.txt
git add f2.txt
git commit -m "Add f2.txt to f2 branch"

# Push branches to GitHub
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin master
git push -u origin develop
git push -u origin f1
git push -u origin f2

# Delete f2 branch locally and on GitHub
git branch -d f2
git push origin --delete f2
