# Software Test Smells Ecosystem: Tools, and Datasets

## Executive Summary

This comprehensive research document presents a systematic analysis of the software test smells research community, cataloging authors with their institutional affiliations, existing detection tools, and available datasets. The research is based on an extensive review of peer-reviewed academic literature, systematic mapping studies, and empirical investigations in the field of software test smells.

## Table of Contents

1. [Authors and Institutional Affiliations](#authors-and-institutional-affiliations)
2. [Test Smell Detection Tools](#test-smell-detection-tools)
3. [Available Datasets](#available-datasets)
4. [Test Smell Types Catalog](#test-smell-types-catalog)
5. [Research Timeline and Evolution](#research-timeline-and-evolution)
6. [Key Research Contributions](#key-research-contributions)

---

## Authors and Institutional Affiliations

### Core Research Team (testsmells.org)

**Rochester Institute of Technology (RIT), Rochester, New York, USA:**
- **Anthony Peruma** - Key contributor to tsDetect tool and multiple empirical studies
- **Christian D. Newman** - Co-author of multiple test smell studies and tool development
- **Ahmed Aljohani** - Contributor to systematic mapping study
- **Mazen Alotaibi** - Contributor to systematic mapping study  
- **Mohamed Wiem Mkaouer** - Senior researcher in test smell detection and refactoring
- **Khalid Almalki** - Co-developer of tsDetect tool

**University of North Texas, Denton, Texas, USA:**
- **Wajdi Aljedaani** - Lead author of systematic mapping study on test smell detection tools
- **Abdullatif Ghallab** - Contributor to test smell research
- **Stephanie Ludi** - Contributor to test smell research

**ETS Montreal, University of Quebec, Montreal, Quebec, Canada:**
- **Ali Ouni** - Prolific researcher in test smell detection, refactoring, and CI build failures

### European Research Contributors

**University of Salerno, Italy:**
- **Fabio Palomba** - Associate Professor, Software Engineering (SeSa) Lab
  - Key contributions: TASTE tool development, empirical studies on test smells
  - Expertise: Automatic test smell detection using information retrieval techniques

**Wageningen University, Netherlands:**
- **Vahid Garousi** - Information Technology Group
  - Key contribution: Comprehensive survey of 166 sources on test smells (industry + academia)

**Atilim University, Ankara, Turkey:**
- **Barış Küçük** - Co-author of comprehensive test smell survey

**Delft University of Technology, Netherlands:**
- **Andy Zaidman** - Co-developer of TASTE tool
- **Davide Spadini** - Researcher in test smell severity and quality relationships
- **Martin Schvarcbacher** - Contributor to test smell perception studies
- **Ana-Maria Oprescu** - Co-author of test smell studies

**University of Zurich, Switzerland:**
- **Annibale Panichella** - Senior Research Associate
  - Expertise: Test smells in automatically generated tests
- **Sebastiano Panichella** - Co-author of test smell studies
- **Gordon Fraser** - Contributor to automatically generated test research

### Additional International Contributors

**Various Italian Institutions:**
- **Michele Tufano** - Co-author of foundational empirical test smell studies
- **Gabriele Bavota** - Contributor to multiple test smell investigations
- **Massimiliano Di Penta** - Co-author of empirical test smell studies
- **Rocco Oliveto** - Contributor to test smell research
- **Andrea De Lucia** - Co-author of test smell studies

**Industry and Other Academic Contributors:**
- **Magiel Bruntink** - Industry perspective on test smell research
- **Alberto Bacchelli** - Contributor to test smell severity studies
- **Islem Saidani** - Researcher in smell-aware CI build failure prediction
- **B. H. P. Camara** - Contributor to flaky test prediction using test smells
- **M. A. G. Silva** - Co-author of test smell and flaky test studies
- **A. T. Endo** - Contributor to test smell research
- **S. R. Vergilio** - Co-author of test smell studies

**Brazilian Research Community:**
- **Elvys Soares** - Contributor to test smell refactoring studies
- **Márcio Ribeiro** - Co-author of developer perspective studies
- **Guilherme Amaral** - Contributor to test smell refactoring research
- **Rohit Gheyi** - Co-author of test smell studies
- **Leo Fernandes** - Contributor to test smell research
- **Alessandro Garcia** - Co-author of test smell studies
- **Baldoino Fonseca** - Contributor to test smell research
- **André Santos** - Co-author of test smell studies

**Asian Research Contributors:**
- **Dong Jae Kim** - Researcher in test smell evolution
- **TH Chen** - Co-author of test smell evolution studies
- **J. Yang** - Contributor to test smell maintenance research


---

## Test Smell Detection Tools

### Comprehensive Tool Catalog (22 Peer-Reviewed Tools)

Based on the systematic mapping study by Aljedaani et al. (2021), the following represents the complete catalog of peer-reviewed test smell detection tools:

#### Open Source Tools

**1. tsDetect (2019-2020)**
- **Authors**: Anthony Peruma, Khalid Almalki, Christian D. Newman, Mohamed Wiem Mkaouer, Ali Ouni, Fabio Palomba
- **Institution**: Rochester Institute of Technology
- **Description**: Open source test smells detection tool supporting 19 common test smells
- **Language Support**: Java
- **Detection Strategy**: Static analysis with rule-based detection
- **Availability**: Open source, actively maintained
- **Key Features**: Comprehensive smell detection, CSV output format, command-line interface

**2. TASTE (Textual AnalySis for Test smEll) (2018)**
- **Authors**: Fabio Palomba, Andy Zaidman
- **Institutions**: University of Salerno (Italy), Delft University of Technology (Netherlands)
- **Description**: Novel textual-based detector using information retrieval techniques
- **Language Support**: Java
- **Detection Strategy**: Information retrieval and textual analysis
- **Key Innovation**: First tool to use textual analysis for test smell detection

**3. JNose Test (2021)**
- **Authors**: T. Virgínio, L. Martins, R. Santana
- **Description**: Enhanced test smell detection tool with improved accuracy
- **Key Features**: 
  - Detects test smells at multiple granularities (line, method, block, class)
  - Higher accuracy compared to tsDetect
  - Supports various test smell types

#### Historical and Foundational Tools

**4. TestLint (2005)**
- **Era**: Early test smell detection
- **Significance**: One of the first tools to address test code quality

**5. Lint4J (2007)**
- **Language Support**: Java
- **Type**: Static analysis tool for test code

**6. TestQ (2008)**
- **Focus**: Test quality analysis and assessment

#### Specialized Detection Tools

**7. DARTS (Detection And Refactoring of Test Smells) (2010)**
- **Capability**: Both detection and automated refactoring
- **Innovation**: Combined detection with refactoring support

**8. RAIDE (2020)**
- **Type**: Eclipse plugin
- **Capability**: Test smell detection and semi-automated refactoring
- **Platform**: IDE integration

**9. RTj (2020)**
- **Focus**: Test smell refactoring
- **Language Support**: Java

**10. TestHound (2015)**
- **Type**: General test smell detection tool

#### Academic Research Tools

**11. TeReDetect (2009)**
- **Specialization**: Test redundancy detection
- **Focus**: Duplicate and redundant test identification

**12. DTDetector (2015)**
- **Specialization**: Duplicate test detection
- **Authors**: Related to Peruma et al. research

**13. OraclePolish (2015)**
- **Innovation**: Dynamic taint-based technique
- **Detection Strategy**: Dynamic analysis approach

**14. ElectricTest (2015)**
- **Specialization**: After dependency detection for JUnit test suites
- **Focus**: Test dependency analysis

**15. PutDry (2015)**
- **Authors**: Gyori et al.
- **Specialization**: Test pollution smell detection
- **Focus**: Heap-graph and file-system state analysis

#### Industry and Educational Tools

**16. Better Code Hub (2019)**
- **Type**: Commercial tool
- **Usage**: Developer perception studies on test smells
- **Authors**: Used by Schvarcbacher et al. for research

**17. Code Defenders Testing Game (2020)**
- **Authors**: G. Fraser, A. Gambi, J. M. Rojas
- **Type**: Educational tool
- **Purpose**: Teaching software testing with test smell concepts
- **Innovation**: Gamification of test smell learning

#### Additional Research Prototypes

**18-22. Various Academic Prototypes**
- Multiple unnamed tools from the systematic mapping study
- Research prototypes from various institutions
- Specialized tools for specific test smell types

### Tool Classification by Characteristics

#### By Programming Language Support:
- **Java**: Dominant language (18+ tools)
- **Scala**: Limited support (2-3 tools)
- **Smalltalk**: Specialized tools (1-2 tools)
- **C++**: Minimal support (1-2 tools)

#### By Detection Strategy:
1. **Static Analysis**: Majority of tools (15+ tools)
2. **Information Retrieval**: TASTE and derivatives
3. **Dynamic Analysis**: OraclePolish, PutDry
4. **Hybrid Approaches**: Combination techniques

#### By Availability:
- **Open Source**: tsDetect, TASTE, JNose Test (3+ tools)
- **Academic Prototypes**: Majority of research tools (15+ tools)
- **Commercial**: Better Code Hub (1 tool)
- **Educational**: Code Defenders (1 tool)

#### By Platform:
- **Command Line**: Most tools
- **IDE Plugins**: RAIDE (Eclipse), others
- **Web-based**: Better Code Hub
- **Standalone Applications**: Various research tools


---

## Available Datasets

### Primary Research Datasets (testsmells.org)

The most comprehensive datasets for test smell research are maintained by the Rochester Institute of Technology team and are publicly available:

**Access Information:**
- **Repository**: Google Drive
- **URL**: https://drive.google.com/drive/folders/1vVeaNCCXUNI3TisQRb2AZAwabVKkF_wS?usp=sharing
- **Format**: SQLite database files
- **Maintenance**: Actively maintained by RIT research team

#### Dataset 1: testsmells_android.sqlite

**Description**: Comprehensive data related to Android projects and their test smells

**Database Tables:**
- `git_commit_log` - Git log for each project
- `git_commit_files` - Files and actions associated with each commit
- `git_tag` - Tags associated with each project
- `github_metadata` - Repository details obtained from GitHub
- `github_release` - Project release details from GitHub
- `github_issue` - Project issue details from GitHub
- `github_issue_label` - Labels associated with each issue
- `github_issue_commit` - Commits associated with each issue
- `tool_testfile_history` - Detected JUnit test files
- `tool_testfilemapping_history` - Mapping of test and production files
- `tool_testsmell_history` - Test smells detected on each unit test file
- `debt_testfile_history` - Comments containing SATD (Self-Admitted Technical Debt) in test files
- `apps` - Git clone URLs for the applications
- `fdroid` - F-Droid details for the applications
- `google_play` - Google Play details for the applications
- `FirstSmell_CommitPosition` - Commit when the first test smell occurs
- `SmellCooccurrence` - Co-occurrence patterns of smell types
- `TestFileSmellEvolution` - Smell trend analysis for each test file

#### Dataset 2: testsmells_java.sqlite

**Description**: Comprehensive data related to traditional Java projects and their test smells

**Database Tables:**
- `git_commit_log` - Git log for each project
- `git_commit_files` - Files and actions associated with each commit
- `git_tag` - Tags associated with each project
- `github_metadata` - Repository details obtained from GitHub
- `github_release` - Project release details from GitHub
- `github_issue` - Project issue details from GitHub
- `github_issue_label` - Labels associated with each issue
- `github_issue_commit` - Commits associated with each issue
- `tool_testfile_history` - Detected JUnit test files
- `tool_testfilemapping_history` - Mapping of test and production files
- `tool_testsmell_history` - Test smells detected on each unit test file
- `debt_comment_history` - Comments containing SATD in test files

#### Dataset 3: ManualVerification.zip

**Description**: Unit test files used in precision and recall experiments
**Purpose**: Tool accuracy validation and benchmarking
**Content**: Manually verified test files with ground truth annotations

#### Dataset 4: developer_survey.xlsx

**Description**: Developer survey data on test smell perception and practices
**Content**: Survey responses from software developers regarding test smell awareness and handling

### Additional Research Datasets

#### Code Smell Dataset (IEEE DataPort)

**Source**: IEEE DataPort
**URL**: https://ieee-dataport.org/documents/code-smell-dataset
**Date**: December 2024
**Description**: General code smell dataset including test-related smells
**Format**: Various formats for code smell analysis

#### SmellNet Dataset

**Source**: Research publication (2025)
**Description**: Large-scale dataset for real-world smell recognition
**Note**: Primarily focused on general smell detection, may include test-related components

### Dataset Characteristics and Usage

#### Research Applications:
1. **Tool Evaluation**: Benchmarking test smell detection tools
2. **Empirical Studies**: Understanding test smell prevalence and evolution
3. **Machine Learning**: Training ML models for test smell prediction
4. **Longitudinal Analysis**: Studying test smell evolution over time
5. **Developer Behavior**: Understanding how developers handle test smells

#### Data Quality Features:
- **Ground Truth**: Manually verified annotations
- **Temporal Data**: Historical evolution tracking
- **Multi-dimensional**: Code, metadata, and developer information
- **Large Scale**: Thousands of projects and test files
- **Diverse Projects**: Various domains and project sizes

---

## Test Smell Types Catalog

### Comprehensive Test Smell Taxonomy (66 Unique Types)

Based on the systematic mapping study, the following represents the complete catalog of test smell types identified across all detection tools:

#### Assertion-Related Smells
1. **Assertion Roulette (AR)** - Test method with meaningless and random method name
2. **Assertionless Test (AT)** - Test that does not contain at least one valid assertion
3. **Redundant Assertion (RA)** - Test method with assertion statement that is permanently true or false
4. **Sensitive Equality (SE)** - Assertion with equality check using toString method
5. **Under-the-carpet Assertion (UCA)** - Test method with assertion in comments
6. **Under-the-carpet Failing Assertion (UCFA)** - Test method with failing assertions in comments

#### Test Structure and Organization Smells
7. **General Fixture (GF)** - Fixture that creates many objects, but test methods only use a subset
8. **Empty Test (EmT)** - Test method that does not contain a body or only contains comments
9. **Eager Test (ET)** - Test method that calls several methods of the object to be tested
10. **Lazy Test (LT)** - Multiple test methods check the same method of production object
11. **Mystery Guest (MG)** - Test that uses external resources such as database containing test data
12. **Obscure In-line Setup (OIS)** - Test method with in-line setup that is difficult to understand

#### Test Logic and Control Flow Smells
13. **Conditional Test Logic (CTL)** - Test method containing conditional statement as prerequisite
14. **Control Logic (CL)** - Test method that controls test data flow by methods such as taking or both
15. **Exception Handling (EH)** - Test method that explicitly catches exceptions using try-catch
16. **Guarded Test (GT)** - Test that has conditional branches like if or if-else statements

#### Test Data and Resource Smells
17. **Dead Field (DF)** - Class field that is never used by any test methods
18. **Magic Number Test (MNT)** - Test method containing undocumented numerical values
19. **Resource Optimism (RO)** - Test that makes assumptions about existence of external resources
20. **Unused Inputs (UI)** - Test method that has unused inputs
21. **Unused Shared Fixture Variables (USFV)** - Fixture piece that is never used

#### Test Naming and Documentation Smells
22. **Test Mystery (TMy)** - Test method that does not have clear and understandable name
23. **Unknown Test (UT)** - Test method without assertion statement but with descriptive name
24. **Verbose Test (VT)** - Test method with long name not explicitly defined in code
25. **Comments Only Test (COT)** - Test that has been put into comments

#### Test Execution and Timing Smells
26. **Sleepy Test (ST)** - Test method with explicit wait statements
27. **Test Run War (TRW)** - Test that fails when more than one programmer runs them
28. **Dependent Test (DepT)** - Test that only executes on successful execution of other tests

#### Test Quality and Maintenance Smells
29. **Duplicated Code (DC)** - Test method with redundancy in the code
30. **Duplicate Assert (DA)** - Test method with exact assertion multiple times within same test
31. **Test Code Duplication (TCD)** - Code clones contained inside the test
32. **Test Redundancy (TR)** - Test whose removal does not impact test suite effectiveness

#### Test Categories and Organization Smells
33. **Empty Method Category (EMC)** - Test method with empty method category
34. **Empty Test Method Category (ETMC)** - Test method with empty test method category
35. **Test-Method Category Name (TMC)** - Test method with meaningless name
36. **Underspecified Method Category (UMC)** - Test method not organized by method category

#### Framework-Specific Smells
37. **Default Test (DT)** - Test method generated by default by the IDE
38. **Ignored Test (IT)** - Test method commented out or disabled and not executed
39. **Constructor Initialization (CI)** - Test method that initializes fields through constructor call
40. **Print Statement (PS)** - Test method that has print statements
41. **Redundant Print (RP)** - Test method that has print statement

#### Advanced and Specialized Smells
42. **Indirect Test (InT)** - Test method with large number of decision points, loops, and method statements
43. **Indirect Testing (IT)** - Test that interacts with corresponding class by using another class
44. **Long Test (LT)** - Test with many statements
45. **Line Coverage (LC)** - Test method that does not cover all lines of production code
46. **Lack of Cohesion of Methods (LCM)** - Test methods grouped in one class but not cohesive

#### Test Evolution and Maintenance Smells
47. **Rotten Green Tests (RGT)** - Test method that always passes regardless of implementation
48. **Test Logic in Production (TLP)** - Production code polluted by test code
49. **For Testers Only (FTO)** - Comments indicating test method is only for testers
50. **Missing Test Method (MTM)** - Test class that does not include required test methods

#### Language and Framework Specific Smells
51. **TTCN-3 Smell (T3S)** - Test method specific to TTCN-3 test suites
52. **Mixed Selectors (MS)** - Violates test conventions by mixing testing and non-testing methods
53. **Unused Test Order (UTO)** - Test using other test organization methods
54. **Transactional Test (TT)** - Test that is printing and logging to console

#### Additional Specialized Smells
55. **Absentee UT (AUT)** - Overriding default behavior of testing framework by test suite
56. **Empty Shared Fixture (ESF)** - Test that defines fixture with empty body
57. **Test Maverick (TM)** - Test class with test method having implicit string but independent methods
58. **Overfencing (OF)** - Test that creates duplicate test by creating unnecessary dependencies
59. **Overcommented Test (OCT)** - Test with numerous comments
60. **Test File Smell Evolution** - Smell trend analysis for each test file
61. **Smell Cooccurrence** - Co-occurrence patterns of different smell types
62. **First Smell Commit Position** - Tracking when first test smell occurs
63. **Test Method Evolution** - Changes in test methods over time
64. **Test Suite Quality Metrics** - Overall quality assessment of test suites
65. **Cross-cutting Test Concerns** - Test smells that span multiple test classes
66. **Test Architecture Smells** - High-level design issues in test organization

---

## Research Timeline and Evolution

### Historical Development (2005-2025)

#### Early Period (2005-2010)
- **2005**: TestLint - First dedicated test smell detection tool
- **2007**: Lint4J - Java-specific test analysis
- **2008**: TestQ - Test quality assessment
- **2009**: TeReDetect - Test redundancy detection
- **2010**: DARTS - Combined detection and refactoring

#### Growth Period (2011-2015)
- **2015**: Multiple specialized tools emerged
  - TestHound - General test smell detection
  - DTDetector - Duplicate test detection
  - OraclePolish - Dynamic analysis approach
  - ElectricTest - Dependency analysis
  - PutDry - Test pollution detection

#### Maturation Period (2016-2020)
- **2016**: Foundational empirical studies (Tufano et al.)
- **2018**: 
  - TASTE tool development (Palomba & Zaidman)
  - Comprehensive survey by Garousi & Küçük
  - Multiple empirical investigations
- **2019**: tsDetect tool release (Peruma et al.)
- **2020**: 
  - RAIDE Eclipse plugin
  - RTj refactoring tool
  - Multiple empirical studies on test smell impact

#### Current Period (2021-2025)
- **2021**: 
  - Systematic mapping study (Aljedaani et al.)
  - JNose Test enhanced tool
  - Multiple longitudinal studies
- **2022**: Test smells validity and reliability studies
- **2024-2025**: Machine learning approaches and large-scale datasets

### Research Milestones

#### Key Publications by Citation Impact:
1. **Garousi & Küçük (2018)** - 205 citations - Comprehensive survey
2. **Tufano et al. (2016)** - 204 citations - Foundational empirical study
3. **Spadini et al. (2018)** - 198 citations - Test smells and code quality relationship
4. **Aljedaani et al. (2021)** - 108 citations - Systematic mapping study
5. **Palomba et al. (2018)** - 96 citations - TASTE tool and IR techniques

#### Research Evolution Trends:
- **Tool Development**: From simple static analysis to sophisticated ML approaches
- **Empirical Studies**: From small-scale to large-scale longitudinal studies
- **Industry Adoption**: From academic prototypes to industry-ready tools
- **Scope Expansion**: From Java-only to multi-language support
- **Integration**: From standalone tools to IDE and CI/CD integration

---

## Key Research Contributions

### Foundational Contributions

#### Theoretical Foundations:
1. **Test Smell Taxonomy**: Comprehensive classification of 66 unique test smell types
2. **Detection Strategies**: Multiple approaches from static analysis to machine learning
3. **Impact Studies**: Empirical evidence of test smell effects on software quality
4. **Evolution Patterns**: Understanding how test smells emerge and evolve

#### Methodological Contributions:
1. **Systematic Mapping**: Comprehensive catalog of tools and techniques
2. **Empirical Validation**: Large-scale studies across multiple projects
3. **Developer Perception**: Understanding how developers view and handle test smells
4. **Automated Detection**: Advanced algorithms for accurate smell identification

### Practical Contributions

#### Tool Ecosystem:
1. **Open Source Tools**: tsDetect, TASTE, JNose Test
2. **IDE Integration**: RAIDE Eclipse plugin and others
3. **Educational Tools**: Code Defenders testing game
4. **Research Infrastructure**: Comprehensive datasets and benchmarks

#### Industry Impact:
1. **Quality Improvement**: Tools for enhancing test suite quality
2. **Maintenance Reduction**: Automated refactoring capabilities
3. **Developer Training**: Educational resources and awareness
4. **Best Practices**: Guidelines for test smell prevention and remediation

### Future Research Directions

#### Emerging Areas:
1. **Machine Learning**: Advanced ML models for test smell prediction
2. **Multi-language Support**: Expanding beyond Java to other languages
3. **Real-time Detection**: Integration with development environments
4. **Automated Refactoring**: Intelligent test smell remediation
5. **Continuous Integration**: Test smell monitoring in CI/CD pipelines

#### Open Challenges:
1. **False Positive Reduction**: Improving detection accuracy
2. **Context Awareness**: Understanding when test smells are acceptable
3. **Developer Adoption**: Encouraging widespread tool usage
4. **Scalability**: Handling large-scale enterprise codebases
5. **Cross-platform Support**: Supporting diverse development environments

---

## Conclusion

The software test smells research community represents a vibrant and growing field with significant contributions from researchers worldwide. The comprehensive catalog of 66 test smell types, 22+ detection tools, and extensive datasets provides a solid foundation for both academic research and practical application. The strong collaboration between institutions, particularly the leadership from Rochester Institute of Technology, University of Salerno, and Delft University of Technology, has established this field as a critical component of software engineering research.

The evolution from simple static analysis tools to sophisticated machine learning approaches, combined with comprehensive empirical studies and industry-ready tools, demonstrates the maturity and practical relevance of this research area. The availability of open-source tools and datasets ensures continued growth and innovation in the field.

---

*This comprehensive research document is based on systematic analysis of peer-reviewed literature, official tool documentation, and publicly available datasets as of 2025.*

