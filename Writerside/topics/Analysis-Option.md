---
switcher-label: Language
---

# Analyzing Options

## 분석 옵션 {switcher-key="한국어"}

Sparrow Cloud는 특히 웹 취약점 분석에 대한 다양한 옵션을 준비했습니다. 분석을 수행하기 전에 다음과 같이 옵션을 설정할 수 있습니다.


## Analysis Option {switcher-key="English"}

Sparrow Cloud has prepared various options especially for web vulnerability analysis. You can set the options as follows before performing the analysis.


### 웹 취약점 분석 옵션 {switcher-key="한국어"}


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

일반 본문 분석은 **URL 수집중에 받은 응답 메시지의 본문이 HTML이 아닌 일반 본문에서 URL을 수집**하는지를 의미하며 `예`, `아니요`로 구분합니다.(기본값: `예`)

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


### Web Vulnerability Analysis Options {switcher-key="English"}


**Detailed Performance Logs

This option indicates whether to log detailed browser behaviour, HTTP client behaviour, etc. when collecting URLs (default: `Yes`, `No`).

Setting this option to `ON' allows you to log the actions taken during ingestion, so you can verify that you ingested the URL correctly, but it increases the size of the log. Setting this option to `No` will result in smaller logs, but will make it harder to verify that the URL was collected correctly.


**Mobile screens

Mobile screen means whether the internal browser used in the analysis is set to mobile screen if the web application being analysed supports mobile screen, which is either `ON' or `OFF'. This option allows you to analyse web pages that display differently on PC and mobile (default: `No`).

