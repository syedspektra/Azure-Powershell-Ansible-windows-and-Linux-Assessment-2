# Getting Started

## Scenario

You are a cloud automation engineer working in a shared Azure lab environment. In this 90-minute assessment lab, you will complete four challenge exercises focused on Azure resource deployment, static website hosting, Linux automation, and service configuration. The exercises are designed to assess your ability to work independently in Azure and Linux without detailed procedural guidance.

## Lab Overview

This challenge lab includes four mostly independent exercises:

- Deploy an Azure resource by using an ARM template.
- Configure static website hosting in Azure Storage.
- Create and schedule a Linux task with cron.
- Configure a persistent systemd service.

### Azure tasks — Scenario 5 and Scenario 6

Scenarios 5 and 6 are performed in the **Azure portal** and are validated automatically in the environment. You can complete them in **any web browser on your own machine** — there is no need to use the lab VM for these.

1. Open a web browser and go to **https://portal.azure.com**.
2. Sign in with the Azure credentials below:

      * Username:<inject key="azureaduseremail" cloudname="Microsoft Azure" enableCopy="false" enableClickToPaste="false" />
      * Password:<inject key="azureaduserpassword" cloudname="Microsoft Azure" enableCopy="false" enableClickToPaste="false" />

   > Tip: open a private / incognito window first so the lab account doesn't conflict with any personal Azure session.

3. After signing in, make sure you are working in a supported region: **East US**, **East US 2**, or **West US 2**.

### Linux tasks — Scenario 7 and Scenario 8

Scenarios 7 and 8 are performed **directly on the lab VM** using the terminal.

Your deployment identifier for this lab is **<inject key="DeploymentID" enableCopy="true" />**.

## Expectations

This is an assessment-style lab, not a tutorial. You are expected to determine the approach yourself and meet the success criteria defined in each scenario. Each scenario is validated independently.
