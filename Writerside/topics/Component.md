---
switcher-label: Language
---

# Component

## 식별 유형 {switcher-key="한국어"}

컴포넌트를 식별하기 위해 사용한 대상의 유형을 **바이너리**, **의존성**, **소스코드**, **스니펫**, **SBOM** 중 하나로 표시합니다. 

- **바이너리**: 분석한 대상이 바이너리 파일임을 의미합니다. 
- **의존성**: **pom.xml**처럼 소프트웨어에서 이용한 라이브러리를 정리한 의존성 파일을 분석한 경우입니다. 
- **소스코드**: 소스코드를 분석 대상으로 소스코드의 해시값을 생성하고 비교합니다. 
- **스니펫**: C/C++ 언어 파일 중에서 헤더 파일(.h 또는 .hpp)을 분석 대상 유형으로 표시합니다. 
- **SBOM**: 소프트웨어를 구성하는 컴포넌트를 정리한 SBOM 파일을 분석한 경우를 가리킵니다.


## 라이선스 

라이선스는 소프트웨어를 개발한 주체가 소프트웨어를 사용할 수 있는 권한 또는 사용을 허가한다는 내용을 담은 일종의 계약서입니다. 컴포넌트에서 발견되는 오픈소스는 이런 라이선스를 포함하고 있을 가능성이 높습니다.

라이선스는 사용을 허용하는 동시에 사용할 수 있는 조건을 규정하기도 하기 때문에 분석에서 식별한 라이선스를 확인하는 것이 중요합니다. Sparrow Cloud에서는 오픈소스 라이선스를 이슈로 검출합니다. 검출된 라이선스의 고지 의무 및 제약 사항 등 사용할 때 지켜야 하는 조건을 반드시 추가적으로 확인하세요.


## SBOM

Software Bill Of Materials (SBOM)는 분석한 대상 소프트웨어에서 서비스를 제공하기 위해 활용한 구성 요소에 대한 메타 정보라고 할 수 있습니다. Sparrow Cloud에서는 분석한 컴포넌트를 SBOM 형태의 파일로 내보낼 수 있는 기능을 제공합니다.
자세한 내용은 [SBOM 내보내기](Export-SBOM.md)를 참고하세요.


## identification type {switcher-key="English"}

Displays the type of target used to identify the component: **Binary**, **Dependencies**, **Source Code**, **Snippets**, **SBOM**.

- Binary: means that the target analysed is a binary file.
- Dependency: If a dependency file was analysed, such as **pom.xml**, which lists the libraries used by the software.
- Source code: source code is analysed to generate and compare hash values of the source code.
- Snippets: Marks header files (.h or .hpp) among C/C++ language files as the type to analyse.
- SBOM: Indicates that the SBOM file, which lists the components that make up the software, is analysed.


## Licences 

A licence is a type of agreement that states that the entity that developed the software gives you permission to use it, or permits you to use it. Open source found in components is likely to include such a licence.

It's important to verify the licences you identify in your analysis because while they allow you to use them, they also stipulate the conditions under which you can use them. Sparrow Cloud detects open source licences as issues. Be sure to further check the conditions of use, such as notice obligations and restrictions, for any licences that are detected.


## SBOMs

A Software Bill Of Materials (SBOM) is meta-information about the components utilised by the analysed software to provide a service. Sparrow Cloud provides the ability to export the analysed components as a file in the form of an SBOM.
For more information, see [Export SBOM](Export-SBOM.md).