# Azure Storage Account Automation Assessment

## Lab Overview

In this assessment, you will use Infrastructure as Code (IaC) to provision Azure storage resources. You will author and deploy an automation script that creates an Azure Storage Account in a repeatable, consistent way, following Azure deployment and naming best practices.

## Scenario

You have joined an organization as a Cloud Engineer. The company is moving away from manual portal-based provisioning and wants all storage resources created through automation so deployments are consistent and repeatable. Your task is to deploy a Storage Account using an automation script rather than the portal UI.

## Solution

To meet these requirements, you will author an Azure Resource Manager (ARM) template that defines a general-purpose v2 Storage Account and deploy it to a resource group using an automation command. Using an ARM template ensures the storage resource is provisioned the same way every time, supports version control, and removes manual configuration errors.

# Assessment Objectives

This lab environment is designed to evaluate your practical skills in automating Azure resource deployments using Infrastructure as Code. As part of this assessment, you will author and deploy an automation script that provisions a Storage Account meeting the required configuration.

You are expected to follow Azure deployment best practices and use the specified resource configuration to ensure successful validation.

> **Note:** To ensure successful validation and consistency across all assessment tasks, you must deploy all Azure resources in **one of the following supported Azure Regions only**:
>
> - East US
> - East US 2
> - West US 2
>
> Resources deployed in any other Azure Region may not be detected by the validation scripts and could result in assessment failures.

---

## Task 1: Deploy a Storage Account Using an Automation Script

> **Note:** Follow the specified naming and configuration conventions exactly to ensure validation works properly.

1. Deploy an Azure Storage Account using an **automation script (ARM template)**. The account must **not** be created manually through the portal UI.
2. The Storage Account name must begin with **labstorage**.
3. Configure the account as kind **StorageV2** with the **Standard_LRS** replication SKU.
4. Deploy the account into a resource group located in one of the supported regions.

### Success Criteria

- A Storage Account whose name begins with **labstorage** exists.
- The Storage Account kind is **StorageV2**.
- The Storage Account SKU is **Standard_LRS**.

<validation step="a160b434-3a61-41bf-9aff-48d257f5cee4" />

---

## You have successfully completed the Assessment.

