# rebase_practice

Task5: Rebase Scenario
•	Create a repo rebase_practice.
•	Create branches main and feature/db.
•	Add a few commits in both branches.
•	Rebase feature/db on top of main.
•	Resolve any conflicts and complete the rebase.
•	Push both branches and share git log --graph --oneline --all.

stepts to be followed
Step 1: Create repo or clone the repo from remote git clone

step 2: Create initial commit on main
--> echo "Project initialized" > file1.txt
--> git add file1.txt
--> git commit -m "commit1"
--> echo "first line added" >> file1.txt
--> git add file1.txt
--> git commit -m "commit2" echo "second line added" >> file1.txt
--> git add file1.txt
--> git commit -m "commit3"
Step 3: Create feature branch
--> git checkout -b feature/db
Step 4: Add commits in feature/db
--> echo "DB connection setup" > db.txt
--> git add db.txt
--> git commit -m "commit4-DB connection added"
--> echo "Added DB schema" >> db.txt
--> git add db.txt
--> git commit -m "commit5-Updated DB schema"
Step 5: Add new commits on main branch
--> git checkout main
--> echo "rebase to be done to main from feature/db" > fil2.txt
--> git add file2.txt
--> git commit -m "commit 6"
--> echo "rebasing operation in process" >> file2.txt
--> git add file2.txt
--> git commit -m "commit 7"
Step 6: Rebase feature/db on top of main
--> git checkout feature/db
--> git rebase main
--> If there are no conflicts, continue further if conflicts arise then we have to resolve:
--> edit the file that has conflict and fix conflict git add . git rebase --continue
Step 7: Push both branches
--> git push -u origin main
--> git push -u origin feature/db
Step 8: Verify final commit graph
--> git log --graph --oneline --all
