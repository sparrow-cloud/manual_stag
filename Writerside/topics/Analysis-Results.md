---
switcher-label: Language
---
# Check Results

## 결과 확인하기 {switcher-key="한국어"}

### 최근 분석

프로젝트에서 확인할 수 있는 결과는 **최근 분석**에서 발견한 내용이 포함됩니다. 여기서 **최근 분석**이란 다음 두 가지를 포함합니다: 1) 리포지토리 및 압축 파일을 비롯한 **파일** 자산을 대상으로 수행한 마지막 분석, 2) 웹 페이지를 가리키는 **URL** 자산을 대상으로 수행한 마지막 분석. 즉, 최근 분석에는 최대 2개의 분석 결과가 함께 표시될 수 있습니다.

> **Tip**: **최근 분석** 이전에 수행한 분석 결과의 내용을 확인하려면 최근 분석을 삭제하세요. 분석을 삭제하려면 [분석 상세 정보](#분석-상세-정보)를 참고하세요.

프로젝트의 오른쪽에 있는 **요약**, **레퍼런스**, **이슈**, **자산**, **컴포넌트**라는 다섯 개의 탭을 클릭해서 상세한 결과를 확인하세요.

<img src="프로젝트상세01.png" />

### 분석 상세 정보 

**분석 목록**에서 프로젝트에서 수행한 분석에 대한 전반적인 데이터를 확인할 수 있습니다. 여기에는 분석의 **진행 상황**, **분석 시간**, **분석 시작 일시**, **분석 대상**, **위험도별 이슈 수** 등이 포함됩니다.

<img src="분석상세.png" />


#### 분석 데이터가 표시되지 않는 경우

분석이 실패하는 경우 프로젝트 요약에는 분석 결과가 표시되지 않게 됩니다. 이 때 **분석 상세 정보**를 보면 분석이 실패했으며 실패의 원인이 무엇인지를 확인하실 수 있습니다.

> **Tip**: 분석이 완료된 경우임에도 프로젝트 요약에 분석 결과가 표시되지 않았다면 **분석 상세 정보**에서 **위험도별 이슈 수**가 0이 아닌지를 확인하세요.

#### 과거 분석 데이터를 확인하려는 경우

앞서 설명한 것처럼 프로젝트 요약에는 [**최근 분석**](#최근-분석)만 표시됩니다. 만약 사용자가 프로젝트에서 수행한 다른 분석 결과를 확인하려는 경우 해당 분석 이후에 수행된 모든 분석을 삭제하는 방식으로 과거의 분석 결과를 확인하실 수 있습니다.

> **Warning**: 일단 삭제된 데이터는 다시 복구할 수 없다는 점에 유의하세요.


### 레퍼런스

**레퍼런스**는 분석 대상에서 검출한 이슈와 연관된 레퍼런스 및 레퍼런스 항목을 표시하고 최근 이슈 중에서 레퍼런스 항목에 해당하는 이슈의 개수를 표시합니다.

레퍼런스에 대한 더 자세한 내용은 [레퍼런스](Reference.md)를 참고하세요.

### 이슈 

**이슈**는 분석 대상을 분석한 결과로써 발견한 보안 취약점 및 품질 관련 문제를 가리킵니다. **이슈** 탭에 표시되는 **이슈 목록**에는 Sparrow Cloud에서 검출한 이슈가 포함되어 있습니다. 이슈는 검출한 도구에 따라서 **소스코드 이슈**, **오픈소스 이슈**, **웹취약점 이슈**로 분류됩니다.

이슈에 대한 더 자세한 내용은 [이슈](Issue.md)를 참고하세요.


### 자산 

Sparrow Cloud는 **자산**이라는 분석 결과를 표시합니다. 자산은 분석에 사용한 분석 대상에서 생성됩니다: 분석 대상에 포함된 파일이나 하위 URL을 식별하고 이 정보로 **자산 목록**을 보여줍니다. 분석 대상에 따라서 소스코드 분석과 오픈소스 분석에 사용된 리포지토리에서 식별한 자산은 **파일**로 표시되고, 웹취약점 분석에 사용된 웹 페이지에서 식별한 자산은 **URL**로 표시됩니다.

자산에 대한 더 자세한 내용은 [자산](Asset.md)을 참고하세요.


### 컴포넌트 

**컴포넌트**란 특정 프로그램을 식별할 수 있는 최소 단위이며 라이선스가 필요한 소프트웨어, 독점 소프트웨어, 오픈소스 소프트웨어 등을 가리킵니다. Sparrow Cloud에서는 분석 대상 파일에 포함된 소프트웨어가 무엇인지를 식별하기 위해 파일을 컴포넌트로 나누어서 분석합니다. 그리고 컴포넌트가 사용하고 있는 오픈소스 라이선스를 **컴포넌트** 탭의 개별 컴포넌트에 정리합니다. 또한, 특정 라이선스에 해당하는 컴포넌트는 이슈 목록에서 이슈로 검출됩니다.

컴포넌트에 대한 더 자세한 내용은 [컴포넌트](Component.md)를 참고하세요.


## Analysis results {switcher-key="English"}

### Recent Analyses

The results you can see in your project include the findings from your **recent analyses**. In this context, "recent analyses" includes two things 1) the last analysis performed on **file** assets, including repositories and compressed files, and 2) the last analysis performed on **URL** assets, which point to web pages. This means that up to two analyses can be shown together in Recent Analyses.

