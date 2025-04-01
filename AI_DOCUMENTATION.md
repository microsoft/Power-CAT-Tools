# AI Solution Documentation

The AI automated documentation tool assists makers in streamlining the creation of comprehensive solution documentation by leveraging AI-driven analysis. Users simply pick a solution from their Power Platform environment or upload a solution file and the tool generates a detailed Word document with insights and documentation for the solution using a configurable predefined structure.

![image](https://github.com/user-attachments/assets/3ae71f5a-6da4-407b-856e-033a42bbb3b5)

# Prerequisites

1. **Microsoft Dataverse Environment** – Ensure AI Builder prompts are enabled in the admin center.  
   📌 [Enable AI Builder in Dataverse](https://learn.microsoft.com/ai-builder/administer#enable-or-disable-ai-prompts-in-power-platform-and-copilot-studio)  

2. **AI Builder Credits** – Verify that AI Builder credits are assigned to your environment.  
   📌 [AI Builder licensing and credits](https://learn.microsoft.com/ai-builder/credit-management)  

3. **Creator Kit Core** (*Not required for AppSource installation*) – Ensure the latest Creator Kit Core is installed.  
   📌 [Microsoft Creator Kit](https://aka.ms/creatorkitdownload)  


## Choose a solution to document

The tool provides flexibility for users to either:
1. Select a solution: Directly choose a solution from the Power Platform environment for automated documentation.
1. Upload a solution: Upload a solution file (e.g., a .zip file) for offline documentation generation.

![image](https://github.com/user-attachments/assets/81535961-134a-4415-b9f4-5877d797192a)

## Automated documentation generation

Once the solution is submitted, the tool automatically scans the solution components, including apps, flows, tables, connections, and more. With the information pulled, it generates a structured Word document with detailed sections on solution architecture and component details.

Users can define the predefined template structure to tailor the documentation format and include or exclude specific sections based on project requirements.

Review a summary preview of the documentation before final export.

## Export the Document in Word, Markdown or PDF format

Click Export to Word, Export to PDF or Export to Markdown to download the comprehensive documentation.

![image](https://github.com/user-attachments/assets/463ba40d-de57-47e5-baa1-8290b4e7bbb7)

## Documentation structure

The generated Word document provides detailed information about the solution, including:

- **Overview**
  - Solution Overview
  - Solution Details
  - Architecture Diagram
  - Prerequisites

- **UX and Automations**
  - Canvas Apps / Custom Pages
  - Power Automate Flows
  - Custom Controls

- **Data and Security**
  - Plugins
  - Tables
  - Entity Relationship Diagram
  - Custom APIs
  - AI Model(s)
  - Security Role(s)

- **Summary**

## Limitations

- You **cannot edit** an existing saved document from within the application.
- The **Entity Relationship Diagram** will **not be generated** if the solution contains **more than 25 tables**.
- The **Solution Architecture Diagram** may appear **crammed** for complex solutions, especially when an app is bound to a **large number of tables or flows**.

