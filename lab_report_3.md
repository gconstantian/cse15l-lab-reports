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
find technical/ -type f -size +100k
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
input
```
find technical/ -type f -size -2k
```
output
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
In the first example the command line finds all the files in technical that are larger than 100k and the second example finds all the files in technical that are less than 2k. This can be helpful in finding what is taking the most amount of storage and what files might need to be moved elsewhere to make room for other items.

## 2 -empty
This command checks if a directory is empty.
input
```
find technical/ -type d ! -empty
```
output
```
technical/
technical//government
technical//government/About_LSC
technical//government/Env_Prot_Agen
technical//government/Alcohol_Problems
technical//government/Gen_Account_Office
technical//government/Post_Rate_Comm
technical//government/Media
technical//plos
technical//biomed
technical//911report
```
input
```
find technical/ -type d -empty
```
output
```
```
In the first example the command line finds all the directories that have stuff in them and the second example gives all the directories that are empty.

## 3 -type
This command finds all the objects that match the given type
inpyt
```
find technical/ -type d
```
output 
```
technical/
technical//government
technical//government/About_LSC
technical//government/Env_Prot_Agen
technical//government/Alcohol_Problems
technical//government/Gen_Account_Office
technical//government/Post_Rate_Comm
technical//government/Media
technical//plos
technical//biomed
technical//911report
```
input
```
find technical/government/Env_Prot_Agen -type f
```
output
```
technical/government/Env_Prot_Agen/multi102902.txt
technical/government/Env_Prot_Agen/section-by-section_summary.txt
technical/government/Env_Prot_Agen/jeffordslieberm.txt
technical/government/Env_Prot_Agen/final.txt
technical/government/Env_Prot_Agen/ctf7-10.txt
technical/government/Env_Prot_Agen/ctf1-6.txt
technical/government/Env_Prot_Agen/ro_clear_skies_book.txt
technical/government/Env_Prot_Agen/ctm4-10.txt
technical/government/Env_Prot_Agen/1-3_meth_901.txt
technical/government/Env_Prot_Agen/atx1-6.txt
technical/government/Env_Prot_Agen/tech_sectiong.txt
technical/government/Env_Prot_Agen/bill.txt
technical/government/Env_Prot_Agen/nov1.txt
technical/government/Env_Prot_Agen/tech_adden.txt
```
The first command looks for objects that are a directory and the second example looks for objects that are files within a specific directory. These are notified by whatever letter comes after -type. f means it is a regular file and d means it is a directory.

## 4 -delete
deletes an object
input
```
find technical/911report/chapter-11.txt -delete
```
output
```
find: -delete: technical/911report/chapter-11.txt: relative path potentially not safe
```
input
```
find technical/911report/ -delete
```
output
```
find: -delete: technical/911report/: relative path potentially not safe
```
This command line deletes things. The first example it deletes a textfile and the second example it deletes an entire directory. This is useful when you want to delete files.
