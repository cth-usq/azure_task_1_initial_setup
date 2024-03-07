# Azure Lab Setup

Welcome to the striking world of cloud computing! This is the first task in the module, and its purpose is to ensure that you have prepared the required infrastructure and to get used to the task format. 

Tasks in this module are relying on 2 PowerShell scripts: 

- `scripts/generate-artifacts.ps1` generates the "artifacts" and uploads them to cloud storage. An "artifact" is evidence of a task completed by you. Each task will have its script, which will gather the required artifacts. The script also adds a link to the generated artifact in the `artifacts.json` file in this repository — make sure to commit changes to this file after you run the script. 
- `scripts/validate-artifacts.ps1` validates the artifacts generated by the first script. It loads information about the task artifacts from the `artifacts.json` file.   

## Prerequisites

Before completing any task in the module, make sure that you followed all the steps described in the **Environment Setup** topic, in particular: 

1. Ensure you have an [Azure](https://azure.microsoft.com/en-us/free/) account and subscription.
2. Create a resource group called *"mate-academy"* in the Azure subscription.
3. In the *"mate-academy"* resource group, create a storage account (any name) and a *"task-artifacts"* container.
4. Install [PowerShell 7](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell?view=powershell-7.4) on your computer. All tasks in this module use Powershell 7. To run it in the terminal, execute the following command: 
    ```
    pwsh
    ```
5. Install [Azure module for PowerShell 7](https://learn.microsoft.com/en-us/powershell/azure/install-azure-powershell?view=azps-11.3.0): 
    ```
    Install-Module -Name Az -Repository PSGallery -Force
    ```
If you are a Windows user, before running this command, please also run the following: 
    ```
    Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
    ```
6. Log in to your Azure account using PowerShell:
    ```
    Connect-AzAccount -TenantId <your Microsoft Entra ID tenant id>
    ```

## Requirements

In this task, you need to perform the following steps: 

1. Start PowerShell 7 and run the script for generating artifacts: 
    ```
    scripts/generate-artifacts.ps1
    ``` 
    The script will prompt you only for one parameter: the name of the storage account you created when completing the pre-requirements. 

2. If you want to test your solution before submitting it, run the script for artifacts validation: 
    ```
    scripts/generate-artifacts.ps1
    ```
    The script should run without errors. 

3. Commit your changes and submit your solution for review. 
