---
switcher-label: Language
---
# Start Analyzing

## 분석하기 {switcher-key="한국어"}

이제 앞에서 생성한 프로젝트로 이동해서 분석을 수행하세요. **저장소** 또는 **URL**을 분석하기 위해서는 먼저 프로젝트를 설정해야 합니다. 자세한 내용은 [분석 설정하기](analysisSetting.md)를 참고하세요.

<img src="runAnalysis.png" alt="Alt text" width="450"/>

1. **새 분석 시작하기** 버튼을 클릭하세요.
2. **소스코드 및 컴포넌트** 분석을 시작하려면 **저장소** 또는 **압축 파일**을 선택하세요.
3. **웹 취약점** 분석을 시작하려면 **URL**을 선택하세요.
4. 이제 분석이 시작됩니다.

> **Tip**: 분석이 수행되는 동안 동일한 유형의 분석을 추가로 수행할 수 없습니다. 만약, 실행 중인 분석을 중지하려는 경우 분석 목록에서 해당 분석을 중지할 수 있습니다. 이미 완료된 분석은 중지하거나 삭제할 수 없다는 점에 유의하세요.


## Run Analysis {switcher-key="Korean"}

Now go to the project you created earlier and perform an analysis. To analyse a **repository** or **URL**, you must first set up a project, see [Setting up analysis](analysisSetting.md) for more information.

<img src="runAnalysis.png" alt="Alt text" width="450"/>

1. Click the **Start a new analysis** button.
2. Select a repository or compressed file to start analysing **Source code and components**.
3. Select **URL** to start analysing **Web Vulnerabilities**.
4. The analysis will now start.

> **Tip**: You cannot perform additional analyses of the same type while an analysis is running. If you want to stop a running analysis, you can do so from the list of analyses. Note that you cannot stop or delete an analysis that has already been completed.

### 압축 파일 분석하기 {switcher-key="한국어"}

최대 100 MB까지의 압축 파일을 분석할 수 있습니다. 서비스를 구독하지 않은 사용자는 10 MB 이하의 압축 파일을 분석할 수 있습니다. 


### Analysing zipped file {switcher-key="English"}

You can analyse compressed files up to 100 MB. Users without a subscription to the service can analyse compressed files of 10 MB or less.

#### SBOM 파일 {switcher-key="한국어"} 

이미 생성된 SBOM 파일을 압축한 다음, 분석을 수행해서 결과를 확인할 수 있습니다. 단, SBOM의 형식이 다양하기 때문에 아래에 해당하지 않는 파일은 컴포넌트 분석을 통해 결과가 수행되지 않을 수 있습니다.

- SPDX (.spdx): 버전 2.2
- CycloneDX (.json): 버전 1.4
- SWID tag(.swidtag): 버전 ISO/IEC 19770-2:2015

#### SBOM file {switcher-key="English"}

You can compress an SBOM file that has already been generated, and then run the analysis to see the results. However, due to the various formats of SBOMs, files that do not fall into the following categories may not result in component analysis.

- SPDX (.spdx): version 2.2
- CycloneDX (.json): Version 1.4
- SWID tag (.swidtag): Version ISO/IEC 19770-2:2015


### URL 분석하기 {switcher-key="한국어"}

#### 이벤트 클립보드 {switcher-key="한국어"}

**이벤트 클립보드**는 기본적으로 웹 페이지에서 수행한 이벤트를 기록하고 저장할 수 있는 도구입니다. 이러한 특징을 활용하여 사용자가 수행한 이벤트를 파일로 저장하여 [분석 옵션](Analysis-Option.md)에 입력함으로써 분석 범위를 확장할 수 있습니다. 분석 대상인 URL에 특정 ID와 비밀번호로 로그인하여야 하는 경우 **이벤트 클립보드**에서 해당 이벤트를 파일로 저장하고 **분석 옵션**의 **로그인 기록 파일**에 업로드하면 파일에 저장된 정보를 사용하여 분석을 진행합니다.

### Analysing URLs {switcher-key="English"}

#### Event Clipboard {switcher-key="English"}

The **Event Clipboard** is basically a tool that allows you to record and save events performed on a web page. You can use this feature to expand the scope of your analysis by saving the events performed by the user to a file and entering it into the [Analysis-Option.md]. If the URL you are analysing requires you to log in with a specific ID and password, you can save the event from the **Event Clipboard** to a file and upload it to the **Login History File** in **Analysis Options**, and the information stored in the file will be used for analysis.

