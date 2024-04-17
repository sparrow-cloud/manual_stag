# Component

## Identification type

Indicate the type of target used to identify the component: **Binary**, **Dependencies**, **Source Code**, **Snippets**, **SBOM**.

- Binary: means that the target analysed is a binary file.
- Dependency: If a dependency file was analysed, such as **pom.xml**, which lists the libraries used by the software.
- Source code: source code is analysed to generate and compare hash values of the source code.
- Snippets: Marks header files (.h or .hpp) among C/C++ language files as the type to analyse.
- SBOM: Indicates that the SBOM file, which lists the components that make up the software, is analysed.


## Licence or Open source license

The licence is a type of agreement that states that the entity that developed the software gives you permission or permission to use the software. Open source found in a component is likely to include such a licence.

It's important to check the licences you identify in your analysis, because while they allow you to use them, they also stipulate the conditions under which you can use them. Sparrow Cloud detects copyleft and permissive licences as issues, among other licences. Be sure to additionally check the terms of the licence that corresponds to the detected issue.


## SBOM

The Software Bill Of Materials (SBOM) is meta-information about the components used by the analysed software to provide services. Sparrow Cloud provides the ability to export the analysed components to a file in the form of an SBOM.
For more information, see [Export SBOM](SBOM_내보내기.md).
