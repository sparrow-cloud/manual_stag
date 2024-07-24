---
switcher-label: Language
---

# Analyzing Options

## 분석 옵션 {switcher-key="한국어"}

Sparrow Cloud는 특히 웹취약점 분석에 대한 다양한 옵션을 준비했습니다. 분석을 수행하기 전에 다음과 같이 옵션을 설정할 수 있습니다.


### 웹취약점 분석 옵션 


**상세 수행 로그**

상세 수행 로그는 **URL을 수집할 때 실행한 브라우저의 동작이나, HTTP 클라이언트의 동작 등을 로그에 상세하게 저장**하는지를 의미하며 `예`, `아니요`로 구분합니다.(기본값: `아니요`)

이 옵션을 `예`로 설정하면 수집할 때 실행한 동작을 로그로 확인할 수 있으므로 **URL을 정상적으로 수집했는지 확인**할 수 있지만 로그 용량이 커집니다. 이 옵션을 `아니요`로 설정하면 로그 용량은 작아지지만 URL을 정상적으로 수집했는지 확인하기가 어렵습니다.


**모바일 화면**

모바일 화면은 분석 대상인 웹 애플리케이션이 모바일 화면을 지원하는 경우 **분석에서 사용하는 내부 브라우저를 모바일 화면 형태로 설정**하는지를 의미하며 `예`, `아니요`로 구분합니다. 이 옵션을 통해 PC와 모바일에서 표시되는 형태가 다른 웹 페이지도 분석할 수 있습니다.(기본값: `아니요`)

이 옵션을 `예`로 설정하면 URL을 분석할 때 사용되는 **브라우저를 모바일 화면으로 변경**합니다. 이 옵션을 `아니요`로 설정하면 **브라우저를 기본 PC 화면 형태로 사용**합니다.


**페이지 부분 로딩**

페이지 부분 로딩은 **내부 브라우저가 페이지의 리소스를 완전히 로딩하지 않아도 수집을 진행**하는지를 의미하며 `예`, `아니요`로 구분합니다. 리소스를 불러올 수 없거나 불러오는데 시간이 걸리는 페이지의 경우 완전히 로딩되기를 기다리면 시간이 오래 걸리거나 타임아웃이 발생하여 수집을 진행하지 못할 수 있습니다.(기본값: `아니요`)

이 옵션을 `예`로 설정하면 **리소스가 로딩되기를 기다리지 않고 수집을 진행**하여 수집 속도가 빨라집니다. 이로 인해 리소스가 반드시 필요한 페이지의 경우 정상적으로 수집하지 못할 가능성이 있습니다. 이 옵션을 `아니요`로 설정하면 **페이지의 리소스가 모두 로딩되어야 수집을 진행**합니다. 이로 인해 리소스가 반드시 필요한 페이지도 정상적으로 수집할 수 있지만 리소스를 로딩하는데 문제가 있는 페이지에서 속도가 느려지게 됩니다.

**일반 본문 분석**

일반 본문 분석은 **URL 수집 중에 받은 응답 메시지의 본문이 HTML이 아닌 일반 본문에서 URL을 수집**하는지를 의미하며 `예`, `아니요`로 구분합니다.(기본값: `예`)

이 옵션을 `예`로 설정하면 **일반 본문에서 URL 패턴을 사용하여 URL을 수집**합니다. 이로 인해 더 많은 URL을 수집하게 되지만 HTML뿐만 아니라 모든 본문을 분석하기 때문에 분석 속도가 느려지고 의미없는 URL을 수집할 가능성이 높습니다.


**서브 도메인 수집**

서브 도메인 수집은 **프로젝트에 입력한 분석 대상 URL의 서브 도메인에 해당하는 URL을 수집하는지**를 의미하며 `예`, `아니요`로 구분합니다. **서브 도메인이란, 특정 컨텐츠를 보조하기 위해 자동으로 연결되는 도메인의 확장자**이며 `(서브).(메인 도메인)`의 형식으로 표시됩니다. 예를 들어, 프로젝트에 입력한 URL이 `https://google.com`이면 `google.com`이 메인 도메인이고 `translate.google.com`, `mail.google.com`, `drive.google.com` 등이 서브 도메인입니다.(기본값: `예`)

이 옵션을 `예`로 설정하면 **분석 대상 URL의 서브 도메인에 해당하는 URL도 수집**하게 됩니다. 이 옵션을 `아니요`로 설정하면 **분석 대상 URL의 서브 도메인에 해당하는 URL을 수집하지 않게** 됩니다.


**상위 경로 수집**

상위 경로 수집은 분석 대상 URL의 상위 경로에 해당하는 URL이 있는 경우 **프로젝트에 입력한 분석 대상 URL의 상위 경로를 수집**하는지를 의미하며 `예`, `아니요`로 구분합니다. 예를 들어, URL이 `http://dast.com/1/2/3` 이면 상위 경로는 `http://dast.com/1/2`, `http://dast.com/1`, `http://dast.com`입니다.(기본값: `아니요`)

