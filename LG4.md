# Linux System Service Configuration Assessment

## Lab Overview

In this assessment, you will create and manage a background service on a Linux system using **systemd**. You will define a service, configure it to start automatically on boot, start it, and ensure it is running.

## Scenario

You have joined an organization as a Cloud Engineer. The application team needs a custom background process to run continuously on a Linux server and to start automatically whenever the server reboots. Your task is to configure this process as a managed system service using systemd.

## Solution

To meet these requirements, you will define a systemd service that runs a continuous background process, then enable and start it. systemd is the standard init and service manager on modern Linux distributions, providing automatic startup, restart-on-failure, and centralized service control. Success is confirmed when the service is both enabled and active.

# Assessment Objectives

This lab environment is designed to evaluate your practical skills in managing system services on Linux. As part of this assessment, you will create and configure a systemd service that runs as a managed, auto-starting service.

You are expected to follow Linux service management best practices and use the specified service name to ensure successful validation.

> **Note:** Perform all steps inside the **provided Linux VM** using an account with `sudo` privileges. Do not change the specified service name, as the validation script depends on it.

---

## Task 1: Configure a System Service

> **Note:** Follow the specified naming conventions exactly to ensure validation works properly.

1. Create a systemd service named **labservice** that runs a continuous background process on the Linux VM.
2. Configure the service to start automatically **on boot**.
3. Start the service so that it is currently running.

### Success Criteria

- A systemd service named **labservice** exists.
- The service is **enabled** (starts on boot).
- The service is **active** (currently running).

<validation step="8a0a8a40-d147-4171-8c0f-1df19aa37723" />

---

## You have successfully completed the Assessment.

