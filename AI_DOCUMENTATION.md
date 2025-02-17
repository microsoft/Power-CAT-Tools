# AI automated documentation

The AI automated documentation tool assists makers in streamlining the creation of comprehensive solution documentation by leveraging AI-driven analysis. Users simply pick a solution from their Power Platform environment or upload a solution file and the tool generates a detailed Word document with insights and documentation for the solution using a configurable predefined structure.

# Prerequisites

1. **Microsoft Dataverse Environment** – Ensure AI Builder prompts are enabled in the admin center.  
   - 📌 [Enable AI Builder in Dataverse](https://learn.microsoft.com/en-us/ai-builder/administrator-settings)  

2. **Permissions** – You must have the *System Customizer* security role.  
   - 📌 [Security roles in Dataverse](https://learn.microsoft.com/en-us/power-platform/admin/database-security)  

3. **AI Builder Credits** – Verify that AI Builder credits are assigned to your environment.  
   - 📌 [AI Builder licensing and credits](https://learn.microsoft.com/en-us/ai-builder/licensing)  

4. **Creator Kit Core** (*Not required for AppSource installation*) – Ensure the latest Creator Kit Core is installed.  
   - 📌 [Microsoft Creator Kit](https://learn.microsoft.com/en-us/power-platform/guidance/creator-kit/)  

5. **Power Apps Component Framework Feature** (*Not required for AppSource installation*) – Enable the Power Apps Component Framework Feature.  
   - 📌 [Enable PCF in Power Apps](https://learn.microsoft.com/en-us/powerapps/developer/component-framework/implementing-controls-using-powerapps-component-framework)  


## Choose a solution to document

The tool provides flexibility for users to either:
1. Select a solution: Directly choose a solution from the Power Platform environment for automated documentation.
1. Upload a solution: Upload a solution file (e.g., a .zip file) for offline documentation generation.

![image](https://github.com/user-attachments/assets/81535961-134a-4415-b9f4-5877d797192a)

## Automated documentation generation

Once the solution is submitted, the tool automatically scans the solution components, including apps, flows, tables, connections, and more. With the information pulled, it generates a structured Word document with detailed sections on solution architecture and component details.

Users can define the predefined template structure to tailor the documentation format and include or exclude specific sections based on project requirements.

Review a summary preview of the documentation before final export.

## Export the Word Document

Click Export to Word to download the comprehensive documentation.

## Documentation structure

The generated Word document provides detailed information about the solution, including:

- Solution Overview: High-level architecture and components
- Component Details
- Canvas Apps: Detailed app structure, screens, and controls
- Flows: Description of triggers, actions, and connections]
- Data Tables: Schema details and relationships
- Connectors: List of all external connections

