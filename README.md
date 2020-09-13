# Guttman Chart Analyzation System

## Introduction
Guttman chart is useful for educators to analyse students' academic performance. Through the chart, teachers can intuitively see irrgular patterns or odd behaviours among a group of students.

The educator collect students' assessment data and convert it into a guttman chart format file (normally an Excel file). He/she then can upload this guttman chart format file to this system, which can automatically analyze the assessment data. The system can find out which part of the assessment data is odd and irregular and can be visually rendered on the website.

## Instructions for Building and Executing

### Run on Your Local PC

#### Step1. Install Python

Makes sure you have `python3` and `pip` installed. `Python 3.7` was confirmed to work, lower versions of `Python3` were not tested.

`Python 2.x` were confirmed **NOT** working.


#### Step2. Install Python libraries

`pip3 install 'flask>=1.1.1' pandas xlsxwriter xlrd textdistance`

If you do not have a shortcut for pip, use
`python3 -m pip install 'flask>=1.1.1' pandas xlsxwriter xlrd textdistance` 
 
or `python -m pip install 'flask>=1.1.1' pandas xlsxwriter xlrd textdistance` 


Please notice some lower versions of flask were confirmed **NOT** working.


#### Step3. Install Git, and clone our repo

`git -c http.sslVerify=false clone https://bitbucket.cis.unimelb.edu.au:8445/scm/swen900142019rvquoll/swen90014-2019-rv-quoll.git`


#### Step4. Run

`cd swen90014-2019-rv-quoll`

`flask run`

If you do not have a shortcut for flask, use
`python3 -m flask run` or

`python -m flask run`

The server should be listening on http://127.0.0.1:5000 (defualt setting of flask)


#### Step5. Test
To run all back-end unit tests: `python3 test.py` 

For mannual test, you could use **[repo_root_path]/testdata** as test data.

**Note:**
In this sprint, we have not handled possible errors or exceptions yet. 
If you are going to use your own test data, please notice that the format of the Excel file must follow all rules below:

1. File extension **MUST** be .xls or .xlsx
2. The excel file **MUST** have **two** worksheets.
3. The **first** row should be the description of each item.
4. Students' data should begin from the **third** row.
5. The number of sub-items should be greater than the max marks.<br/>