# Exercise 04: Configure a systemd Service for the Backup Script

### Estimated Duration: 20 Minutes

## Scenario

Your team wants the existing backup process on the Linux jump VM to be manageable through systemd. You must configure a service that runs the backup script, ensure the unit is recognized by the operating system, and confirm that it can be enabled and started successfully.

## Overview

In this exercise, you will complete the systemd configuration for the backup workload by defining the required unit file, associating it with the correct script, reloading systemd, and validating the service state on the jump VM.

Before you begin, sign in to the Azure portal at <https://portal.azure.com> using **<inject key="AzureAdUserEmail"></inject>** and **<inject key="AzureAdUserPassword"></inject>** if you need to verify subscription context. Your lab deployment ID is **<inject key="DeploymentID" enableCopy="false"/>**.

## Objectives

- Task 1: Configure the backup service unit
- Task 2: Enable and verify the service

## Task 1: Configure the backup service unit

In this task, you will define the required systemd unit for the backup process.

- Create or complete the unit file at **`/etc/systemd/system/cloudlabs-backup.service`**.
- Ensure the unit is named **`cloudlabs-backup.service`**.
- Configure the service so that it runs the backup script located at **`/opt/cloudlabs/scripts/backup.sh`**.
- Confirm the unit definition is suitable for systemd to load without errors after a daemon reload.
- Use standard Linux tools to review the unit content and verify that the script target is correct.

> [!Important]
> The validation for this exercise expects the canonical service path, service name, and script path exactly as specified in the challenge requirements.

## Task 2: Enable and verify the service

In this task, you will make the service available to systemd and confirm that it operates successfully.

- Reload systemd so the new or updated unit file is recognized.
- Enable **`cloudlabs-backup.service`**.
- Start the service and verify that it reaches the expected successful state.
- Review service status details and any relevant logs to confirm the backup script can be invoked through systemd.
- If needed, correct the unit definition and retest until the service loads and runs successfully.

<validation step="951a19c4-e1ce-4dff-b5df-e2f981bbc880" />

## Summary

In this exercise, you configured the canonical systemd unit file for the backup workload, pointed it to **`/opt/cloudlabs/scripts/backup.sh`**, reloaded systemd, enabled the service, and verified that **`cloudlabs-backup.service`** can start successfully on the jump VM.
