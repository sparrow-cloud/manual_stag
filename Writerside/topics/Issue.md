---
switcher-label: Language
---

# Issue


## 이슈 유형 {switcher-key="한국어"}

이슈는 해당 이슈를 검출한 분석 엔진에 따라서 **소스코드 이슈**, **컴포넌트 이슈**, **웹 취약점 이슈**로 나눌 수 있습니다.

- 소스코드 이슈: 소스코드 분석을 통해 검출된 이슈입니다.
  - 보안 취약점: 소스코드에 잠재된 취약점 중 소프트웨어 보안과 관련된 문제입니다.
  - 품질 문제: 소스코드에 보안 문제를 발생시키지 않지만 품질 측면에서 검토해야 하는 문제입니다.
- 컴포넌트 이슈: 컴포넌트 분석을 통해 검출된 이슈입니다.
  - 취약한 컴포넌트: 컴포넌트 자체에서 취약점이 발견되었기 때문에 취약하다고 판단되는 문제입니다.
  - 라이선스: 컴포넌트에서 사용하는 오픈소스 라이선스 중에서 카피레프트 라이선스 혹은 허용적 라이선스가 포함된 문제입니다.
- 웹 취약점 이슈: 웹 취약점 분석을 통해 검출된 이슈입니다.


## 이슈 위험도 

Sparrow Cloud는 프로젝트에서 검출된 최근 이슈를 위험한 정도에 따라 5단계로 구분합니다. 사용자는 위험도를 통해 검출된 이슈가 얼마나 위험한 문제인지를 파악할 수 있습니다. 예를 들어, 소스코드 이슈에서 **매우 높음** 위험도는 당장 해결해야 하는 시급한 문제를 가리키며, **매우 낮음**은 보안이나 품질에 큰 영향을 미치지 않는 문제를 포함합니다.

이러한 위험도는 이슈를 검출하는 규칙의 **위험도**와 동일합니다. 위험도는 이슈 검출 규칙이 기초하고 있는 컴플라이언스의 설명에 기반하여 지정됩니다. 가장 위험한 이슈부터 차례대로 **매우 높음**, **높음**, **보통**, **낮음**, **매우 낮음**과 같은 5개의 단계로 구분됩니다.


## 이슈 상태 

이슈가 검출되면 해당 이슈를 확인하고 해결하거나, 오탐 또는 다른 원인으로 인해 이슈에서 제외하도록 처리해야 합니다. 이슈를 어떻게 처리했는지 표시하기 위해서 이슈마다 **이슈 상태**를 다음과 같이 표시합니다.

- 미확인: 담당자가 검출된 이슈를 아직 검토하지 않음.
- 확인: 담당자가 해당 이슈를 확인함.
- 해결: 담당자가 해당 이슈에서 발견된 문제를 해결함.


## 이슈 제외 

검출된 이슈 중에는 잠재적으로 문제가 될 가능성이 있을 뿐 실제로 보안 취약점 혹은 품질 문제라고 볼 수 없는 경우가 있습니다. 이러한 경우 보안 진단 전문가라고 할 수 있는 사용자가 특정 이슈를 문제에서 제외시킬 수 있도록 만든 기능이 **이슈 제외**입니다.

이슈 상세 정보 페이지에 있는 **이슈 제외** 버튼을 클릭하면 이슈가 제외됩니다. 이 기능을 통해 제외된 이슈는 이슈 목록에 표시되지 않도록 설계되어 있습니다. 또한 제외된 이슈는 프로젝트에서 계산하는 이슈 수에도 포함되지 않습니다.



## Issue type {switcher-key="English"}

Issues can be categorised as Source Issues, Supply Chain Issues, or Web Vulnerability Issues, depending on the analysis engine that detected the issue.

- Source issues: Issues detected through source code analysis.
  - Security vulnerability: A potential vulnerability in the source code that is related to software security.
  - Quality issues: Issues that do not cause security issues in the source code, but should be reviewed from a quality perspective.
- Supply Chain issues: Issues detected through supply chain analysis.
  - Vulnerable component: An issue that is considered vulnerable because a vulnerability has been found in the component itself.
  - Licence: Issues where the open source licence used by the component contains a copyleft or permissive licence.
- Web vulnerability issues: Issues detected through web vulnerability analysis.


## Issue risk 

Sparrow Cloud categorises recent issues detected in your project into five levels of risk. The risk level gives users an idea of how dangerous a detected issue is. For example, in source code issues, a **Very High** risk level indicates urgent issues that need to be addressed immediately, while **Very Low** includes issues that do not have a significant impact on security or quality.

These risk levels are the same as the risk level of the rule that detects the issue. The risk level is assigned based on the description of the compliance that the issue detection rule is based on. There are five levels of risk, starting with the most risky issues and moving up: **Very High**, **High**, **Moderate**, **Low**, and **Very Low**.


## Issue status 

When an issue is detected, it needs to be verified and resolved, or processed to exclude it from the issue due to false positives or other causes. To indicate how the issue has been handled, we display an **issue status** for each issue as follows

- Unchecked: The issue has not yet been reviewed by an assigned person.
- Checked: The issue has been reviewed by an assigned person.
- Resolved: The rep has resolved the issue found in the issue.


## Exclude an issue 

Sometimes detected issues are only potentially problematic and not actually security vulnerabilities or quality issues. In these cases, the **Issue Exclusion** feature was created to allow users who are experts in security diagnostics to exclude certain issues from the problem.

To exclude an issue, click the **Exclude issue** button on the issue detail page. Issues excluded through this feature are designed to not appear in the issue list. They are also not included in the issue count for the project.



