# Azure Static Website Hosting Assessment

## Lab Overview

In this assessment, you will host a static website directly from Azure Storage. You will enable the static website feature on a Storage Account, publish a web page, and make it accessible through the Storage Account's web endpoint.

## Scenario

You have joined an organization as a Cloud Engineer. The marketing team needs a low-cost, highly available way to publish a simple landing page without running any web servers. Your task is to host a static website using the Storage Account you provisioned in Scenario 5.

## Solution

To meet these requirements, you will enable the static website feature on the Storage Account, which exposes a special **$web** container, and publish the provided web page as the site's index document so it is reachable from the primary web endpoint.

# Assessment Objectives

You are expected to enable static website hosting and publish the provided web page so that it is served from the Storage Account.

> **Note:** Use the same Storage Account (the one beginning with **labstorage**) you created in Scenario 5.

> **Where to perform this task:** Complete this scenario in the **Azure portal** using **any web browser** (go to `https://portal.azure.com` and sign in with the Azure credentials on the Getting Started page). It is validated automatically in the environment.

---

## Task 1: Host a Static Website Using Azure Storage

1. Enable **static website hosting** on the Storage Account, using **index.html** as the index document.
2. Publish the web page below as the site's index document (file name **index.html**) to the **$web** container.
3. Confirm the page is reachable from the Storage Account's **primary web endpoint**.

**Web page to publish (save as index.html and upload):**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Azure Static Website</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Segoe UI', Arial, sans-serif;
           background: linear-gradient(135deg, #0078d4 0%, #003a6b 100%);
           color: #fff; min-height: 100vh; display: flex;
           align-items: center; justify-content: center; }
    .card { background: rgba(255,255,255,0.08);
            border: 1px solid rgba(255,255,255,0.2); border-radius: 16px;
            padding: 48px 56px; text-align: center; max-width: 560px; }
    h1 { font-size: 2.2rem; margin-bottom: 16px; }
    p { font-size: 1.05rem; line-height: 1.6; opacity: 0.9; }
    .badge { display: inline-block; margin-top: 24px; padding: 8px 18px;
             background: #fff; color: #0078d4; border-radius: 24px; font-weight: 600; }
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