Setting this option to `ON' will **change the browser used when analysing URLs to the mobile screen**. Setting this option to `No` will **use the browser as the default PC screen** when analysing URLs.


**Partial page loading

Partial page loading refers to whether **the internal browser proceeds with collection without fully loading the page's resources**, which is either `ON' or `OFF'. For pages whose resources cannot be loaded or take a while to load, waiting for them to fully load may take a long time or cause a timeout and prevent collection from proceeding. (Default: `OFF')

Setting this option to `ON' speeds up ingestion by **proceeding with ingestion without waiting for the resource to load**. This may prevent pages that absolutely need the resource from collecting properly. Setting this option to `No` will **proceed with ingestion only after all resources on the page have loaded**. This will allow pages that absolutely need resources to collect normally, but will slow down pages that have problems loading resources.

**Plain text analyses

Analyse plain text means that the body of the response message received during URL collection is collected in plain text rather than HTML. (Default: `Yes`, `No`)

Setting this option to `ON' will **collect URLs using URL patterns from the plain body**. This will result in more URLs being collected, but because it analyses all the body, not just the HTML, it will be slower and more likely to collect meaningless URLs.


**Collecting subdomains

Subdomain collection refers to whether the project collects URLs that are subdomains of the URL to be analysed, which is either yes or no. **A subdomain is an extension of a domain that is automatically linked to to support specific content, and is represented in the form of `(sub).(main domain)'. For example, if the URL you enter in your project is `https://google.com`, then `google.com` is the main domain and `translate.google.com`, `mail.google.com`, `drive.google.com`, etc. are subdomains. (Default: `Yes`)

Setting this option to `ON' will **collect URLs that are subdomains of the URL being analysed**. Setting this option to `No` will **not collect URLs that are subdomains of the URL being analysed**.


**Collect parent paths

Collect parent paths means whether to **collect the parent path of the analysed URL entered in the project** if it exists. For example, if the URL is `http://dast.com/1/2/3`, the parent paths are `http://dast.com/1/2`, `http://dast.com/1`, and `http://dast.com` (default: `No`).

Setting this option to `ON' will **also analyse the parent path of the URL being analysed**. However, if the parent path is a site that does not need to be analysed, or if accessing the parent path will automatically take you to another URL, there is a possibility of analysing meaningless URLs. Setting this option to `No` will only analyse the child paths contained in the URLs to be analysed in the project.


**Analyse HTML comments

Analyse HTML comments means whether to **collect URLs in comments when receiving response messages in the body of HTML when collecting URLs** (default: `Yes`, `No`).

Setting this option to `ON' will **look for URLs contained in HTML comments and collect them**. This will result in more URLs being collected, but it will also slow down the analysis due to analysing the comments and is more likely to collect meaningless URLs.


**Storage-based vulnerability detection

Storage-based vulnerability detection refers to whether we **take additional steps to detect storage-based vulnerabilities**, which is either yes or no. A storage-based vulnerability is a vulnerability that is stored in the DB, such as Stored XSS (Persistent XSS) or Stored SQL Injection (Persistent SQL Injection), and affects other pages after an attack, rather than being reflected directly on the page. (Default: `No`)

Setting this option to `Yes` will **take extra work to detect storage-based vulnerabilities and enable checkers to detect storage-based vulnerabilities**. This slows down the analysis, but allows for the detection of storage-based vulnerabilities. Setting this option to `No` **does not perform any work to detect storage-based vulnerabilities, and disables the checker for detecting storage-based vulnerabilities. This speeds up analysis, but does not detect storage-based vulnerabilities.


**URL collection depth

URL collection depth refers to **how far away the URLs to be collected are from the starting URL** and is categorised as `high', `medium', or `low'. The further away the URL is from the starting URL, the more minimal actions must be performed to reach the specific URL, such as page navigation. (Default: `Medium`)

Setting this option to `Up` will collect URLs farther away from the starting URL, but it will take longer to collect them. Setting this option to `Low` will cause the project to spend less time collecting URLs, but will not collect URLs that are farther away.


**DOM collection depth

The DOM harvesting depth refers to how far away the DOM to be harvested is from the first DOM generated from the same URL and is categorised as 'high', 'medium' or 'low'. The further away the DOMs are, the more minimal actions the first DOM needs to perform to reach a specific DOM from the same URL. (Default: `Medium`)

Setting this option to `Up` will collect the DOMs that are generated when navigating to a URL, even those that are farther away from the first DOM, but it will take longer to collect them. If this option is set to `Low`, the project will take less time to collect DOMs, but will not collect farther DOMs.


**How much page events are performed

Page event performance refers to how much the events on the page to be collected are fired and is categorised as `High`, `Medium`, or `Low`. An event is an action that is included on each page of the web application being analysed and occurs when a mouse click, keystroke, or hover over a specific element. (Default: `High')

Setting this option to `High' will **fire more events on the page**, but they will take longer to collect. Setting this option to `Low` will result in fewer events on the page, but will take less time to collect.


**Resource loading wait time

Resource loading wait time refers to the maximum time to wait for resources that require a long time to load when the Partial page loading option is set to Yes. You can enter a number greater than or equal to `1` and less than or equal to `600000`; if no value is entered, the default value is `10000`. (Unit: milliseconds; default: `10000`)

The lower the **value entered for this option, the more resources it will start to ingest without waiting for them to load. This can result in pages that absolutely need resources not being ingested properly. The larger the **value** entered for this option, the longer the time spent waiting for resources to load, and therefore the longer it takes to collect them.


**Event wait time

The event wait time refers to the amount of time you wait for the result of performing an event to be reflected in the DOM each time you perform the event. You can enter a number from `0` to `5000`, and the default value is `300` if no option is entered. (Unit: milliseconds; default: `300`)

The larger the value entered for this option, the slower it is to collect the URLs of web applications that **take time to reflect the events they perform in the DOM**. A smaller value entered for this option will collect URLs faster, but will not collect URLs for web applications that require time for the DOM to change.


**HTTP request count

HTTP request count refers to the number of HTTP requests that can be sent in one second when collecting URLs. You can enter a number greater than or equal to `-1` and less than or equal to `10000`, and if no option is entered, the default value is `-1`, in which case you will not limit the number of HTTP requests that can be sent. (Unit: number, default: `-1`)

The **larger value entered for this option increases the number of HTTP requests that can be sent per second, making URL collection faster**, but it can also increase traffic volume, which can **increase the load on the web application server being analysed**. The lower the value entered for this option, the lower the traffic volume, which reduces the load on the analysed web application server, but slows down the collection of URLs.


**HTTP Client Latency

HTTP client latency refers to the maximum amount of time that an HTTP client waits when it encounters delays in connecting to the web server, sending HTTP requests, and receiving HTTP responses in order to perform analytics. You can enter a number greater than or equal to `0` and less than or equal to `30000`, and the default value is `3000` if no option is entered. (Units: milliseconds; default: `3000`)

The higher the **value entered for this option, the faster the analysis will proceed** even if the delay is caused by a poor network connection to the web server. However, if the connection to the web server is constantly disconnected, the analysis time is likely to increase. The lower the value entered for this option, the faster the analysis, but the URL may not be analysed if the delay is caused by a poor network connection to the web server.



## 웹 페이지 설정 옵션  {switcher-key="한국어"}

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


## Web page settings options {switcher-key="English"}

**Login History File

A login history file is an .ecl format file saved from the Sparrow DAST event clipboard that records a user's actions at a specific URL. It is typically used when collecting or analysing URLs by storing the ID and password information that a user used to log in at a specific URL.

**If you attach a login history file** during URL collection and analysis, when you reach the URL where the Event Clipboard's recording started, it will reproduce the user's actions stored in the file. In this way, you can **pass the required authentication on the login page**. For more information about the Event Clipboard, see [Analysing with the Event Clipboard](#analyze.md#co6xdo_66).


**Client language**.

Sets what language is set in the browser where the web application being analysed is displayed, and what language the HTTP client can understand. This can be entered in locale format, represented by **Language_region** (default: `en_GB`)


**Collection URLs to exclude

Gather URLs to exclude refers to a list of strings that are skipped if the URL contains certain words. You can enter one or more strings and separate them with an enter or comma (,).

If any of the words in the list you enter for this option are included in the URL you want to collect, then the URL will not be collected. However, the URL will be skipped just before it is collected, so the browser can still visit it.


**Analytics URLs to exclude

Analyse URLs to exclude is a list of strings that, if they contain certain words, will skip the URL without analysing it. You can enter one or more URLs and separate them with Enter or a comma (,).

If any of the words in the list you enter for this option are included in the URL you want to analyse, the URL will not be analysed.

> **Tip:** If you want to exclude the behaviour of a page, rather than the entire page represented by a URL, from analysis, use the **Event Performance Exclusion Elements** option below.


**URL suffixes to exclude

URL suffixes to exclude is a **list of suffixes to skip without collecting URLs if they contain certain words or extensions at the end of the URL**. You can enter them in the form of extensions starting with a period (.) and separated by an enter or comma (,). (Default: `.js, .css, .xml, .jpg, .jpeg, .gif, .bmp, .png, .ico, .wma, .wav, .mp3, .wmv, .avi, .mp4, .mov, .exe, .zip, .tar, . tar.gz, .7z, .doc, .xls, .ppt, .docx, .xlsx, .pptx, .pdf, .txt, .csv, .jar, .eot, .woff2, .woff, .ttf, .otf, .apk, .hwp`)

If any of the words in the **list** entered in this option are included at the end of the URL you want to collect, you will not collect that URL. It will look at the attribute values of the HTML element, etc. before going to the URL and skip it, so you can skip it before downloading the file, etc.


**Additional collection scope

If there are URLs you want to collect in addition to the URLs you entered when adding or setting up your project, you can enter them here. However, the **Additional collection scope** must be reachable from the URLs you set in the project or from URLs within the collection scope. You can enter one or more values as a string and separate them with an enter or comma (,).

Additional collection scope refers to URLs that are reachable from the URL being analysed but are not in the primary collection scope. Here, the primary collection scope of an analysis means URLs that are reachable from the analytics target URL entered in the project and have the same schema, such as http, and the same domain name or IP and port. For example, if your analytics target URL is `http://sparrow.com/main`, then even if you encounter a URL called `https://google.com` during ingestion, the rule of thumb is not to ingest it because it has a different schema or domain name. However, if you enter `google.com` in this option, you will collect `https://google.com`. You can enter more than one value and separate them with enter or a comma (,).

If the **list** you enter in this option contains any of the URLs in the list, they will be collected.


**Exclude elements from performing the event (CSS selector)

If the page contains any of the CSS selectors in the list you enter in this option, we will fire the events of both the HTML element and its child HTML elements. You can enter one or more CSS selectors to exclude and separate them with an Enter or comma (,).

If the page contains any of the CSS selectors in the **list** entered in this option, the page will not fire all events on the corresponding HTML elements and child HTML elements. This is how you can **disable the logout button from being clicked** on a page.


**Additional elements to fire events (CSS selectors)

If the page contains at least one CSS selector from the list entered in this option, it will fire all of the events of its HTML elements and child HTML elements. You can enter one or more CSS selectors to add and separate them with an Enter or comma (,).

If the page contains any of the CSS selectors in the **list** entered in this option, it will fire the events of both the HTML element and its child HTML elements. In this way, you can **fire** elements on your page that are not included in the event, such as tags.


**Exclude elements from firing events (XPath)

If the page contains any of the XPaths in the list entered in this option, it will not fire all events for that HTML element and its child HTML elements. In this way, you can prevent users from clicking the Logout button on a page. You can enter one or more XPaths to exclude and separate them with an Enter or comma (,).

If the page contains any of the XPaths in the **list** entered in this option, the page will not fire any events on that HTML element and its child HTML elements. In this way, you can **disable the logout button from being clicked** on a page.


**Additional elements to fire events on (XPath)

If the page contains any of the XPaths in the list you enter for this option, it will fire the events of both the HTML element and its child HTML elements. You can enter one or more XPaths to add and separate them with an Enter or comma (,).

If any of the XPaths in the **list** you enter in this option are included on the page, they will fire the events of both the HTML element and its child HTML elements. In this way, you can **fire elements on your page that are not included in the event, such as tags.


**Custom HTTP headers

Custom HTTP headers refers to a list of header names and values that are included in the HTTP request to be sent when collecting the URL. Entering the name and value of a header in this option will add that header to all HTTP request messages. You can add one or more headers by clicking the **Add** button and delete them by clicking the trash can icon.

This option requires you to **Enter headers that are required in HTTP requests**, which may slow down collection as it sets up a proxy in the browser.

With the exception of the `Cookie` header, **if you enter multiple headers with the same name, only one of them will be applied**. So if you need to enter multiple values, separate the header values with `;`. If a header with the same name already exists, it will be removed and a custom header will be added. To use custom headers, the host of the URL to be analysed must not be set to `localhost` or `127.0.0.1`. If you want to analyse a locally located web application, you must enter the local IP address.
