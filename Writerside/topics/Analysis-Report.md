---
switcher-label: Language
---
# Report

## 분석 보고서  {switcher-key="한국어"}

Sparrow Cloud에서는 PDF 형식의 분석 보고서를 제공합니다. 프로젝트 상세의 **내보내기** 버튼을 클릭해서 최근 분석의 결과를 보고서로 출력하거나 다음과 같은 방법으로 특정 분석의 보고서를 출력하세요.


1. 프로젝트로 이동하세요.
2. 페이지 위에 있는 **분석 목록 조회하기** 버튼을 클릭하세요.
   <img src="분석목록.png" />
3. 보고서를 출력하려는 분석을 클릭하세요.
4. 슬라이드 아래에 있는 **보고서 내보내기** 버튼을 클릭하세요.
   <img src="보고서내보내기.png" />
5. 출력할 보고서의 **파일 이름**을 입력하세요.
6. **내보내기** 버튼을 클릭하세요.

> **Tip**: 완료된 분석의 보고서만 출력할 수 있습니다. 분석 보고서 파일이 너무 큰 경우 여러 개의 파일로 나뉘어서 출력됩니다. 보고서 파일 샘플을 확인하시려면 <a href="https://raw.githubusercontent.com/sparrow-cloud/cloud/925d2e7e4e64b7a43b74ccfd9147a04666348492/report-examples/file-report.pdf">파일 분석 보고서</a> 또는 <a href="https://raw.githubusercontent.com/sparrow-cloud/cloud/925d2e7e4e64b7a43b74ccfd9147a04666348492/report-examples/web-report.pdf">URL 분석 보고서</a>를 참고하세요.

보고서에는 다음과 같은 내용이 포함됩니다.

- 요약 정보         : 프로젝트 및 분석에 대한 간단한 정보.
- 위험도별 이슈 수   : 각 위험도에 해당하는 이슈 수.
- 레퍼런스별 이슈 수 : 검출된 이슈와 매핑된 레퍼런스 및 각 레퍼런스에 해당하는 이슈 수. 
- 이슈 상세 결과     : 이슈에 대한 설명, 해당하는 레퍼런스를 비롯한 이슈 유형에 따른 자세한 정보.
- 제외된 이슈 정보   : 제외된 이슈에 대한 정보.
- 이슈 검출 규칙 정보 : 이슈를 검출한 규칙의 목록.

<img src="보고서.png" />



## Export Report {switcher-key="English"}

Sparrow Cloud provides reports on the analysis in PDF format. Export the report of recent analysis from **Export** dropdown button in the Project or export the report of a certain analysis in the following way:


1. navigate to your project.
2. click the **View analysis list** button at the top of the page.
   <img src="analysisList.png" />
3. Click the analysis for which you want to print a report.
4. Click the **Export report** button below the slide.
   <img src="exportReport.png" />
5. Enter a filename for the report you want to print out.
6. Click the **Export** button.

> **Tip**: You can print out the report from completed analyses only. If the analysis report file is too large, it will be split into multiple files. For the report sample, click <a href="https://raw.githubusercontent.com/sparrow-cloud/cloud/925d2e7e4e64b7a43b74ccfd9147a04666348492/report-examples/file-report-en.pdf">Analyzed file report</a> or <a href="https://raw.githubusercontent.com/sparrow-cloud/cloud/925d2e7e4e64b7a43b74ccfd9147a04666348492/report-examples/web-report-en.pdf">Analyzed URL Report</a>.



The report contains the following content:

- Summary : brief information about the project and the analysis.
- Risk level and issues : the number of issues corresponding to each risk.
- Reference and issues : the references mapped to the detected issues and the number of issues corresponding to each reference.
- Issue details: detailed information for the issues, including a description and references.
- Excluded issues : information about excluded issues.
- Detection rules : list of detection rules.


<img src="report.png" />