# Power CAT Tools

The **Power CAT Tools** app is your ultimate companion for enhancing your development experience within Microsoft Power Platform. This powerful suite of features is designed to streamline your development workflow by automating essential tasks and providing insightful guidance based on real-world best practices. Whether you're a seasoned developer or just getting started, Power CAT Tools offers valuable resources to help you build robust and efficient solutions with greater ease.

![Home](https://github.com/user-attachments/assets/55eeb901-60d4-454d-85d5-660e504be61c)

## Features

### Power Platform code review
The Code Review Tool automatically analyzes your code to ensure compliance with best practices and standards. It helps makers and advanced makers detect and resolve potential issues early in development, resulting in higher-quality code and reduced technical debt.

More information on [code review](CODE_REVIEW.md)

### AI solution documentation

Leveraging artificial intelligence, this feature creates detailed and accurate documentation for your solutions. It saves makers and advanced makers time and effort, ensuring that documentation is always up-to-date and comprehensive.

More information on [AI solution documentation](AI_DOCUMENTATION.md)

### Security roles risk assessment

The Risk Assessment feature evaluates potential risks in your solutions and provides actionable mitigation strategies. This proactive approach helps admins address risks early, ensuring the stability and security of their solutions.

More information on [risk assessment](RISK_ASSESSMENT.md)

### API playground

Offering a Postman-like experience, the API Playground allows developers to test and explore APIs seamlessly. It simplifies the process of integrating and debugging APIs, enhancing overall productivity.

More information on [API playground](https://learn.microsoft.com/power-apps/maker/data-platform/dataverse-accelerator/api-playground)

### Plugin monitor

This tool monitors and analyzes plugin performance and behavior, providing insights into plugin efficiency and helping developers optimize their plugins for better performance. 

More information on [plugin monitor](https://learn.microsoft.com/power-apps/maker/data-platform/dataverse-accelerator/plugin-monitoring)

## Get started

See [setup information and installation instructions](./SETUP.md). 

## Latest release

The latest shipped version is available via **[Releases](https://github.com/microsoft/Power-CAT-Tools/releases)**. From there, you can download the latest version of all managed solutions that have been tested and are ready for use. 

Stay up to date with our releases by **subscribing** to them: 
1. Select **Watch**
2. Select **Custom** > **Releases** > **Apply** to receive notifications about our releases

### Important Note
Power Platform Review Tool and AI Documentation rely on the YAML representation of canvas apps when reading Canvas Apps. To ensure compatibility, export the solution from an early release cycle environment if you intend to use the Upload Solution option for reviewing or generating technical documentation.
For more details, see : [View source code files for canvas apps](https://learn.microsoft.com/en-us/power-apps/maker/canvas-apps/power-apps-yaml).

# About this GitHub repo

The Power CAT Tools GitHub Repo contains the source, releases, issues and backlog items of all components that are part of the Power CAT Tools solution.

## Submit feedback

Let us know by filing an issue. 
Before submitting your issue please search the [issues](https://github.com/microsoft/Power-CAT-Tools/issues) to ensure your issue has not already been reported

If your bug or feature request has already been reported, join the conversation by commenting and adding your reaction. Please use reactions to vote and not "+1" comments.
- 👍: upvote
- 👎: downvote

## Microsoft Open Source Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).

Resources:

- [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)
- [Microsoft Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)
- Contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with questions or concerns

## Trademarks 

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft trademarks or logos is subject to and must follow [Microsoft’s Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general). Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship. Any use of third-party trademarks or logos are subject to those third-party’s policies.

## Security

Microsoft takes the security of our software products and services seriously, which includes all source code repositories managed through our GitHub organizations, which include [Microsoft](https://github.com/Microsoft), [Azure](https://github.com/Azure), [DotNet](https://github.com/dotnet), [AspNet](https://github.com/aspnet), [Xamarin](https://github.com/xamarin), and [our GitHub organizations](https://opensource.microsoft.com/).

If you believe you have found a security vulnerability in any Microsoft-owned repository that meets Microsoft's [Microsoft's definition of a security vulnerability](https://docs.microsoft.com/en-us/previous-versions/tn-archive/cc751383(v=technet.10)), please report it to us as described below.

## Reporting Security Issues

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report them to the Microsoft Security Response Center (MSRC) at [https://msrc.microsoft.com/create-report](https://msrc.microsoft.com/create-report).

If you prefer to submit without logging in, send email to [secure@microsoft.com](mailto:secure@microsoft.com).  If possible, encrypt your message with our PGP key; please download it from the the [Microsoft Security Response Center PGP Key page](https://www.microsoft.com/en-us/msrc/pgp-key-msrc).

You should receive a response within 24 hours. If for some reason you do not, please follow up via email to ensure we received your original message. Additional information can be found at [microsoft.com/msrc](https://www.microsoft.com/msrc).

Please include the requested information listed below (as much as you can provide) to help us better understand the nature and scope of the possible issue:

  * Type of issue (e.g. buffer overflow, SQL injection, cross-site scripting, etc.)
  * Full paths of source file(s) related to the manifestation of the issue
  * The location of the affected source code (tag/branch/commit or direct URL)
  * Any special configuration required to reproduce the issue
  * Step-by-step instructions to reproduce the issue
  * Proof-of-concept or exploit code (if possible)
  * Impact of the issue, including how an attacker might exploit the issue

This information will help us triage your report more quickly.

If you are reporting for a bug bounty, more complete reports can contribute to a higher bounty award. Please visit our [Microsoft Bug Bounty Program](https://microsoft.com/msrc/bounty) page for more details about our active programs.

For more information read the [FAQ](./FAQ.md)
