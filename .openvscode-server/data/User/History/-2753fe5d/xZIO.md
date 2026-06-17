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
vsysuser@uptickpro-pod-334-iitmshakti:~$ cat > sample.log << 'EOF'
2026-06-15 09:00:01 INFO Application started
2026-06-15 09:01:12 WARNING Disk usage at 75%
2026-06-15 09:02:45 ERROR Failed to connect to database
2026-06-15 09:03:10 INFO Retrying connection
2026-06-15 09:03:30 Error Temporary network issue
2026-06-15 09:04:22 WARNING High memory usage detected
2026-06-15 09:05:01 ERROR User authentication failed
2026-06-15 09:06:17 INFO Background job completed
2026-06-15 09:07:40 warning Cache nearing capacity
2026-06-15 09:08:55 ERROR Unable to write to log file
2026-06-15 09:09:20 INFO Application shutdown initiated
> EOF
vsysuser@uptickpro-pod-334-iitmshakti:~$ find . -name "sample.log"
./sample.log
vsysuser@uptickpro-pod-334-iitmshakti:~$ grep "ERROR" sample.log
2026-06-15 09:02:45 ERROR Failed to connect to database
2026-06-15 09:05:01 ERROR User authentication failed
2026-06-15 09:08:55 ERROR Unable to write to log file
vsysuser@uptickpro-pod-334-iitmshakti:~$ grep "ERROR" sample.log > errors.txt
vsysuser@uptickpro-pod-334-iitmshakti:~$ grep -c "ERROR" sample.log
3
vsysuser@uptickpro-pod-334-iitmshakti:~$ grep -i "WARNING" sample.log
2026-06-15 09:01:12 WARNING Disk usage at 75%
2026-06-15 09:04:22 WARNING High memory usage detected
2026-06-15 09:07:40 warning Cache nearing capacity
```

### Number of ERROR lines found

<!-- Write the count from grep -c here -->
`<your answer>`

### Screenshot

![Task 2 — grep results](screenshots/task2.png)
