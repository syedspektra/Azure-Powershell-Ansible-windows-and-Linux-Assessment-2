# Exercise 02: Host a Static Website Using Azure Storage

### Estimated Duration: 20 Minutes

## Scenario

You are working as a cloud automation engineer in the shared lab environment. A baseline Azure Storage Account has already been deployed for your team. Your task is to use the Azure portal from the Linux jump VM to configure static website hosting and publish the required site content so the site can be validated successfully.

## Overview

In this exercise, you will sign in to Azure by using Microsoft Edge on the jump VM, locate the predeployed Storage Account in the **rg-<inject key="DeploymentID" enableCopy="false"></inject>** resource group, enable the static website feature, upload the required website files from the jump VM, and confirm that the site returns the expected content.

## Objectives

- Task 1: Sign in to Azure and identify the target Storage Account
- Task 2: Configure static website hosting and publish the required files
- Task 3: Verify the website endpoint and expected content

## Task 1: Sign in to Azure and identify the target Storage Account

In this task, you will access the Azure portal from the jump VM and confirm the Storage Account that will be used for the static website challenge.

- Use **Microsoft Edge** on the Linux jump VM to open <https://portal.azure.com>.
- Sign in with:
  - Username: `<inject key="AzureAdUserEmail"></inject>`
  - Password: `<inject key="AzureAdUserPassword"></inject>`
- Confirm that you are working in subscription `<inject key="SubscriptionID"></inject>`.
- Locate the predeployed Storage Account in the **rg-<inject key="DeploymentID" enableCopy="false"></inject>** resource group.
- Confirm that your work for this exercise will be completed in the Azure portal from the jump VM context.

> [!Important]
> This is an assessment-style exercise. You are expected to determine the exact portal actions required without step-by-step guidance.

## Task 2: Configure static website hosting and publish the required files

In this task, you will configure the Storage Account for static website hosting and publish the required website assets.

- Enable the **Static website** feature on the provided Storage Account.
- Use the website source folder on the jump VM at `/opt/cloudlabs/www` as your content source.
- Ensure that the `$web` container contains both of the required files:
  - `index.html`
  - `404.html`
- Make sure the published site content is aligned with the expected validation outcome.

> [!Important]
> Both `index.html` and `404.html` must be present in the `$web` container for this exercise to be considered complete.

> [!Tip]
> Review the uploaded content carefully before moving on. Missing files or uploading to the wrong location will cause validation failure.

## Task 3: Verify the website endpoint and expected content

In this task, you will confirm that the static website endpoint is reachable and that the correct page content is returned.

- Retrieve the static website endpoint from the Storage Account configuration.
- Open the endpoint in the browser on the jump VM.
- Verify that the site is reachable.
- Verify that the returned page contains the text **CloudLabs Azure Challenge Lab**.
- If necessary, review the uploaded files in `$web` and correct any issues before final validation.

<validation step="Static Website"/>

## Summary

In this exercise, you used Microsoft Edge on the jump VM to sign in to Azure, configured static website hosting on the provided Storage Account in **rg-<inject key="DeploymentID" enableCopy="false"></inject>**, uploaded `index.html` and `404.html` to the `$web` container, and confirmed that the static website endpoint returns the expected content: **CloudLabs Azure Challenge Lab**.