> **Tip**: Note that if you check analyse results before **Recent Analyses**, delete **Recent Analyses**. See [Analysis details](#analysis-details) for more information.

To see detailed results, click the five tabs on the right side of the project: **Summary**, **Reference**, **Issue**, **Asset**, and **Component**.

<img src="projdetails01.png" />


### Analysis details

**Analysis List** shows more data from the analysis conducted in the project: including **Status**, **Analyzing time**, **Started time**, **Analyzing target**, **Risk level and issues** and etc.

<img src="analysisDetails.png" />


#### Cannot check results in Project summary.

When the analysis fails, no results have shown in the Project summary. Then, go to the **Analysis details** to check that the analysis fails and what makes it fails as well.

> **Tip**: For a completed analysis, and it does not show any results, check that **Risk level and issues** shows zero in the **Analysis details**.

#### Want to view results from the previous analysis.

As mentioned earlier, Project summary only shows data about [**Recent analyses**](#Recent-Analyses). If you want to check previous analysis results from the project, you can see the results by deleting all subsequent analyses performed after that analysis.

> **Warning**: Note that the deleted data cannot be restored.


### References

**References** show references and reference chapters, and presents the related number of issues detected on the recent analysis.

For more information about the references, see [Reference](Reference.md).

### Issues 

**Issues** are security vulnerabilities and quality problems found as a result of analysing your analysis targets. The **Issues list** displayed in the **Issue** tab contains the issues detected by Sparrow Cloud. Issues are categorised as code issues, open source issues, or web app issues, depending on the tool that detected them.

For more information about the issues, see [Issue](Issue.md).


### Assets 

Sparrow Cloud displays analysis results called **Assets**. Assets are generated from the analysis target you used for analysis: It identifies the files or sub URLs contained in the analyse target and uses this information to show a list of **assets**. Depending on the analysis target, assets identified from repositories used for code and open source analysis are shown as **Files**, while assets sourced from web pages used for web app analysis are shown as **URLs**.

For more information about assets, see [Asset](Asset.md).


### Components 

**Components** are the smallest units that can identify a specific program and refers to software that requires a licence, proprietary software, open source software, etc. Sparrow Cloud breaks down files into components to identify what software is included in the file being analysed, and organises the open source licences that the components are using into individual components on the **Component** tab. Components that are under a specific licence are also detected as issues in the issue list.

For more information about components, see [Component](Component.md).