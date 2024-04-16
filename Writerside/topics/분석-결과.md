# Analysis Results

In Projects, you can view information about analyses performed on your project, including recent analyses, and set options for performing analyses. The detailed results of analyses are displayed in four tabs on the right side of the project: Summary, Issues, Assets, and Components.

## Issues

**Issues** are the security vulnerabilities and quality issues found as a result of analysing the analysed object. The **Issue List** displayed in the **Issues** tab contains the issues detected by Sparrow Cloud. Issues are categorised as source code issues, component issues, or web vulnerability issues, depending on the tool that detected them.

For more information about issues, see [Issues](issues.md).

## Assets

Sparrow Cloud displays analysis results called **Assets**. Assets are created from the analyzing target you used for your analysis: It identifies the files or sub URLs contained in the analysis target and uses this information to show a list of **assets**. Depending on the analysis target, assets identified from repositories used for source code analysis and component analysis are shown as **Files**, while assets sourced from web pages used for web vulnerability analysis are shown as **URLs**.

For more information about assets, see [Assets](assets.md).

## Component

A **component** is the smallest unit that can identify a specific programme and refers to software that requires a licence, proprietary software, open source software, etc. Sparrow Cloud breaks down files into components to identify what software is included in the file being analysed, and organises the open source licences that the components are using into individual components on the **Components** tab. Additionally, components that are under a specific licence are detected as issues in the issue list.

For more information about components, see [Components](components.md).

