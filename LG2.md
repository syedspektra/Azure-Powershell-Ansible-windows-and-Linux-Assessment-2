# Azure Static Website Hosting Assessment

## Lab Overview

In this assessment, you will host a static website directly from Azure Storage. You will enable static website hosting on a Storage Account, publish a web page, and make it accessible through the Storage Account's web endpoint.

## Scenario

You have joined an organization as a Cloud Engineer. The marketing team needs a low-cost, highly available way to publish a simple landing page without running any web servers. Your task is to host a static website using the Storage Account you provisioned in Scenario 5.

## Solution

To meet these requirements, you will enable the static website feature on the Storage Account, which exposes a special **$web** container, and publish the provided web page as the site's index document. The page must then be reachable from the Storage Account's primary web endpoint. This approach delivers a fast, serverless, and inexpensive website.

# Assessment Objectives

This lab environment is designed to evaluate your practical skills in hosting static web content on Azure Storage. As part of this assessment, you will enable static website hosting and publish the provided web page so that it is served from the Storage Account.

You are expected to follow Azure best practices and use the specified configuration to ensure successful validation.

> **Note:** To ensure successful validation and consistency across all assessment tasks, you must deploy all Azure resources in **one of the following supported Azure Regions only**:
>
> - East US
> - East US 2
> - West US 2
>
> Resources deployed in any other Azure Region may not be detected by the validation scripts and could result in assessment failures.

---

## Task 1: Host a Static Website Using Azure Storage

> **Note:** Use the Storage Account (the one beginning with **labstorage**) that you created in Scenario 5.

1. Enable **static website hosting** on the Storage Account, using **index.html** as the index document.
2. Publish the web page provided below as the site's index document (file name **index.html**).
3. Ensure the published page is accessible from the Storage Account's **primary web endpoint**.

**Web page to publish (index.html):**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Azure Static Website</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      background: linear-gradient(135deg, #0078d4 0%, #003a6b 100%);
      color: #ffffff;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .card {
      background: rgba(255, 255, 255, 0.08);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 16px;
      padding: 48px 56px;
      text-align: center;
      max-width: 560px;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.25);
    }
    h1 { font-size: 2.2rem; margin-bottom: 16px; }
    p { font-size: 1.05rem; line-height: 1.6; opacity: 0.9; }
    .badge {
      display: inline-block;
      margin-top: 24px;
      padding: 8px 18px;
      background: #ffffff;
      color: #0078d4;
      border-radius: 24px;
      font-weight: 600;
      font-size: 0.95rem;
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Welcome to my Azure Static Website</h1>
    <p>This page is served directly from an Azure Storage Account using the static website feature — no web server required.</p>
    <span class="badge">Hosted on Azure Storage</span>
  </div>
</body>
</html>
```

### Success Criteria

- Static website hosting is **enabled** on the Storage Account.
- An **index.html** file is published to the **$web** container.
- The Storage Account's primary web endpoint returns the published page.

<validation step="b687500b-32a1-485c-8ab3-2168d70bb1c9" />

---

## You have successfully completed the Assessment.

