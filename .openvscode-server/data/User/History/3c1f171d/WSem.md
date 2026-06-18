<p align="center">
  <img src="../../vyoma.png" alt="Vyoma Systems" width="200"/>
</p>

# Module 02 — Git & Version Control · Submission

> Fill in the sections below. For each task, paste the exact commands you ran and add a
> screenshot to the `screenshots/` folder, then reference it as shown. Replace the placeholder
> text and image names with your own.

---

## Task 1 — Publish your first repository

### Commands I used

```bash
sysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git push -u origin main
branch 'main' set up to track 'origin/main'.
Everything up-to-date
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git add .
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git commit -m "Assignment 2 task 1"
[main 9e40209] Assignment 2 task 1
 2 files changed, 5 insertions(+), 1 deletion(-)
 create mode 100644 .gitignore
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git push -u origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 379 bytes | 379.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/AmsyarRiz/learn_git.git
   59b7ba3..9e40209  main -> main
branch 'main' set up to track 'origin/main'.
```

### Link to my GitHub repository

<!-- Paste the URL of your repository on GitHub -->
`<https://github.com/AmsyarRiz/learn_git.git>`

### Screenshot

<!-- Save your screenshot in the screenshots/ folder, e.g. screenshots/task1.png -->
![Task 1 — repository on GitHub](screenshots/task1.png)

---

## Task 2 — Branch, modify, and merge

### Commands I used

```bash
# Paste the commands you ran here
vsysuser@uptickpro-pod-334-iitmshakti:~$ cd learn_git
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git branch
  feature
* main
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git checkout feature
Switched to branch 'feature'
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ echo "Additional line" >> notes.txt
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git add .
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git commit -m "task 2"
[feature 340b8c2] task 2
 1 file changed, 1 insertion(+)
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git push
fatal: The current branch feature has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin feature

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git push --set-upstream origin feature
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 316 bytes | 316.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'feature' on GitHub by visiting:
remote:      https://github.com/AmsyarRiz/learn_git/pull/new/feature
remote:
To https://github.com/AmsyarRiz/learn_git.git
 * [new branch]      feature -> feature
branch 'feature' set up to track 'origin/feature'.
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git push
Everything up-to-date
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git merge feature
Auto-merging notes.txt
CONFLICT (content): Merge conflict in notes.txt
Automatic merge failed; fix conflicts and then commit the result.
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git add .
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git commit -m "resolved"
[main 272c965] resolved
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 305 bytes | 305.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/AmsyarRiz/learn_git.git
   6b94e6d..272c965  main -> main
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git merge feature
Already up to date.
vsysuser@uptickpro-pod-334-iitmshakti:~/learn_git$ git log --oneline --graph --all
*   272c965 (HEAD -> main, origin/main) resolved
|\
| * 340b8c2 (origin/feature, feature) task 2
* | 6b94e6d delete line
* | a931f13 update notes
* | 9e40209 Assignment 2 task 1
|/
* 59b7ba3 update notes
* 7c10595 Initial commit
* 4778ace Initial commit
```

### Screenshot

![Task 2 — git log graph](screenshots/task2.png)

---

## Optional stretch goal — fork & pull request

<!-- If you completed the stretch goal, paste your pull request link here. Otherwise, delete this section. -->
`<your pull request URL>`
