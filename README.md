# CAISE2022

This repository contains the source code to compute overall time and cost information for composed services. 

### Publication: 

Hollauf, F.S., Franceschetti, M., Eder, J. (2022). Time-Cost Tradeoffs for Composed Services. In: Franch, X., Poels, G., Gailly, F., Snoeck, M. (eds) Advanced Information Systems Engineering. CAiSE 2022. Lecture Notes in Computer Science, vol 13295. Springer, Cham. https://doi.org/10.1007/978-3-031-07472-1_31

Setup:
  - Java SDK 13
  - Maven 3.6.3
  - JUnit 5
  - XML Input: JAXB
  - XLSX Output: Apache POI

Input: XML-files validating against schema provided under src\main\resources\TCP.xsd
  - 1 XML-file = 1 tree to compute
  - put files to run under src\main\resources\Input
  - examples can be found here: src\main\resources\Examples\*

Run:
  - BEFORE: create src\main\resources\Output directory!
  - after placing input files run src\main\java\CalculateOverallTCMap.java
  
Output: 
  - overall TCMap as XLSX-file for each file in the input directory under src\main\resources\Output

Experiments:
  - Setup:
    - Windows 10 machine
    - 16 GB RAM

  - input files: src\main\resources\Examples
  - run src\main\java\ExperimentsMain.java
  - runs each calculation 100 times (=> static final int NUMTESTRUNS)
  - each directory in src\main\resources\Examples represents a class with several files to test
  - output file: each directory gets own sheet, while the files in it represent the row names for each sheet
  - output: src\main\resources\Examples\SpeedTestResults.xlsx
  - presented results in the CAiSE2022 submission can be found here: src\main\resources\Examples\SpeedTestResultsPaperVersion.xlsx
