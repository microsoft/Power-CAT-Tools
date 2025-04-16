# Power CAT Tools - Installation Guide

Install the **Power CAT Tools** solution from Microsoft AppSource into your Power Platform environment by following the steps below.

---

## Prerequisites

- Admin or Environment Maker permissions in the target environment
- Access to [make.powerapps.com](https://make.powerapps.com)

---

## Option 1: Install from Microsoft AppSource

### 1. Open Power Apps Portal

- Go to [https://make.powerapps.com](https://make.powerapps.com)
  
![image](https://github.com/user-attachments/assets/4733fcd4-2dde-468a-9fff-b6985e0e0314)

---

### 2. Open Advanced Settings

- Click the gear icon (**⚙️**) in the top-right corner
- Select **Advanced settings**
  
![image](https://github.com/user-attachments/assets/28c6808e-7271-4368-bc78-b1243e6d7312)

---

### 3. Access Microsoft AppSource

- A new tab will open with the classic Dynamics 365 settings
- Navigate to:  
  `Settings > Customizations > Microsoft AppSource`

![image](https://github.com/user-attachments/assets/295f2174-2590-4cd9-aeff-166d316962e6)

---

### 4. Search for Power CAT Tools

- In the AppSource window, use the search bar to find **Power CAT Tools**
- Click on the app in the search results

![image](https://github.com/user-attachments/assets/4d44f451-cc03-4a36-a892-058e7bb18162)

---

### 5. Start Installation

- On the app page, click **Get it now**
- You’ll be redirected to the Power Platform Admin Center

![image](https://github.com/user-attachments/assets/d486dd51-b8ff-4925-a9bf-1fb072b849b7)

---

### 6. Choose Environment & Accept Terms

- Select the environment where the solution should be installed
- Accept the license agreement and privacy terms

---

### 7. Install the Solution

- Click **Install**
- The installation may take a few minutes to complete

![image](https://github.com/user-attachments/assets/a6a8e50b-2ce7-433d-abdb-da534bc5e1df)

---

### 8. Launch Power CAT Tools

- Return to [make.powerapps.com](https://make.powerapps.com)
- Navigate to **Apps**
- Open the newly installed **Power CAT Tools** model-driven app

![image](https://github.com/user-attachments/assets/a74231a4-9195-4e4e-b495-673e549a0ce4)

![image](https://github.com/user-attachments/assets/f50e6973-a130-4da3-8015-34934f01f2d2)

---

## Option 2: Install using Power Platform Package Deployer (via pac CLI)

This option allows you to manually install the Power CAT Tools solution using the Power Platform CLI (`pac`).  
Use this method if you prefer deploying from a package deployer `.zip` file instead of AppSource.

---

#### Step 1: Prerequisites

- Install the [Power Platform CLI](https://learn.microsoft.com/power-platform/developer/cli/introduction) on your machine
- Download the solution package  
  Navigate to the [Releases](../../releases) section of this GitHub repository and from the latest release, download: `PowerCATToolkit_Package_Deployer.zip`

---

#### Step 2: Connect to Your Dataverse Environment

1. Open **Command Prompt**:
   - Press `Win + R`, type `cmd`, and press `Enter`
2. In the Command Prompt window, run the following command to authenticate and connect to your Dataverse environment:

  ```bash
  pac auth create -env "<YOUR-ENVIRONMENT-URL>"
  ```
  > Replace 'YOUR-ENVIRONMENT-URL' with the URL of your Dataverse environment (e.g., https://yourorg.crm.dynamics.com/)
 
---

#### Step 3: Deploy the Solution Package

1. Ensure you have downloaded the deployment package from the latest Releases: 'PowerCATToolkit_Package_Deployer.zip`

2. In the same Command Prompt window, run the following command to deploy the solution:

  ```bash
  pac package deploy -p "<FULL-PATH-TO-ZIP-FILE>" --logConsole
  ```
  > Replace the path 'FULL-PATH-TO-ZIP-FILE' with the actual file location where you saved the 'PowerCATToolkit_Package_Deployer.zip` file.

---

#### Step 4: Verify the Solution in Your Environment

After a successful deployment, follow these steps to confirm the Power CAT Tools solution is installed:

1. Open [make.powerapps.com](https://make.powerapps.com)
2. From the top-right corner, ensure you're in the **correct environment** where you deployed the solution
3. In the left navigation pane:
   - Click on **Apps**
   - Confirm that the **Power CAT Tools** model-driven app is listed and can be opened

![image](https://github.com/user-attachments/assets/a74231a4-9195-4e4e-b495-673e549a0ce4)

---

## Upgrade the solution using Power Platform CLI (`pac`)

> This step is only required if you already have the **Power CAT Tools** solution installed and want to upgrade to a newer version.

This section guides you through upgrading the **Power CAT Tools** solution using the **Power Platform CLI (`pac`)**.

This method is ideal when deploying a newer version of the managed solution downloaded from GitHub Releases.

---

#### Step 1: Prerequisites

- Install the [Power Platform CLI](https://learn.microsoft.com/power-platform/developer/cli/introduction) on your machine
- Download the solution package  
  Navigate to the [Releases](../../releases) section of this GitHub repository and from the latest release, download: `PowerCATToolkit_Package_Deployer.zip`

---

#### Step 2: Connect to Your Dataverse Environment

1. Open **Command Prompt**:
   - Press `Win + R`, type `cmd`, and press `Enter`
2. In the Command Prompt window, run the following command to authenticate and connect to your Dataverse environment:

  ```bash
  pac auth create -env "<YOUR-ENVIRONMENT-URL>"
  ```
  > Replace 'YOUR-ENVIRONMENT-URL' with the URL of your Dataverse environment (e.g., https://yourorg.crm.dynamics.com/)
 
---

#### Step 3: Upgrade the Solution

1. Ensure you have downloaded the correct **managed solution file** from the latest GitHub release:  
   `PowerCATToolkit_xx.xxx.xxxx_managed.zip`

2. Use the following command to upgrade the solution:

   ```bash
   pac solution import --path "<FULL-PATH-TO-DOWNLOADED-ZIP>" --import-as-holding
   ```
  > Replace <FULL-PATH-TO-DOWNLOADED-ZIP> with the full file path to the downloaded PowerCATToolkit_xx.xxx.xxxx_managed.zip file from the GitHub Releases section.

---

#### Step 4: Finalize & Verify the Upgrade

1. After the import completes successfully:
   - Open [make.powerapps.com](https://make.powerapps.com)
   - Select the **correct environment** from the environment selector
   - Navigate to **Solutions**
   - Confirm that the **Power CAT Tools** solution is listed with the updated version

2. To validate functionality:
   - Go to **Apps**
   - Open the **Power CAT Tools** model-driven app
   - Confirm that it loads without issues and reflects any new features or updates introduced in the new version
  
---

#### Important Note on Target Environment

The upgrade process is applied to the environment that was configured in  
**`Step 2: Connect to Your Dataverse Environment`** using the `pac auth create` command.

If you need to upgrade the solution in additional environments, you must:

1. Re-run `pac auth create` and connect to the **new target environment**
2. Repeat the steps outlined in **`Step 3: Upgrade the Solution`**

This ensures that each environment receives the upgraded solution package independently.
