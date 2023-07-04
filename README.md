# Introduction

This repository hosts the artifact of Understanding Resolution of Multi-Language Bugs: An Empirical Study on Apache Projects. `ProjectInfo.pdf` and `NumberofPLsinMPLBs(RQ2).pdf` are the online tables from the article. Details are given below.

## ProjetInfo.pdf

This PDF file contains basic information about the used projects.

## NumberofPLsinMPLBs(RQ2).pdf

This PDF file contains information about the results of RQ2.

## DataSet

This folder contains the raw data and results of the experiments. The raw data consists of two parts: GitHubData and JIRAData.

### GitHubData

This folder contains one file `CommitRecord.zip`, which is extracted to get the `CommitRecord` folder. `CommitRecord` contains the commit history text for each project.

### JIRAData

This folder contains two files `issue.csv.zip` and `transition.csv.zip`, which can be extracted to get `issue.csv` and `transition.csv`. `issue.csv` mainly contains the Summary and Description of the bug, `transition.csv` mainly contains the status transition information of the bug.

### ResultData

This folder contains two files `bugs_study.csv` and `manual_analysis.xlsx`. `bugs_study.csv` is the bug dataset used in RQ1 to RQ4, and `manual_analysis.xlsx` is the result of RQ5 manual analysis.

<details><summary>bugs_study.csv</summary>
<p>
This SQL file can be imported into MySQL and will create a  `bugs_study` table. Its structure is as below: 

### #

The serial number of the bug.

### BugID

The unique ID of the bug in the Apache projects.

### IsMPLB

Whether the bug is an MPLB. '0' means the bug is SPLB, '1' means the bug is MPLB.

### PL

The name of the PLs involved in the resolution of the bug.

### PLNo

The number of PLs involved in the resolution of the bug.

### LOCM

The number of lines of source code modified in the bug.

### NOFM

The number of source files modified in the bug.

### NODM

The number of directories modified in the bug.

### OT

The time from the creation of a bug report to the final resolution of the bug.

### Entropy

The normalized entropy of the modified source files for fixing the bug during the last 60 days.

### Reopen

Whether the bug was reopened. '0' means the bug has not been reopened, '1' means the bug has been reopened. 


</p>
</details>



<details><summary>manual_analysis.xlsx</summary>
<p>
This Excel file has three columns, as explained below:

### BugID

The unique ID of the bug in the Apache projects.

### Bug Resolution Category

Each bug is labelled with a bug resolution category, i.e., a cause for why this bug resolution involves multiple PL.

### Cross-language Calling Mechanisms

Each bug labelled with zero, one, or multiple cross-language calling mechanisms used in this bug resolution.
</p>
</details>