이 옵션을 `예`로 설정하면 **분석 대상 URL의 상위 경로도 분석**하게 됩니다. 단, 상위 경로가 분석할 필요가 없는 사이트이거나 상위 경로에 접근하면 자동으로 다른 URL로 이동하게 된다면 의미 없는 URL을 분석할 가능성이 있습니다. 이 옵션을 `아니요`로 설정하면 **프로젝트의 분석 대상 URL에 포함된 하위 경로만을 분석**하게 됩니다.


**HTML 주석 분석**

HTML 주석 분석은 **URL을 수집할 때 HTML 본문의 응답 메시지를 수신하는 경우 주석에 있는 URL을 수집**하는지를 의미하며 `예`, `아니요`로 구분합니다.(기본값: `아니요`)

이 옵션을 `예`로 설정하면 **HTML 주석에 포함된 URL을 찾아 해당 URL을 수집**하게 됩니다. 이로 인해 더 많은 URL을 수집하게 되지만 주석을 분석하기 때문에 분석 속도가 느려지고 의미 없는 URL을 수집할 가능성이 높습니다.


**저장 기반 취약점 검출**

저장 기반 취약점 검출은 **저장 기반 취약점을 검출하기 위한 동작을 추가적으로 수행**하는지를 의미하며 `예`, `아니요`로 구분합니다. 저장 기반 취약점이란 Stored XSS(Persistent XSS)나 Stored SQL Injection(Persistent SQL Injection) 처럼 DB에 저장되어서, 공격 후 페이지에 바로 반영되지 않고 다른 페이지에 영향을 주는 취약점을 의미합니다.(기본값: `아니요`)

이 옵션을 `예`로 설정하면 **저장 기반 취약점을 검출하기 위해 추가적인 작업을 수행하고, 저장 기반 취약점을 검출하기 위한 체커를 활성화**합니다. 이로 인해 분석 속도가 느려지지만 저장 기반 취약점을 검출할 수 있습니다. 이 옵션을 `아니요`로 설정하면 **저장 기반 취약점을 검출하기 위한 작업을 수행하지 않고, 저장 기반 취약점을 검출하기 위한 체커를 비활성화**합니다. 이로 인해 분석 속도는 빨라지지만 저장 기반 취약점을 검출할 수 없습니다.


**URL 수집 깊이**

URL 수집 깊이는 **수집할 URL이 시작 URL에서부터 얼마나 멀리 떨어져 있는지**를 의미하며 `상`, `중`, `하`로 구분합니다. URL이 멀수록 시작 URL에서 특정 URL에 도달하기 위해 페이지 이동 등 수행해야 하는 최소한의 동작이 많아집니다.(기본값: `중`)

이 옵션을 `상`으로 설정하면 **시작 URL에서부터 멀리 있는 URL까지도 수집**하게 되지만 **수집하는 시간이 오래** 걸립니다. 이 옵션을 `하`로 설정하면 프로젝트에서 **URL을 수집하는 시간은 짧아**지지만 멀리 있는 URL은 수집하지 않게 됩니다.


**DOM 수집 깊이**

DOM 수집 깊이는 **수집할 DOM이 동일한 URL에서 생성된 첫 번째 DOM으로부터 얼마나 멀리 떨어져 있는지**를 의미하며 `상`, `중`, `하`로 구분합니다. DOM이 멀수록 첫 번째 DOM에서 동일한 URL의 특정 DOM에 도달하기 위해 수행해야 하는 최소한의 동작이 많아집니다.(기본값: `중`)

이 옵션을 `상`으로 설정하면 URL로 이동할 때 생성되는 **첫 DOM에서부터 멀리 있는 DOM까지도 수집**하게 되지만 **수집하는 시간이 오래** 걸립니다. 이 옵션을 `하`로 설정하면 프로젝트에서 **DOM을 수집하는 시간은 짧아**지지만 멀리 있는 DOM은 수집하지 않게 됩니다.


**페이지 이벤트 수행 정도**

페이지 이벤트 수행 정도는 **수집할 페이지에 있는 이벤트를 얼마나 많이 실행하는지**를 의미하며 `상`, `중`, `하`로 구분합니다. 이벤트란 분석 대상인 웹 애플리케이션의 각 페이지에 포함되어 있는 동작으로써 마우스를 클릭하거나 키를 입력하거나 특정 요소에 마우스를 가져가면 발생하는 사건을 가리킵니다.(기본값: `중`)

이 옵션을 `상`으로 설정하면 **페이지에서 더 많은 이벤트를 수행**하게 되지만 **수집하는 시간이 오래** 걸립니다. 이 옵션을 `하`로 설정하면 **수집하는 시간은 짧아**지지만 페이지에서 더 적은 이벤트를 수행하게 됩니다.


