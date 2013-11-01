git init
git remote add origin https://github.com/hhru/frontik
git fetch
git checkout master
git filter-branch --subdirectory-filter frontik/testing/ HEAD
git remote add origin2 https://github.com/Baras/git_task2_repo_A.git
git push -u origin2 master

git init
git remote add origin https://github.com/hhru/frontik
git fetch
git checkout master
git filter-branch --tree-filter 'rm -rf frontik/testing' HEAD
git remote add origin2 https://github.com/Baras/git_task2_repo_B.git
git push -u origin2 master