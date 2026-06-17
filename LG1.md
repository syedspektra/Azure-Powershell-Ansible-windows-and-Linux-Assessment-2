# Azure Storage Account Automation Assessment

## Lab Overview

In this assessment, you will use Infrastructure as Code (IaC) to provision Azure storage resources. You will deploy an Azure Storage Account using an Azure Resource Manager (ARM) template, in a repeatable and consistent way.

## Scenario

You have joined an organization as a Cloud Engineer. The company is moving away from manual portal-based provisioning and wants all storage resources created through automation so deployments are consistent and repeatable. Your task is to deploy a Storage Account using an ARM template rather than manually creating it.

## Solution

To meet these requirements, you will deploy an ARM template that defines a general-purpose v2 Storage Account. Using a template ensures the storage resource is provisioned the same way every time and removes manual configuration errors.

# Assessment Objectives

You are expected to deploy a Storage Account that matches the required configuration using the automation template provided below.

> **Note:** Deploy all Azure resources in **one of the following supported Azure Regions only**: **East US**, **East US 2**, or **West US 2**.

> **Where to perform this task:** Complete this scenario in the **Azure portal** using **any web browser** (go to `https://portal.azure.com` and sign in with the Azure credentials on the Getting Started page). It is validated automatically in the environment.

---

## Task 1: Deploy a Storage Account Using an ARM Template

In the Azure portal, search for **Deploy a custom template** → **Build your own template in the editor** → paste the template below → **Save** → select the resource group provided in your environment and a supported region → **Review + create** → **Create**.

**ARM template — copy and paste into the editor:**

```json
{
  "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
  "contentVersion": "1.0.0.0",
  "parameters": {
    "storageAccountName": {
      "type": "string",
      "defaultValue": "[concat('labstorage', uniqueString(resourceGroup().id))]"
    },
    "location": {
      "type": "string",
      "defaultValue": "[resourceGroup().location]"
    }
  },
  "resources": [
    {
      "type": "Microsoft.Storage/storageAccounts",
      "apiVersion": "2023-01-01",
      "name": "[parameters('storageAccountName')]",
      "location": "[parameters('location')]",
      "sku": { "name": "Standard_LRS" },
      "kind": "StorageV2",
      "properties": {
        "minimumTlsVersion": "TLS1_2",
        "allowBlobPublicAccess": true,
        "supportsHttpsTrafficOnly": true
      }
    }
  ],
  "outputs": {
    "storageAccountName": {
      "type": "string",
      "value": "[parameters('storageAccountName')]"
    }
  }
}
```

> The template auto-generates a globally unique name that begins with `labstorage`. Note this name — you will use the same Storage Account in Scenario 6.

### Success Criteria

- A Storage Account whose name begins with **labstorage** exists.
- The Storage Account kind is **StorageV2**.
- The Storage Account SKU is **Standard_LRS**.

<validation step="6939e7d4-6b18-4c10-943a-89453bf0d57f" />

---

## You have successfully completed the Assessment.