**리소스 로딩 대기 시간**

리소스 로딩 대기 시간은 **페이지 부분 로딩 옵션이 '예'로 설정된 경우 불러오는데 오랜 시간이 필요한 리소스를 기다리는 최대 시간**을 가리킵니다. `1` 이상 `600000` 이하의 숫자를 입력할 수 있으며 값을 입력하지 않은 경우 기본값은 `10000`입니다.(단위: 밀리초, 기본값: `10000`)

이 옵션에 입력된 **값이 적을수록 로딩되기를 기다리지 않고 수집하기 시작하는 리소스가 많아**집니다. 따라서 반드시 리소스가 필요한 페이지를 정상적으로 수집하지 못할 가능성이 있습니다. 이 옵션에 입력된 **값이 클수록 리소스 로딩을 기다리는 시간이 길어**지기 때문에 수집하는 시간이 오래 걸립니다.


**이벤트 대기 시간**

이벤트 대기 시간은 **이벤트를 수행할 때마다 이벤트 수행 결과가 DOM에 반영되기를 기다리는 시간**을 가리킵니다. `0` 이상 `5000` 이하의 숫자를 입력할 수 있으며 옵션을 입력하지 않은 경우 기본값은 `300`입니다.(단위: 밀리초, 기본값: `300`)

이 옵션에 입력된 값이 클수록 **수행한 이벤트를 DOM에 반영하는데 시간이 걸리는 웹 애플리케이션의 URL을 수집**할 수 있지만 수집하는 속도가 느려집니다. 이 옵션에 입력된 값이 적을수록 URL을 수집하는 속도는 향상되지만 **DOM이 변경될 때 시간이 필요한 웹 애플리케이션의 URL을 수집하지 않게** 됩니다.


**HTTP 요청 횟수**

HTTP 요청 횟수는 **URL을 수집할 때 1초에 전송할 수 있는 HTTP 요청의 개수**를 가리킵니다. `-1` 이상 `10000` 이하의 숫자를 입력할 수 있으며 옵션을 입력하지 않는 경우 기본값은 `-1`이며 이 경우에 전송할 수 있는 HTTP 요청의 개수를 제한하지 않게 됩니다.(단위: 개, 기본값: `-1`)

이 옵션에 입력된 **값이 클수록 1초에 전송할 수 있는 HTTP 요청의 개수가 늘어나서 URL을 수집하는 속도가 빨라**지지만 트래픽량이 늘어나 **분석 대상 웹 애플리케이션 서버에 부하도 늘어**날 수 있습니다. 이 옵션에 입력된 값이 **적을수록 트래픽량이 낮아져 분석 대상 웹 애플리케이션 서버의 부하도 줄어**들지만 URL을 수집하는 속도가 늦어집니다.


**HTTP 클라이언트 대기 시간**

HTTP 클라이언트 대기 시간은 **HTTP 클라이언트가 분석을 수행하기 위해** 웹 서버에 연결하고, HTTP 요청을 보내고, HTTP 응답을 받는 과정에서 지연이 발생했을 때 **기다리는 최대 시간**을 가리킵니다. `0` 이상 `30000` 이하의 숫자를 입력할 수 있으며 옵션을 입력하지 않은 경우 기본값은 `3000` 입니다.(단위: 밀리초, 기본값: `3000`)

이 옵션에 입력된 **값이 클수록 웹 서버와의 네트워크 연결 상태가 좋지 않아 지연이 발생한 경우에도 분석이 정상적으로 진행**됩니다. 단, 웹 서버와의 연결 끊김이 지속적으로 발생하면 분석 시간이 늘어날 가능성이 높습니다. 이 옵션에 입력된 **값이 적을수록 분석 속도는 빨라지지만 웹 서버와의 네트워크 연결 상태가 좋지 않아서 지연이 발생한 경우 URL을 분석하지 못할 가능성**이 있습니다.


### 웹 페이지 설정 옵션 

**로그인 기록 파일**

로그인 기록 파일은 **Sparrow DAST 이벤트 클립보드에서 저장한 .ecl 형식의 파일**로써 **특정 URL에서 사용자의 동작이 기록**되어 있습니다. 주로 사용자가 특정 URL에서 로그인하는 데 사용한 ID 및 비밀번호 정보를 저장하여 URL을 수집하거나 분석할 때 사용합니다.

