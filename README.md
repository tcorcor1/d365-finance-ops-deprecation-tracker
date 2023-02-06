<div align="center">
  <img alt="Commerce" src="/docs/img/Commerce_scalable.svg" height="50">
  <img alt="FinOps" src="/docs/img/Finance+Operations_scalable.svg" height="50">
  <img alt="SupplyChain" src="/docs/img/SupplyChainManagement_scalable.svg" height="50">
  <img alt="ProjectOps" src="/docs/img/ProjectOperations_scalable.svg" height="50">
  <img alt="CoreHR" src="/docs/img/CoreHR_scalable.svg" height="50">
  <h1>D365 Finance & Operations Deprecation Tracker</h1>
</div>

**:pushpin: For Power Platform deprecation announcements please see [Power Platform deprecation tracker](https://github.com/tcorcor1/power-platform-deprecation-tracker)**

Repository designed for tracking and notifying subscribers on changes to Microsoft Dynamics 365 Finance & Operations deprecation pages.

**Tracked pages as of 12/6/2022**:

- [Removed or deprecated features in Dynamics 365 Commerce](https://learn.microsoft.com/en-us/dynamics365/commerce/get-started/removed-deprecated-features-commerce)
- [Removed or deprecated features in Dynamics 365 Finance](https://learn.microsoft.com/en-us/dynamics365/finance/get-started/removed-deprecated-features-finance)
- [Removed or deprecated features in Dynamics 365 Supply Chain Management](https://learn.microsoft.com/en-us/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates)
- [Removed or deprecated features in Dynamics 365 Human resources](https://learn.microsoft.com/en-us/dynamics365/human-resources/get-started/removed-deprecated-features-hr)
- [Removed or deprecated features in Dynamics 365 Project Operations](https://learn.microsoft.com/en-us/dynamics365/project-operations/whats-new/removed-depreciated-features-project)
- [Removed or deprecated platform features](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/get-started/removed-deprecated-features-platform-updates)

I would love to track more pages and expand on this idea. If you have suggestions for pages please leave a comment on my [blog post](https://tldr-dynamics.com/blog/d365-finance-ops-deprecation-tracker) or drop an issue here.

### How it works

Every 12 hours, an Azure function will scrape pages and check for changes. If it finds updates, it will create a commit and release. If you watch this repo, you will receive an email upon each release.

If you don't want any emails, just star the repo and pop in once in a while to check out the history on the files, i.e. [/pages/d365-finance-deprecations.txt](https://github.com/tcorcor1/d365-finance-ops-deprecation-tracker/blob/main/pages/d365-finance-deprecations.txt).

### Tech used

- [HtmlAgilityPack](https://html-agility-pack.net/) - HTML parser written in C# to read/write DOM and supports plain XPATH or XSLT
- [Octokit](https://octokitnet.readthedocs.io/en/latest/) for .NET - A GitHub API client library for .NET
- Azure Functions
