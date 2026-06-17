# Linux Task Scheduling with PowerShell Assessment

## Lab Overview

In this assessment, you will automate a recurring task on a Linux system. You will create a PowerShell script and schedule it to run on a fixed interval using the Linux **cron** scheduler.

## Scenario

You have joined an organization as a Cloud Engineer. The operations team needs a routine task to run automatically at a regular interval on a Linux server without any manual intervention. Your task is to create a PowerShell script and schedule it to run periodically using cron.

## Solution

To meet these requirements, you will author a PowerShell (pwsh) script that records a timestamped entry to a log file, and configure a cron job that runs the script every minute.

# Assessment Objectives

You are expected to create the PowerShell script and schedule it with cron so the log file is updated automatically.

> **Where to perform this task:** Complete this scenario in the **terminal on the lab VM**.

---

## Task 1: Schedule an Automated Task Using Cron

**1. Create the PowerShell script `logtask.ps1` in your home directory:**

```bash
cat > $HOME/logtask.ps1 << 'EOF'
$timestamp = Get-Date -Format "yyyy-MM-dd HH:mm:ss"
"$timestamp - Scheduled task executed" | Out-File -FilePath "$HOME/cronjob.log" -Append
EOF
```

**2. Run it once (to create the log), then schedule it to run every minute with cron:**

```bash
pwsh $HOME/logtask.ps1
(crontab -l 2>/dev/null; echo "* * * * * /usr/bin/pwsh $HOME/logtask.ps1") | crontab -
```

> The command above stores the full path because `$HOME` expands when you run it. If you ever edit the crontab by hand (`crontab -e`), use `$HOME` or the full path such as `/home/Labuser/logtask.ps1` — do **not** use `$USER`, because cron does not set it and the job will not run.

**3. Confirm the cron entry exists and the log is being written automatically:**

```bash
crontab -l
sleep 70
cat $HOME/cronjob.log
```

You should see the cron entry listed, and multiple timestamped lines (one per minute) in `cronjob.log`.

### Success Criteria

- A cron job exists that runs the PowerShell script **logtask.ps1**.
- The script generates timestamped entries in **cronjob.log**.

<validation step="78d3c1ec-5798-49a9-80ae-6dc76c7fd4f0" />

---

## You have successfully completed the Assessment.
