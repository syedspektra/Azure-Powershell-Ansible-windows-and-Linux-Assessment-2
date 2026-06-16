# Linux Task Scheduling with PowerShell Assessment

## Lab Overview

In this assessment, you will automate a recurring task on a Linux system. You will create a PowerShell script, schedule it to run on a fixed interval using the Linux **cron** scheduler, and ensure the scheduled job executes automatically.

## Scenario

You have joined an organization as a Cloud Engineer. The operations team needs a routine task to run automatically at a regular interval on a Linux server without any manual intervention. Your task is to create a PowerShell script and schedule it to run periodically using cron.

## Solution

To meet these requirements, you will author a PowerShell (pwsh) script that records a timestamped entry to a log file, and configure a cron job that runs the script every minute. Cron is the standard time-based job scheduler on Linux, and running PowerShell through cron lets you reuse cross-platform automation scripts on Linux hosts. Success is confirmed when the log file is updated automatically by the scheduled job.

# Assessment Objectives

This lab environment is designed to evaluate your practical skills in scheduling automated tasks on Linux. As part of this assessment, you will create a PowerShell script and configure a cron job that runs it on a schedule.

You are expected to follow Linux automation best practices and use the specified file names to ensure successful validation.

> **Note:** Perform all steps inside the **provided Linux VM**. PowerShell (`pwsh`) is available on the lab VM. Do not change the specified script or log file names, as the validation script depends on them.

---

## Task 1: Schedule an Automated Task Using Cron

> **Note:** Follow the specified naming conventions exactly to ensure validation works properly.

1. Create a PowerShell script named **logtask.ps1** in your home directory that writes a timestamped entry to a log file named **cronjob.log** (also in your home directory) each time it runs.
2. Schedule **logtask.ps1** to run automatically **every minute** using cron.
3. Ensure the cron job executes and that **cronjob.log** is updated automatically.

### Success Criteria

- A cron job exists that runs the PowerShell script **logtask.ps1**.
- The script generates timestamped entries in **cronjob.log**.

<validation step="78d3c1ec-5798-49a9-80ae-6dc76c7fd4f0" />

---

## You have successfully completed the Assessment.
