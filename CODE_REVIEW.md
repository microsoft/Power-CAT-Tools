# Power Platform code review tool 

The Power Apps Code Review Tool is designed to streamline the evaluation of canvas apps by providing a comprehensive analysis framework. Leveraging the Power Apps Language Tooling library, this tool offers a customizable checklist of best practices, an overview of app checker results, insights into app settings, and a code/formula viewer with advanced search capabilities.

## Features
Today, the tool supports these features:

- **Customizable checklist**. The tool presents a series of patterns to examine within your application. Users can mark each pattern as pass or fail, add comments for app makers, or view additional details. Some items are automatically assessed based on detectable patterns during the initial review setup.
  
- **App Checker Integration**. Displays results from the app checker as of the app's last publication. While these results are accessible in Power Apps Studio during development, their inclusion here provides a consolidated view, helping to identify critical issues like inefficient loading or delegation problems.
  
- **App analysis**. Offers a quick assessment of essential app settings that impact performance. This section includes:
  - Screen Information: Counts the number of controls per screen to ensure it remains below the recommended maximum of 300 controls.
  - Media Files: Lists all embedded media along with their sizes.
  - Network Trace: Identifies slow network requests within the app.
    
- **Code Viewer**. Lists all screens, controls, and properties with search and filter functions, allowing users to quickly locate formulas within the app. Users can search by control name, property, or any text present in Power Apps formulas. Additionally, formulas can be linked to specific patterns, aiding in providing precise feedback to app developers.

## Creating a review

Upon launching the Power Apps Code Review Tool, you are presented with a list of existing reviews and the option to create a new one.

### Select a solution for a new review

The tool allows you to select specific solutions for evaluation. Follow these steps to initiate a review for a solution:

1. Open the Code Review Tool: Navigate to the Power Platform environment where your solution is hosted.
2. Select a Solution: From the solution list, choose the solution containing the canvas app(s) you want to review.
3. Review Setup: The tool will load all relevant apps within the selected solution. You can choose to review all or specific apps.

This selection ensures that the review process is focused and relevant to your development objectives.

![image](https://github.com/user-attachments/assets/6071cfea-bb6d-41f7-bad8-59c06476f614)

### Reading a review

After selecting and reviewing a solution, the tool provides detailed analysis results.

#### Summary dashboard

The summary dashboard offers a high-level view of the review findings, including:

-  Checklist completion status: Displays the number of patterns passed, failed, or pending review.
-  App checker issues: Highlights critical warnings and errors detected during the review.
-  Performance Metrics: Provides insights into app complexity and media usage.

![image](https://github.com/user-attachments/assets/d54fe2c3-7773-41f6-a494-6321565e149a)

#### Detailed insights

![image](https://github.com/user-attachments/assets/d6cfb441-7cc1-49dc-9d4f-3eaa6559735d)

- Pattern details: Each pattern includes a status indicator, comments, and links to supporting documentation.
- Code insights: View detailed formula breakdowns, search for specific control properties, and link directly to areas of concern.
- App settings: Analyze key settings affecting app performance, such as control limits and data connections.

By reviewing these results, developers and reviewers can identify and prioritize areas for improvement, ensuring that canvas apps adhere to best practices and maintain optimal performance.

## Troubleshooting

- Incase you see a the below message while reviewing canvas app, follow any one of the options shared below under **Solution Update Options** section.

`Note: It appears that solution used in this review is outdated. Please re-export the solution and re-upload to ensure all patterns are executed.`

![image](https://github.com/user-attachments/assets/bc3a9199-e5a4-4231-988b-652ae4afd2e9)

####  Solution Update Options

#####  Option 1: Re-export from Early Release Environment

Please re-export the solution from an early release cycle environment.  
You can refer to the following link for guidance:  
🔗 [Early Access Features - Power Platform](https://learn.microsoft.com/en-us/power-platform/admin/early-release)

---

#####  Option 2: Manual Update via Power Apps Studio

Alternatively, you can manually import the app (`.msapp`) in Power Apps Studio:

1. Use the **Download a copy** option to get the latest `.msapp` file.
2. Unzip the Power Platform solution package.
3. Inside the `CanvasApps` folder, create a new `src` folder (if it doesn't exist).
4. Place the new `.msapp` file inside the `src` folder.
5. Re-zip all the solution components.
6. Review and import the updated solution again.

