## Researching Command
## find

1. find ./technical -name 

~~~
find ./technical -name *hapter-13* //find files whose name contain hapter-13

./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
~~~

It finds files whose name contain hapter-13, and it is useful because it helps you finding out files contain certain substring. 

~~~
find ./technical -name *pter-13.*.txt

./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
~~~

It finds all txt files whose name contain pter-13. It is useful when you only want to find files with the name and also are certain file type (.txt, for example). 

~~~
find ./technical -name chapter-13.1.txt

./technical/911report/chapter-13.1.txt
~~~

It finds one specific file whose name is "chapter-13.1.txt". It is useful when you need to find one certain file. 
<Br>
2. find -type 

~~~
find ./technical -type d 
./technical
./technical/911report
./technical/biomed
./technical/government
./technical/government/About_LSC
./technical/government/Alcohol_Problems
./technical/government/Env_Prot_Agen
./technical/government/Gen_Account_Office
./technical/government/Media
./technical/government/Post_Rate_Comm
./technical/plos
~~~

It finds all directories within technical. It is useful because it helps you finding all directories in a directory. It does not only find the child directories, but also child of the child directories. 

~~~
find ./technical/government/Alcohol_Problems/ -type f

./technical/government/Alcohol_Problems/DraftRecom-PDF.txt
./technical/government/Alcohol_Problems/Session2-PDF.txt
./technical/government/Alcohol_Problems/Session3-PDF.txt
./technical/government/Alcohol_Problems/Session4-PDF.txt
~~~

It finds all files within aalcohol_problems directory. It is useful when you only want to return files within a directory. 

~~~
find ./technical/government/ ! -type f

./technical/government/
./technical/government/About_LSC
./technical/government/Alcohol_Problems
./technical/government/Env_Prot_Agen
./technical/government/Gen_Account_Office
./technical/government/Media
./technical/government/Post_Rate_Comm
~~~

It finds all files within government that are not files. It is useful when you want to exclude all files when return. 
<Br>
3. find -size

~~~
find ./technical/911report -size -10M

./technical/911report
./technical/911report/chapter-1.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-8.txt
./technical/911report/chapter-9.txt
~~~

It finds all files under 10 megabytes. This is particularly useful because it allows you to find files with certain sizes. 

~~~
find ./technical/911report -size +100k

./technical/911report/chapter-1.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
~~~

It finds all files larger than 100 kilobyte. This is useful when you want to exclude very small files. 

~~~
find ./technical/911report -size +100k -size -150k

./technical/911report/chapter-1.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
~~~

It finds all files greater than 100 kilobytes and smaller than 150 kilobytes. This is useful when you want to find files within certain size range. 
<Br>
<Br>