**로그인 기록 파일을 첨부하는 경우** URL 수집 및 분석 중에 이벤트 클립보드의 기록이 시작된 URL에 도달하면 해당 파일에 저장된 사용자의 동작을 그대로 재현하게 됩니다. 이러한 방법으로 **로그인 페이지에서 필요한 인증을 통과**할 수 있습니다. 이벤트 클립보드에 대한 자세한 내용은 [이벤트 클립보드로 분석](#analyze.md#co6xdo_66)을 참고하세요.


**클라이언트 언어**

분석 대상인 웹 애플리케이션이 표시되는 브라우저에서 어떤 언어를 설정했고, HTTP 클라이언트가 어떤 언어를 이해할 수 있는지 설정합니다. **언어_지역**으로 표시되는 로케일 형식으로 입력할 수 있습니다.(기본값: `ko_KR`)


**제외할 수집 URL**

제외할 수집 URL은 URL에 특정 단어가 포함된 경우 해당 URL을 수집하지 않고 건너뛰는 문자열 목록을 가리킵니다. 하나 이상의 문자열을 입력하고 엔터 또는 쉼표(,)로 구분할 수 있습니다.

이 옵션에 입력한 목록에 해당하는 단어가 하나라도 수집하려는 URL에 포함되었다면 해당 URL을 수집하지 않게 됩니다. 단, URL을 수집하기 직전에 건너뛰기 때문에 브라우저가 해당 URL에 방문할 수 있습니다.


**제외할 분석 URL**

제외할 분석 URL은 URL에 특정 단어가 포함된 경우 해당 URL을 분석하지 않고 건너뛰는 문자열 목록을 가리킵니다. 하나 이상의 URL을 입력하고 엔터 또는 쉼표(,)로 구분할 수 있습니다.

이 옵션에 입력한 목록에 해당하는 단어가 하나라도 분석하려는 URL에 포함되었다면 해당 URL을 분석하지 않게 됩니다.

> **Tip:** URL로 표시되는 페이지 전체가 아니라 페이지의 동작을 분석에서 제외하려는 경우 아래에 있는 **이벤트 수행 제외 요소** 옵션을 사용하세요.


**제외할 URL 접미사**

제외할 URL 접미사는 **URL의 끝에 특정 단어나 확장자가 포함된 경우 해당 URL을 수집하지 않고 건너뛰는 접미사 목록**을 가리킵니다. 마침표(.)로 시작하는 확장자 형식으로 입력하고 엔터 또는 쉼표(,)로 구분할 수 있습니다.(기본값: `.js, .css, .xml, .jpg, .jpeg, .gif, .bmp, .png, .ico, .wma, .wav, .mp3, .wmv, .avi, .mp4, .mov, .exe, .zip, .tar, .tar.gz, .7z, .doc, .xls, .ppt, .docx, .xlsx, .pptx, .pdf, .txt, .csv, .jar, .eot, .woff2, .woff, .ttf, .otf, .apk, .hwp`)

이 옵션에 입력한 **목록에 해당하는 단어가 하나라도 수집하려는 URL의 끝에 포함되었다면 해당 URL을 수집하지 않게** 됩니다. URL로 이동하기 전에 HTML 요소의 속성 값 등을 보고 건너뛰기 때문에 해당 URL에 방문하지 않으므로 파일 다운로드 등을 수행하기 전에 건너뛸 수 있습니다.


**추가 수집 범위**

프로젝트를 추가하거나 설정할 때 입력한 URL 이외에 수집하려는 URL이 있는 경우 여기에 입력한 URL을 추가로 수집할 수 있습니다. 단, **추가 수집 범위**는 프로젝트에 설정한 URL이나 수집 범위 안에 있는 URL에서 도달할 수 있어야 합니다. 하나 이상의 값을 문자열로 입력하고 엔터 또는 쉼표(,)로 구분할 수 있습니다.

추가 수집 범위는 **분석 대상 URL로부터 도달할 수는 있지만 기본 수집 범위에 해당하지 않는 URL**을 가리킵니다. 여기서 분석의 기본 수집 범위는 프로젝트에 입력한 분석 대상 URL로부터 도달할 수 있으며 http와 같은 스키마가 같고 도메인명 또는 IP와 포트가 같은 URL을 의미합니다. 예를 들어, 분석 대상 URL이 `http://sparrow.com/main`이면 수집할 때 `https://google.com`이라는 URL을 발견하더라도 스키마나 도메인명이 다르기 때문에 수집하지 않는 것이 원칙입니다. 하지만 이 옵션에 `google.com`을 입력하면 `https://google.com`을 수집하게 됩니다. 하나 이상의 값을 입력하고 엔터 또는 쉼표(,)로 구분할 수 있습니다.

이 옵션에 입력한 **목록에 해당하는 URL이 하나라도 포함되어 있다면 해당 URL을 수집**하게 됩니다.


**이벤트 수행 제외 요소(CSS 선택자)**

이 옵션에 입력한 목록에 해당하는 CSS 선택자가 하나라도 페이지에 포함되었다면 해당하는 HTML 요소와 하위 HTML 요소의 이벤트를 모두 수행하게 됩니다. 하나 이상의 제외할 CSS 선택자를 입력하고 엔터 또는 쉼표(,)로 구분할 수 있습니다.

이 옵션에 입력한 **목록에 해당하는 CSS 선택자가 하나라도 페이지에 포함되었다면 해당하는 HTML 요소와 하위 HTML 요소의 이벤트를 모두 수행하지 않게** 됩니다. 이러한 방법으로 페이지에서 **로그아웃 버튼을 클릭하지 않도록 설정**할 수 있습니다.


**이벤트 수행 추가 요소(CSS 선택자)**

이 옵션에 입력한 목록에 해당하는 CSS 선택자가 하나라도 페이지에 포함되었다면 해당하는 HTML 요소와 하위 HTML 요소의 이벤트를 모두 수행하게 됩니다. 하나 이상의 추가할 CSS 선택자를 입력하고 엔터 또는 쉼표(,)로 구분할 수 있습니다.

이 옵션에 입력한 **목록에 해당하는 CSS 선택자가 하나라도 페이지에 포함되었다면 해당하는 HTML 요소와 하위 HTML 요소의 이벤트를 모두 수행**하게 됩니다. 이러한 방법으로 페이지에서 **이벤트에 포함되지 않는 태그와 같은 요소를 수행**할 수 있습니다.


**이벤트 수행 제외 요소(XPath)**

이 옵션에 입력한 목록에 해당하는 XPath가 하나라도 페이지에 포함되었다면 해당하는 HTML 요소와 하위 HTML 요소의 이벤트를 모두 수행하지 않게 됩니다. 이러한 방법으로 페이지에서 로그아웃 버튼을 클릭하지 않도록 설정할 수 있습니다. 하나 이상의 제외할 XPath를 입력하고 엔터 또는 쉼표(,)로 구분할 수 있습니다.

이 옵션에 입력한 **목록에 해당하는 XPath가 하나라도 페이지에 포함되었다면 해당하는 HTML 요소와 하위 HTML 요소의 이벤트를 모두 수행하지 않게** 됩니다. 이러한 방법으로 페이지에서 **로그아웃 버튼을 클릭하지 않도록 설정**할 수 있습니다.


**이벤트 수행 추가 요소(XPath)**

이 옵션에 입력한 목록에 해당하는 XPath가 하나라도 페이지에 포함되었다면 해당하는 HTML 요소와 하위 HTML 요소의 이벤트를 모두 수행하게 됩니다. 하나 이상의 추가할 XPath를 입력하고 엔터 또는 쉼표(,)로 구분할 수 있습니다.

이 옵션에 입력한 **목록에 해당하는 XPath가 하나라도 페이지에 포함되었다면 해당하는 HTML 요소와 그 하위 HTML 요소의 이벤트를 모두 수행**하게 됩니다. 이러한 방법으로 페이지에서 **이벤트에 포함되지 않는 태그와 같은 요소를 수행**할 수 있습니다.


**사용자 정의 HTTP 헤더**

사용자 정의 HTTP 헤더는 URL을 수집할 때 전송할 HTTP 요청에 포함되는 헤더의 이름과 값의 목록을 가리킵니다. 이 옵션에 헤더의 이름과 값을 입력하면 해당 헤더를 모든 HTTP 요청 메시지에 추가하게 됩니다. **추가하기** 버튼을 클릭하여 하나 이상의 헤더를 추가하고 휴지통 아이콘을 클릭하여 삭제할 수 있습니다.

이 옵션에는 **HTTP 요청에 반드시 필요한 헤더를 입력**해야 합니다. 이로 인해 브라우저에 프록시를 설정하므로 수집 속도가 느려질 수 있습니다.

`Cookie` 헤더를 제외하고 **동일한 이름의 헤더를 여러 개 입력한 경우 그 중 하나만 적용**됩니다. 따라서 여러 값을 입력해야 하는 경우 헤더 값을 `;`로 구분하여 입력하세요. 같은 이름의 헤더가 이미 있는 경우 해당 헤더를 지우고 커스텀 헤더가 추가됩니다. 커스텀 헤더를 사용하려면 분석 대상 URL의 호스트가 `localhost` 또는 `127.0.0.1`로 설정되면 안됩니다. 로컬에 있는 웹 애플리케이션을 분석하려는 경우 로컬 IP 주소를 입력해야 합니다.


## Analysis Option {switcher-key="English"}

Sparrow Cloud has prepared various options especially for web app analysis. You can set the options as follows before performing the analysis.


### Web App Analysis Options 



**Detailed Execution Log**

Detailed Execution Log means whether to **store the detailed actions of the Browser, HTTP client, etc. that were executed when collecting the URL in the Log.(Default: `OFF`)

If this Option is set to `ON`, you can check the actions you started when collecting in the Log, so you can **OK if you collected the URL correctly**, but it will increase the size of the Log. If this Option is set to `OFF`, the Log volume will be smaller, but it will be harder to check if the URL was collected normally.


**Mobile Screen**

Mobile Screen means whether to **Set the internal browser used in the analysis to Mobile Screen if the Web application being analyzed supports Mobile Screen**. This option allows you to analyze Web pages that are displayed differently on PC and mobile.(Default: `OFF`)

If this Option is set to `ON`, it will **Change Browser to Mobile Screen** used when analyzing URLs. If this Option is set to `OFF`, **enable the Browser to be the Default PC screen**.


**Partial Page Loading**

Partial Page Loading refers to whether **the internal Browser will proceed with Crawling without fully loading the resources on the page**. For pages whose resources cannot be loaded or take time to load, waiting for them to fully load may take a long time or cause a Timeout, preventing Crawling from proceeding.(Default: `OFF`)

If this Option is set to `ON` then it will speed up Crawling by **proceeding with Crawling without waiting for the resource to load**. This may prevent pages that absolutely need the resource from crawling properly. If this Option is set to `OFF`, it **will wait for All of the page's resources to load before proceeding with Crawling**. This will likely result in normal crawling for pages that absolutely need resources, but will slow down for pages that have problems loading resources.

**Plain Text Analysis**

Plain Text Analysis means **Collecting URLs from the plain text of the response Message received during URL collection**, not from HTML.(Default: `ON`)

If this Option is set to `ON`, it will **Crawling URLs from the General Contents using the URL pattern**. This will result in collecting more URLs, but because it will analyze all the Contents, not just the HTML, it will be slower and more likely to collect meaningless URLs.


**Sub-domain Crawling**

Sub-domain Crawling means **whether it collects URLs that are sub-domains of the Analyzing Target URL entered in the Project**. A subdomain is **an extension of a domain that is Auto linked to support specific content** and is displayed in the Format of `(sub).(main domain)`. For example, if the URL Input in your Project is `https://google.com`, then `google.com` is the main domain and `translate.google.com`, `mail.google.com`, `drive.google.com`, etc. are subdomains.(Default: `ON`)

If this option is set to `ON`, it will **also collect URLs that are sub-domains of the Analyzing Target URL**. If this Option is set to `OFF`, it will **not collect URLs that are subdomains of the Analyzing Target URL**.


**Parent Domain Crawling**

Parent Path Collection means whether to **collect the URLs corresponding to the parent path of the Analyzing Target URL entered in the Project**, if any. For example, if the URL is `http://dast.com/1/2/3`, the parent paths are `http://dast.com/1/2`, `http://dast.com/1`, and `http://dast.com`. (Default: `OFF`)

If this option is set to `ON`, **Analyzing Target URL's parent path will also be analyzed**. However, if the parent path is a site that doesn't need to be analyzed, or if accessing the parent path automatically takes you to another URL, there is a possibility of analyzing a meaningless URL. If this option is set to `OFF`, you will **Only analyze the child paths included in the Analyzing Target URL for the Project**.


**HTML Comment Analysis**

HTML Comment Analysis means whether **When collecting URLs, collect the URLs in the comments if you receive a response Message in the Contents of HTML**. (Default: `OFF`)

If this option is set to `ON`, it will **look for URLs Included in HTML comments and crawl those URLs**. This will result in collecting more URLs, but because it analyzes the comments, the analysis will be slower and more likely to collect meaningless URLs.


**Detect Storage Vulnerability**

Detect Storage Vulnerability refers to whether **additionally performs actions to detect storage-based vulnerabilities**. A storage-based vulnerability is a vulnerability that is stored in the DB, such as Stored XSS (Persistent XSS) or Stored SQL Injection (Persistent SQL Injection), and affects other pages without being reflected on the page immediately after the attack.(Default: `OFF`)

If this option is Setting to `ON`, it will **Start Work extra to Detect Storage Vulnerability and Enable Checker to Detect Storage Vulnerability. This slows down the analysis, but allows for the detection of storage-based vulnerabilities. If this option is set to `OFF`, **Does not perform any additional work to detect storage-based vulnerabilities, and disables the checker to detect storage-based vulnerabilities**. This will speed up the analysis, but will not detect storage-based vulnerabilities.


**URL Crawling Depth**

URL Crawling Depth means **how far away the URL to be crawled is from the Start URL** and is categorized into `High`, `Medium`, and `Low`. The farther the URL is from the Start URL, the more minimal actions you need to perform, such as Going to a page, to reach a specific URL.(Default: `Medium`)

If this option is set to `High`, we will **crawl URLs farther away from the Start URL**, but it will take longer to do so. If this option is set to `Low`, the Project will **crawl URLs in less time**, but will not collect URLs that are farther away.


**DOM Crawling Depth**.

DOM Crawling Depth means **how far away the DOM to be harvested is from the first DOM generated from the same URL**. The farther the DOM is, the more minimal actions the first DOM needs to perform to reach a specific DOM from the same URL.(Default: `Medium`)

If this option is set to `High`, it will **crawl DOMs from the first DOM to the farthest DOM** that are created when navigating to a URL, but it will take **more h** to do so. If this option is set to `Low`, the Project will **crawl DOMs in less time**, but will not collect the farther DOMs.


**Level of Conducted Events**

The Level of Conducted Events on a Page refers to **how many events on the page to be collected**. An Event is an action included on each page of the Web application being analyzed, which is an event that occurs when you click the mouse, input a key, or hover over a specific element.(Default: `Medium`)

If this option is set to `High`, you will **have more events on the page**, but they will take **more time crawling**. If this option is set to `Low`, **it will take less time to crawl**, but the page will perform fewer events.


**Resource Loading Timeout**

Resource Loading Timeout refers to the maximum time **waiting for resources that require a long time to load when the Partial Page Loading Option is set to ON**. You can Input a number of `1` and more than or less than `600000`, and if no Value is Input, the Default is `10000`.(Unit: Milliseconds, Default: `10000`)

The lower the **Value** entered for this Option, the more resources it will Start Crawling without waiting for them to load, so there is a possibility that pages that absolutely need resources may not be able to be crawled properly. The higher the **Value** input for this Option, the longer we wait for resources to load**, and therefore the longer it takes to Crawl.


**Event Timeout**

Event Timeout refers to the amount of time **waiting for the results of performing an event to be reflected in the DOM each time the event is performed**. You can Input a number more than `0` and less than `5000`, and if no Option is Input, the Default is `300`.(Unit: Milliseconds, Default: `300`)

The larger the value entered for this Option, the slower it will be to **Crawled URLs of Web applications that take hrs to reflect the events they have performed in the DOM**. The lower the Value Input for this Option, the faster it will collect the URLs, but it will **not collect URLs for Web applications that require time when the DOM changes**.


**Number of HTTP Requests per Sec**

Number of Requests refers to **the number of HTTP Requests per Sec that can be sent when collecting URLs**. You can Input a number that is more than `-1` and less than `10000`, and if no Option is entered, the Default is `-1`, in which case you will not limit the number of HTTP Requests that can be sent.(Unit: item(s), Default: `-1`)

A **higher** value entered for this Option will increase the number of HTTP Request(s) that can be sent in a second, which will make Analyzing Target URLs faster**, but may also increase the amount of traffic, which will **increase the load on the Analyzing Target Web Application server**. The **lower the value entered for this option, the lower the traffic volume, which will reduce the load on the Analyzing Target Web application server**, but will slow down the speed of collecting the URL.


**HTTP Client Timeout**

HTTP Client Timeout refers to the maximum amount of time **the HTTP client waits** when it encounters a delay in connecting to the Web server, sending an HTTP Request, and receiving an HTTP response **to perform analysis**. You can Input a number that is more than `0` and less than `30000`, and if no Option is Input, the Default is `3000`.(Unit: Milliseconds, Default: `3000`)

The higher the **Value entered for this option, the more the analysis will proceed normally** even if there is a delay due to poor network connection status with the Web server. However, if the connection with the Web server is continuously disconnected, the Analyzing Time is likely to increase. The lower the **Value entered in this Option, the faster the analysis speed, but there is a possibility that the URL may not be analyzed** if the delay is caused by poor network connection status with the Web server.



### Web page setting options


**Sign-in Log File**

A Sign-in Log File is a **file in .ecl format saved from the Sparrow DAST Event Clipboard** that records a User's behavior at a specific URL. It is mainly used when collecting or analyzing URLs by storing the ID and Password information that a user used to log-in at a specific URL.

If you attach a **Sign-in Log File** during URL collection and analysis, when the Event Clipboard reaches the URL where the recording started, it will replay the User's behavior stored in the file. In this way, you can **pass the required authentication on the Logged-in page**. For more information about the Event Clipboard, see [Analyzing with the Event Clipboard](#analyze.md#co6xdo_66).


**Browser or HTTP Client Language**

Sets what language is set in the Browser where the Web application being analyzed is displayed and what language the HTTP client can understand. Input in the locale format represented by **Language_Region** (Default: `en_US`)


**Crawling URL to Unload**

Crawling URL to Unload refers to a list of strings that will be skipped if the URL contains certain words. You can enter one or more strings and separate them with an Enter or comma (,).

If any of the words in the list you entered in this option are included in the URL you want to harvest, you will not harvest that URL. However, it will skip right before collecting the URL, so the Browser can still visit it.


**Analyzing URL to Unload**

Excluded Analysis URLs is a list of strings that will skip the URL without analyzing it if it contains certain words. You can enter one or more URLs and separate them with an Enter or comma (,).

If any of the words in the list you entered for this option are included in the URL you want to analyze, the URL will not be analyzed.

> **Tip:** If you want to exclude the behavior of a page from analysis, rather than all pages represented by URLs, enable the **Event Performance Excluded Elements** option below.


**URL Suffix to Unload**

Unloaded URL Suffix is a **List of suffixes that will skip the URL without collecting it if it contains certain words or extensions at the end of the URL**. Input them in the format of extensions starting with a period (.) and separated by an Enter or comma (,) (Default: `.js, .css, .xml, .jpg, .jpeg, .gif, .bmp, .png, .ico, .wma, .wav, .mp3, .wmv, .avi, .mp4, .mov, .exe, .zip, .tar, . tar.gz, .7z, .doc, .xls, .ppt, .docx, .xlsx, .pptx, .pdf, .txt, .csv, .jar, .eot, .woff2, .woff, .ttf, .otf, .apk, .hwp`)

If any of the words in the **List** Input in this Option are included at the end of the URL you want to crawl, it will not crawl that URL. It will look at the Value of the HTML element's attributes, etc. before going to the URL and skip it, so you can skip it before downloading the File, etc.


**Additional Crawling URL**

If there are URLs you want to collect in addition to the URLs you entered when Adding Project or Setting, you can collect additional URLs here. However, the **Additional Crawling URLs** must be reachable from the URLs you set in the Project or from URLs within the collection scope. You can enter one or more Values as a string and separate them with an Enter or comma (,).

Additional Crawling Scope refers to **URLs that can be reached from the Analyzing Target URL but are not in the Default Crawling Scope**. Here, the Default Collection Scope of an analysis refers to URLs that are reachable from the Analyzing Target URL entered in the project and have the same schema, such as http, and the same domain name or IP and port. Yes, if your Analyzing Target URL is `http://sparrow.com/main`, then even if you come across a URL called `https://google.com` when collecting, you shouldn't collect it because it has a different schema or domain name. However, if you input `google.com` into this Option, it will crawl `https://google.com`. You can Input more than one Value and separate them with an Enter or a comma (,).

If any of the URLs in the **List** you Input in this Option are Included, you will **Crawling URLs**.


**Element to Unload (CSS Selector)**

If the page contains any CSS selectors that fall into the List you Input in this Option, it will Perform the events of All of its HTML elements and child HTML elements. Input one or more CSS selectors to be Excluded and separate them with an Enter or comma (,).

If any of the CSS selectors in the **List** you Input in this Option are Included on the page, they will **not** perform the events of their corresponding HTML elements and child HTML elements. In this way, you can **Prevent clicking the Logged-out button on a page** by.


**Additional Element (CSS selector)**

If the page contains at least one CSS Selector from the List you Input in this Option, it will Perform All of the events of its HTML elements and child HTML elements. Input one or more CSS selectors to add and separate them with an Enter or comma (,).

If any of the CSS Selectors in the **List** you Input in this Option are included on the page, they will **perform the events of all of their corresponding HTML elements and child HTML elements**. In this way, you can **fire** elements on your page that are not Included in the event, such as Tags.


**Element to Unload (XPath)**

If the page contains any of the XPaths in the List you Input in this Option, it will not perform All of the events for that HTML element and its child HTML elements. In this way, you can prevent users from clicking the Logged-out button on a page. Input one or more XPaths to be Excluded and separate them with an Enter or comma (,).

If any of the XPaths in the **List** you Input in this Option are Included in the page, it will prevent All of the events of that HTML element and its child HTML elements from being fired. In this way, you can **Prevent clicking the Logged-out button on a page** by.


**Additional Element (XPath)**

If the page contains any XPaths from the List you Input in this Option, it will fire All of the events of the corresponding HTML elements and child HTML elements. Input one or more XPaths to add, and separate them with an Enter or comma (,).

If any of the XPaths in the **List** you Input in this Option are included on the page, they will **fire the events of that HTML element and all of its child HTML elements**. In this way, you can **fire elements on the page that are not included in the event, such as Tags**.


**Custom HTTP Header**

Custom HTTP Headers refers to a List of Names and Values of Headers that are included in the HTTP Request to be sent when Crawling URLs. Inputting the Name and Value of a Header in this Option will add that Header to all HTTP Request Messages. You can add one or more headers by clicking the **Add** button, and more by clicking the trash can icon.

This Option requires you to **Input Headers that are required for HTTP Requests**, which may slow down Crawling as it sets up a proxy in the Browser.

Except for the `Cookie` header, **if you enter multiple headers with the same name, only one of them will be applied**. So, if you need to enter multiple values, please enter the header values separated by `;`. If a header with the same name already exists, it will be cleared and the custom header will be added. To enable custom headers, the Host of the Analyzing Target URL must not be set to `localhost` or `127.0.0.1`. If you are analyzing a locally located Web application, you must Input the local IP Address.

