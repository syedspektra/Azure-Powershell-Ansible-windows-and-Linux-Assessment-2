# Exercise 01: Write automation to deploy infrastructure using ARM templates

### Estimated Duration: 0.5 Hour(s)

## Scenario

You are working as a cloud automation engineer and need to create a reusable ARM-based deployment for a low-cost Azure resource. Your task is to author the required automation from the jump VM and deploy it into your learner resource group in Azure. The deployment must align to the lab naming and cost requirements and should be suitable for repeatable use in the shared subscription context.

## Overview

In this exercise, you will use the jump VM to create or complete an ARM template at `/opt/cloudlabs/arm/deploy-storage.json` and optionally use a PowerShell deployment script at `/opt/cloudlabs/arm/deploy-storage.ps1`. You will deploy a low-cost Azure Storage Account into the learner resource group that follows the `rg-$DID` naming context, where your deployment identifier is **<inject key="DeploymentID" enableCopy="false"></inject>**. You may verify deployment results in Azure after signing in with **<inject key="AzureAdUserEmail"></inject>** and **<inject key="AzureAdUserPassword"></inject>**.

## Objectives

- Task 1: Review deployment requirements and author the ARM template
- Task 2: Deploy the template into the learner resource group
- Task 3: Confirm the deployed resource matches the required cost and naming expectations

## Task 1: Author the ARM deployment artifacts

In this task, you will create or complete the automation artifacts needed for the deployment.

Your solution must satisfy all of the following requirements:

1. The primary ARM template file must exist at `/opt/cloudlabs/arm/deploy-storage.json`.
2. If you choose to use a deployment helper script, it must exist at `/opt/cloudlabs/arm/deploy-storage.ps1`.
3. The deployment target must be a low-cost Azure Storage Account.
4. The storage account must use the **StorageV2** kind.
5. The storage account must use the **Standard_LRS** SKU.
6. The deployment must be intended for your learner resource group using the `rg-$DID` naming convention.
7. The deployed storage account name must follow the expected pattern `clstorage<uniqueSuffix>`.

> [!Important]
> This is an assessment-style challenge. You are expected to determine the required ARM structure, properties, and deployment logic without a procedural walkthrough.

> [!Tip]
> Use the jump VM as your working environment and keep your artifacts in the canonical ARM workspace under `/opt/cloudlabs/arm`.

## Task 2: Run the deployment

In this task, you will deploy your ARM template into the learner resource group associated with your deployment identifier **<inject key="DeploymentID" enableCopy="false"></inject>**.

To complete this task successfully:

1. Use the resource group naming context `rg-$DID`.
2. Execute a successful ARM deployment from the automation artifacts you prepared.
3. If you use a script, ensure `/opt/cloudlabs/arm/deploy-storage.ps1` correctly deploys `/opt/cloudlabs/arm/deploy-storage.json`.
4. Ensure the deployment completes successfully in Azure.

> [!Note]
> You can use available tools on the jump VM and, if needed, verify results by signing in to the Azure portal with **<inject key="AzureAdUserEmail"></inject>** and **<inject key="AzureAdUserPassword"></inject>**.

## Task 3: Validate the deployed storage account

In this task, you will confirm that the deployed Azure resource meets the exercise requirements.

Success for this exercise means all of the following are true:

1. A deployable ARM template exists at `/opt/cloudlabs/arm/deploy-storage.json`.
2. The deployment completes successfully in the learner resource group `rg-$DID`.
3. The expected Azure Storage Account exists.
4. The storage account name uses the required or expected naming pattern `clstorage<uniqueSuffix>`.
5. The storage account is configured with **StorageV2** and **Standard_LRS**.
6. The deployed resource remains aligned to the lab's low-cost design goal.

<validation step="951a19c4-e1ce-4dff-b5df-e2f981bbc880" />

## Summary

In this exercise, you authored ARM-based automation on the jump VM and used it to deploy a low-cost Azure Storage Account into your learner resource group. Your completed solution should include the canonical template path, optional deployment script path, the correct `rg-$DID` deployment context, and a successful StorageV2 Standard_LRS deployment that follows the expected naming pattern.
