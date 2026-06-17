<p align="center">
  <img src="../../vyoma.png" alt="Vyoma Systems" width="200"/>
</p>

# Module 01 — Linux Essentials · Submission

> Fill in the sections below. For each task, paste the exact commands you ran and add a
> screenshot to the `screenshots/` folder, then reference it as shown. Replace the placeholder
> text and image names with your own.

---

## Task 1 — Build a project workspace

### Commands I used

```bash
# Paste the commands you ran here
vsysuser@uptickpro-pod-334-iitmshakti:~$ mkdir linux_lab
vsysuser@uptickpro-pod-334-iitmshakti:~$ cd linux_
bash: cd: linux_: No such file or directory
vsysuser@uptickpro-pod-334-iitmshakti:~$ cd ./linux_lab/
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab$ mkdir notes
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab$ mkdir scripts
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab$ cd notes
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab/notes$ echo "Day 1: learned mkdir and cd" > day1.txt
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab/notes$ echo "Day 1: also learned ls" >> day1.txt
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab/notes$ cat > day2.txt
Day2: learned cp
Day2: learned rm
Day2: learned find
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab/notes$ cp day1.txt ../scripts/
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab/notes$ ..
bash: ..: command not found
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab/notes$ cd ..
vsysuser@uptickpro-pod-334-iitmshakti:~/linux_lab$ ls -R
```

### Screenshot

<!-- Save your screenshot in the screenshots/ folder, e.g. screenshots/task1.png -->
![Task 1 — ls -R output](screenshots/task1.png)

---

## Task 2 — Log hunting

### Commands I used

```bash
# Paste the commands you ran here
```

### Number of ERROR lines found

<!-- Write the count from grep -c here -->
`<your answer>`

### Screenshot

![Task 2 — grep results](screenshots/task2.png)
