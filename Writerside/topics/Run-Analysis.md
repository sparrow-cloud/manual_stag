---
switcher-label: Language
---
# Start Analyzing

## 분석하기 {switcher-key="한국어"}

이제 앞에서 생성한 프로젝트로 이동해서 분석을 수행하세요. **저장소, 압축 파일** 또는 **URL**을 분석하기 위해서는 먼저 프로젝트를 설정해야 합니다. 자세한 내용은 [분석 설정하기](analysisSetting.md)를 참고하세요.

<img src="분석실행.png" />

1. **새 분석 시작하기** 버튼을 클릭하세요.
2. **소스코드 및 오픈소스** 분석을 시작하려면 **저장소** 또는 **압축 파일**을 선택하세요.
3. **웹취약점** 분석을 시작하려면 **URL**을 선택하세요.
4. 이제 분석이 시작됩니다.

> **Tip**: 분석이 수행되는 동안 동일한 분석 대상을 추가로 분석할 수 없습니다. 만약, 실행 중인 분석을 중지하려는 경우 분석 목록에서 해당 분석을 중지할 수 있습니다.

### 저장소 분석하기

Sparrow Cloud에 등록한 이메일과 동일한 이메일의 GitHub 저장소에 업로드한 파일을 분석할 수 있습니다. 설정하는 방법은 [소스코드 저장소 설정하기](#analysissetting.md#소스코드-저장소-설정하기)를 참고하세요. 서비스를 구독하지 않은 사용자는 Public 저장소만 분석할 수 있습니다.

### 압축 파일 분석하기 

최대 100 MB까지의 압축 파일을 분석할 수 있습니다. 서비스를 구독하지 않은 사용자는 10 MB 이하의 압축 파일을 분석할 수 있습니다.


### URL 분석하기 

웹 사이트 URL을 분석하는 방법은 [분석 대상 웹 페이지 설정하기](#analysissetting.md#분석-대상-웹-페이지-설정하기)를 참고하세요. 서비스를 구독하지 않은 사용자는 일부 웹취약점 분석 옵션을 사용할 수 없습니다.

> **Warning**: 패스워드를 입력하는 로그인 이외의 추가적인 인증이 필요한 웹 사이트의 경우 분석을 수행할 수 없습니다.

#### 이벤트 클립보드 

**이벤트 클립보드**는 기본적으로 웹 페이지에서 수행한 이벤트를 기록하고 저장할 수 있는 도구입니다. 이러한 특징을 활용하여 사용자가 수행한 이벤트를 파일로 저장하여 [분석 옵션](Analysis-Option.md)에 입력함으로써 분석 범위를 확장할 수 있습니다. 분석 대상인 URL에 특정 ID와 비밀번호로 로그인하여야 하는 경우 **이벤트 클립보드**에서 해당 이벤트를 파일로 저장하고 **분석 옵션**의 **로그인 기록 파일**에 업로드하면 파일에 저장된 정보를 사용하여 분석을 진행합니다.

#### 이벤트 클립보드 설치하기 

이벤트 클립보드는 Google Chrome 웹 브라우저의 확장 프로그램 형태로 제공됩니다. 따라서 이벤트 클립보드를 사용하기 위해서는 먼저 **Chrome 브라우저를 설치**하고 **Chrome 웹 스토어에서 이벤트 클립보드를 다운로드**해야 합니다.

[이벤트 클립보드 다운로드](https://chromewebstore.google.com/detail/sparrow-dast-event-clipbo/ikebmfjkmpkaacjablfdfdkonamgijdg?hl=en-US&utm_source=ext_sidebar)

#### 이벤트 클립보드 실행 및 재생 

이벤트 클립보드를 설치하셨다면, 이제 이벤트 클립보드를 실행해 보겠습니다.

1. Chrome 웹 브라우저를 실행하세요.
2. 주소 표시줄 오른쪽에 있는 Sparrow DAST 이벤트 클립보드 아이콘을 클릭하세요.
3. 이벤트 클립보드 창이 표시됩니다.
4. 이벤트 클립보드 창에서 '**시작 URL을 여기에 입력해주세요.**'를 클릭하고 시작 URL을 입력하세요.
5. **기록** 버튼을 클릭하면 입력한 URL로 이동합니다. 이제 기록할 이벤트를 수행하세요.
6. 로그인을 수행한 다음 이벤트 클립보드에서 **정지** 버튼을 클릭하여 기록을 완료합니다.
7. **저장** 버튼을 클릭해서 파일을 저장하세요.


#### 이벤트 클립보드로 분석하기  

위에서 기록한 **로그인 기록 파일**을 사용하여 분석을 수행해보겠습니다.

1. **프로젝트 수정** 슬라이드에서 **웹 페이지 설정** 버튼을 클릭하세요.
2. **로그인 기록 파일** 옵션에서 **파일 찾아보기** 버튼을 클릭하세요.
3. 저장한 이벤트 클립보드 파일을 선택하세요.
4. **웹 페이지 설정**에서 **설정하기** 버튼을 클릭하세요.
5. **프로젝트 수정**에서 **수정하기** 버튼을 클릭하세요.

> **Tip**: 이벤트 클립보드에서 로그인 동작을 기록하는 경우 리디렉션된 페이지부터 기록을 시작해야 합니다. 또한 로그인 후에 로그아웃 버튼을 클릭하는 것을 방지하기 위해 로그아웃 버튼을 분석 옵션에 있는 **이벤트 수행 제외 요소**에 추가하세요.



## Run Analysis {switcher-key="English"}

Now go to the project you created earlier and perform an analysis. To analyse a **repository, zipped file** or **URL**, you must first set up a project, see [Setting up analysis](analysisSetting.md) for more information.

<img src="runAnalysis.png" />

1. Click the **Start analysis** button.
2. Select **Repository** or **Zip file** to start analysing **code and open source**.
3. Or select **URL** to start analysing **Web Vulnerabilities**.
4. The analysis will now start.

> **Tip**: You cannot perform another analyses with the same type of target while an analysis is running. If you want to stop a running analysis, you can do so from the list of analyses.


### Analysing repository

Files uploaded to the Github repositories can be analysed for the users who registered their github emails in the Sparrow Cloud. See [Setting up source code repository](analysisSetting.md#setting-up-source-code-repository) for details. Users who do not subscribe the Sparrow Cloud service can run analysis on public repositories only.

### Analysing zipped file 

You can analyse compressed files up to 100 MB. Users without a subscription to the service can analyse compressed files of 10 MB or less.



### Analysing URL 

See [Setting up web page](analysisSetting.md#setting-up-web-page) for specifying a web page URL to run analysis. Users who do not subscribe the Sparrow Cloud service cannot modify some items of web app analysis options.

> **Warning**: For web-sites that require additional authentication beyond password log-in, analysis cannot be properly completed.


#### Event Clipboard 

The **Event Clipboard** is basically a tool that allows you to record and save events performed on a web page. You can use this feature to expand the scope of your analysis by saving the events performed by the user to a file and entering it into the [Analysis option](Analysis-Option.md). If the URL you are analysing requires you to log in with a specific ID and password, you can save the event from the **Event Clipboard** to a file and upload it to the **Login History File** in **Analysis Options**, and the information stored in the file will be used for analysis.


#### Installing the Event Clipboard 

The Event Clipboard is available as an extension to the Google Chrome web browser. Therefore, to use the Event Clipboard, you must first **install the Chrome browser** and **download the Event Clipboard from the Chrome Web Store**.

[Download Event Clipboard](https://chromewebstore.google.com/detail/sparrow-dast-event-clipbo/ikebmfjkmpkaacjablfdfdkonamgijdg?hl=en-US&utm_source=ext_sidebar)


#### Launch and run the Event Clipboard 

Now that you've installed the Event Clipboard, let's run it.

1. launch the Chrome web browser.
2. Click the Sparrow DAST Event Clipboard icon on the right side of the address bar.
3. The Event Clipboard window will be displayed.
4. In the Event Clipboard window, click "**Please enter your start URL here**" and enter your start URL.
5. Click the **Record** button and you will be taken to the URL you entered. Now perform the event you want to record.
6. Log in and then click the **Stop** button in the event clipboard to complete the recording.
7. Click the **Save** button to save the file.


#### Analysing with the Event Clipboard 

Let's use the **Login History File** we recorded above to perform an analysis.

1. Click **Modify project** button and click the **Set web page** button.
2. Click **Search File** button in **Login History File** option.
3. Select the saved event clipboard file.
4. Click **Set** button in the Web page settings.
5. Click **Modify** button under **Modify Project**.

> **Tip**: When recording login id and password on the event clipboard, make sure to start recording from the redirected page. Also, to prevent clicking the logout button after login, add the logout button to the **Element to Unload** in the web page options.
 
