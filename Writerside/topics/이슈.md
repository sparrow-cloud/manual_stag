# Issue

## Issue type

Issues can be categorised as Source Issues, Component Issues, or Web Vulnerability Issues, depending on the analysis engine that detected the issue.

- Source issues: Issues detected through source code analysis.
  - Security vulnerability: A potential vulnerability in the source code that is related to software security.
  - Quality issues: Issues that do not cause security issues in the source code, but should be reviewed from a quality perspective.
- Supply Chain issues: Issues detected through component analysis.
  - Vulnerable component: An issue that is considered vulnerable because a vulnerability has been found in the component itself.
  - Licence: Issues where the open source licence used by the component contains a copyleft or permissive licence.
- Web App Issues: Issues detected through web vulnerability analysis.


## Issue risk

Sparrow Cloud categorises recent issues detected in your project into five levels of risk. The risk level helps users understand how dangerous a detected issue is. For example, for source code issues, a **very high** risk level indicates urgent issues that need to be addressed immediately, while **very low** includes issues that do not have a significant impact on security or quality.

These risk levels are the same as the risk level of the rule that detects the issue. The risk level is assigned based on the description of the compliance that the issue detection rule is based on. There are five levels of risk, starting with the most risky issues and moving up: **Very High**, **High**, **Moderate**, **Low**, and **Very Low**.


## Issue status

Once an issue is detected, it needs to be verified and resolved, or it needs to be handled to exclude it from the issue due to false positives or other reasons. To indicate how the issue was handled, we display the **issue status** for each issue as follows

- Unconfirmed: The issue has not yet been reviewed by an assigned person.

- Confirmed: The issue has been reviewed by an assigned person.

- Resolved: The rep has resolved the issue found in the issue.


## Excluded issues

Some detected issues are potentially problematic but not actually security vulnerabilities or quality issues. In these cases, the **Issue Exclusion** feature was created to allow users who are experts in security diagnostics to exclude certain issues from the problem.

To exclude an issue, click the **Exclude issue** button at the bottom of the issue details. Issues excluded through this feature are designed to not appear in the issue list. They are also not included in the issue count for the project.