#### 이벤트 클립보드 설치하기 {switcher-key="한국어"}

이벤트 클립보드는 Google Chrome 웹 브라우저의 확장 프로그램 형태로 제공됩니다. 따라서 이벤트 클립보드를 사용하기 위해서는 먼저 **Chrome 브라우저를 설치**하고 **Chrome 웹 스토어에서 이벤트 클립보드를 다운로드**해야 합니다.

[이벤트 클립보드 다운로드](https://chromewebstore.google.com/detail/sparrow-dast-event-clipbo/ikebmfjkmpkaacjablfdfdkonamgijdg?hl=en-US&utm_source=ext_sidebar)


#### Installing the Event Clipboard {switcher-key="English"}

The Event Clipboard is available as an extension to the Google Chrome web browser. Therefore, to use the Event Clipboard, you must first **install the Chrome browser** and **download the Event Clipboard from the Chrome Web Store**.

[Download Event Clipboard](https://chromewebstore.google.com/detail/sparrow-dast-event-clipbo/ikebmfjkmpkaacjablfdfdkonamgijdg?hl=en-US&utm_source=ext_sidebar)


#### 이벤트 클립보드 실행 및 재생 {switcher-key="한국어"}

이벤트 클립보드를 설치하셨다면, 이제 이벤트 클립보드를 실행해 보겠습니다.

1. Chrome 웹 브라우저를 실행하세요.
2. 주소 표시줄 오른쪽에 있는 Sparrow DAST 이벤트 클립보드 아이콘을 클릭하세요.
3. 이벤트 클립보드 창이 표시됩니다.
4. 이벤트 클립보드 창에서 '**시작 URL을 여기에 입력해주세요.**'를 클릭하고 시작 URL을 입력하세요.
5. **기록** 버튼을 클릭하면 입력한 URL로 이동합니다. 이제 기록할 이벤트를 수행하세요.
6. 로그인을 수행한 다음 이벤트 클립보드에서 **정지** 버튼을 클릭하여 기록을 완료합니다.
7. **저장** 버튼을 클릭해서 파일을 저장하세요.

#### Launch and run the Event Clipboard {switcher-key="English"}

Now that you've installed the Event Clipboard, let's run it.

1. launch the Chrome web browser.
2. Click the Sparrow DAST Event Clipboard icon on the right side of the address bar.
3. The Event Clipboard window will be displayed.
4. In the Event Clipboard window, click "**Please enter your start URL here**" and enter your start URL.
5. Click the **Record** button and you will be taken to the URL you entered. Now perform the event you want to record.
6. Log in and then click the **Stop** button in the event clipboard to complete the recording.
7. Click the **Save** button to save the file.


#### 이벤트 클립보드로 분석하기  {switcher-key="한국어"}

위에서 기록한 **로그인 기록 파일**을 사용하여 분석을 수행해보겠습니다.

1. **프로젝트 수정** 슬라이드에서 **웹 페이지 설정** 버튼을 클릭하세요.
2. **로그인 기록 파일** 옵션에서 **파일 찾아보기** 버튼을 클릭하세요. 
3. 저장한 이벤트 클립보드 파일을 선택하세요.
4. **웹 페이지 설정**에서 **설정하기** 버튼을 클릭하세요.
5. **프로젝트 수정**에서 **수정하기** 버튼을 클릭하세요.

> **Tip**: 이벤트 클립보드에서 로그인 동작을 기록하는 경우 리디렉션된 페이지부터 기록을 시작해야 합니다. 또한 로그인 후에 로그아웃 버튼을 클릭하는 것을 방지하기 위해 로그아웃 버튼을 분석 옵션에 있는 **이벤트 수행 제외 요소**에 추가하세요.


#### Analysing with the Event Clipboard {switcher-key="English"}

Let's use the **Login History File** we recorded above to perform an analysis.

1. click the **Web page settings** button on the **Modify project** slide.
2. Click the Browse for File button in the Login History File option.
3. select the saved event clipboard file.
4. Click the Set button in the Web page settings.
5. Click the **Modify** button under **Modify Project**.

> **Tip**: When recording login behaviour from the event clipboard, make sure to start recording from the redirected page. Also, to prevent clicking the logout button after login, add the logout button to the **Event Action Exclusions** in the Analytics options.
 