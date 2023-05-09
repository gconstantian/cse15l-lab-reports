#  Lab Report 3

Hello! Welcome to the third part of the CSE15l journey!! Here we are going to learn about using the command-line

We will be focusing on the 
```
find
```
command

## 1 -size

What this does is find files that are either greater than or less than the memory amount given.

input
```
bash-3.2$ find technical/ -type f -size +100k
```

output
```
technical//government/About_LSC/commission_report.txt
technical//government/About_LSC/State_Planning_Report.txt
technical//government/Env_Prot_Agen/multi102902.txt
technical//government/Env_Prot_Agen/ctm4-10.txt
technical//government/Env_Prot_Agen/bill.txt
technical//government/Env_Prot_Agen/tech_adden.txt
technical//government/Gen_Account_Office/d0269g.txt
technical//government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
technical//government/Gen_Account_Office/Sept27-2002_d02966.txt
technical//government/Gen_Account_Office/d01376g.txt
technical//government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
technical//government/Gen_Account_Office/pe1019.txt
technical//government/Gen_Account_Office/gg96118.txt
technical//government/Gen_Account_Office/d01591sp.txt
technical//government/Gen_Account_Office/im814.txt
technical//government/Gen_Account_Office/ai9868.txt
technical//government/Gen_Account_Office/May1998_ai98068.txt
technical//government/Gen_Account_Office/d02701.txt
technical//biomed/1471-2105-3-2.txt
technical//911report/chapter-13.4.txt
technical//911report/chapter-13.5.txt
technical//911report/chapter-13.2.txt
technical//911report/chapter-13.3.txt
technical//911report/chapter-3.txt
technical//911report/chapter-1.txt
technical//911report/chapter-6.txt
technical//911report/chapter-7.txt
technical//911report/chapter-9.txt
technical//911report/chapter-12.txt
```
```
find technical/ -type f -size -2k
```
```
technical//government/Media/Helping_Hands.txt
technical//government/Media/Campaign_Pays.txt
technical//government/Media/Fire_Victims_Sue.txt
technical//government/Media/Court_Keeps_Judge_From.txt
technical//government/Media/It_Pays_to_Know.txt
technical//government/Media/Self-Help_Website.txt
technical//government/Media/Justice_requests.txt
technical//government/Media/Wilmington_lawyer.txt
technical//government/Media/Lawyer_Web_Survey.txt
technical//plos/pmed.0020048.txt
technical//plos/pmed.0020028.txt
technical//plos/pmed.0020191.txt
technical//plos/pmed.0020226.txt
technical//plos/pmed.0020192.txt
technical//plos/pmed.0020157.txt
technical//plos/pmed.0020082.txt
technical//plos/pmed.0020120.txt
```


## 2

## 3

## 4
