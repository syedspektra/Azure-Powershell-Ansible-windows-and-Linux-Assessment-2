# Linux System Service Configuration Assessment

## Lab Overview

In this assessment, you will create and manage a background service on a Linux system using **systemd**. You will define a service, configure it to start automatically on boot, start it, and ensure it is running.

## Scenario

You have joined an organization as a Cloud Engineer. The application team needs a custom background process to run continuously on a Linux server and to start automatically whenever the server reboots. Your task is to configure this process as a managed system service using systemd.

## Solution

To meet these requirements, you will define a systemd unit that runs a continuous background process, then enable and start the service.

## Assessment Objectives

You are expected to create and configure a systemd service named **labservice** that is enabled (starts on boot) and active (running).

> **Where to perform this task:** Complete this scenario in the **terminal on the lab VM** using an account with `sudo` privileges.

---

## Task 1: Configure a System Service

**1. Create the systemd unit file `/etc/systemd/system/labservice.service`:**

```bash
sudo tee /etc/systemd/system/labservice.service > /dev/null << 'EOF'
[Unit]
Description=Lab Service
After=network.target

[Service]
Type=simple
ExecStart=/bin/bash -c 'while true; do sleep 60; done'
Restart=always

[Install]
WantedBy=multi-user.target
EOF
```

**2. Reload systemd, then enable and start the service:**

```bash
sudo systemctl daemon-reload
sudo systemctl enable --now labservice
```

**3. Confirm the service is enabled and active:**

```bash
systemctl is-enabled labservice
systemctl is-active labservice
```

Both commands should return **enabled** and **active**, respectively.

### Success Criteria

- A systemd service named **labservice** exists.
- The service is **enabled** (starts on boot).
- The service is **active** (currently running).

<validation step="8a0a8a40-d147-4171-8c0f-1df19aa37723" />

---

## You have successfully completed the Assessment.
