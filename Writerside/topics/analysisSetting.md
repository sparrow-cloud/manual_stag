# 분석 설정하기

GitHub 저장소나 URL을 분석하려면 **프로젝트**에서 분석 대상인 **소스코드 저장소** 또는 **분석 대상 웹 페이지**를 설정해야 합니다. **소스코드 저장소**는 GitHub 계정으로 생성한 리포지토리를 조회하고 그 중에서 프로젝트에 설정해둔 특정 리포지토리를 가리킵니다. 분석을 수행하면 해당 리포지토리에 포함된 모든 파일을 분석하게 됩니다. **분석 대상 웹 페이지**는 인터넷을 통해 접근할 수 있는 URL 형식의 웹 페이지로써 사용자가 설정합니다. 분석을 수행하면 1) 해당 URL에서 이동할 수 있는 하위 페이지 및 2) 분석 옵션으로 설정한 페이지를 분석할 수 있습니다.


1. **Sparrow Cloud**에 로그인한 다음, 분석하려는 프로젝트를 클릭하세요.
2. **프로젝트 수정하기** 버튼을 클릭하세요.

## 소스코드 저장소 설정하기

<img src="modifyProj01.png" alt="Alt text" width="450"/>

3. GitHub 인증을 하지 않은 경우 **소스코드 저장소**에서 **GitHub 인증** 버튼을 클릭하고 GitHub에 로그인하세요.
4. GitHub으로 계정을 등록했거나 이미 인증을 마쳤다면 **GitHub 저장소 선택** 버튼을 클릭하세요.
5. 슬라이드에서 분석할 저장소를 선택하세요.
6. 프로젝트 정보 슬라이드에서 **수정하기** 버튼을 클릭하세요.


이제 **소스코드 저장소**를 설정했습니다. 여기에서 선택한 저장소에 저장된 파일을 **소스코드** 및 **오픈소스** 분석에서 사용하게 됩니다.

## 분석 대상 웹 페이지 설정하기

<img src="modifyProj03.png" alt="Alt text" width="450"/>

7. **프로젝트 수정** 슬라이드에서 **웹 페이지 설정** 버튼을 클릭하세요.
8. **URL**에 분석 대상인 웹 페이지의 주소를 입력하고 **연결 테스트** 버튼을 클릭하여 연결을 확인하세요.
> **Tip**: URL은 `http://`로 시작하는 URL 형식으로 입력해야 합니다.
9. 필요한 경우 **분석 옵션**을 조정하고 **설정하기** 버튼을 클릭하세요. 
> **Tip**: 사용자는 웹 취약점 분석 옵션을 조정해서 웹 페이지를 어떤 범위로 어느 정도나 분석할지 결정할 수 있습니다. **분석 옵션**에 대한 자세한 설명은 [여기](http://localhost:63342/newCloud/preview/empty-md-topic.html#-k39vs6_6035)를 참고하세요.
10. [키 파일 저장하기](#analysissetting.html#hpery9_1989)를 참고하여 **키 파일**을 다운로드해서 분석 대상 웹 페이지에 저장하세요.
11. 프로젝트 정보 슬라이드에서 **수정하기** 버튼을 클릭하세요.



### 키 파일 저장하기

**키 파일**은 Sparrow Cloud에서 사용자가 프로젝트에 설정한 웹 페이지 URL을 타겟으로 삼아서 생성한 파일입니다. 사용자가 설정한 웹 페이지를 소유했는지를 확인하기 위해서 사용자에게 **키 파일**을 저장하도록 만듭니다. 만약에 사용자가 실수로 아무런 관계 없는 웹 페이지를 분석하도록 설정했더라도 키 파일이 없다면 분석이 시작되지 않게 됩니다.
키 파일을 저장하는 방법은 다음과 같습니다.

<img src="modifyProj04.png" alt="Alt text" width="450"/>

1. 먼저 프로젝트에서 **분석 대상 웹 페이지**를 설정해야 합니다. 위에서 [분석 대상 웹 페이지 설정하기](#analysissetting.html#hpery9_2779)를 참고하세요.
2. **프로젝트 수정하기** 슬라이드의 대상 URL에서 **키 파일 다운로드** 버튼을 클릭하세요.
3. CMD 창이나 파일 탐색기에서 웹 페이지를 실행하는 서버의 **루트 디렉토리**로 이동하세요.
4. 다운로드한 **키 파일**을 저장하세요.

> **Tip**: **루트 디렉토리**는 일반적으로 분석하려는 프로그램이 저장되어 있는 최상위 폴더인 경우가 많습니다.
