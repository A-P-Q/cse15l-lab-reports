## Researching Command
## find
~~~
1. find ./technical -name *hapter-13* //find files whose name contain hapter-13

./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
~~~
It finds files whose name contain hapter-13, and it is useful because it helps you finding out files contain certain substring. 
~~~
2. find ./technical/government/Alcohol_Problems/  //find all files under dir

./technical/government/Alcohol_Problems/
./technical/government/Alcohol_Problems/DraftRecom-PDF.txt
./technical/government/Alcohol_Problems/Session2-PDF.txt
~~~
It finds all files under alcohol problems. It is useful because it helps you finding all files under one specific directory. 
~~~
3. find ./technical -type d -name A*  //find dir whose name start with A

./technical/government/About_LSC
./technical/government/Alcohol_Problems
~~~
It finds all files whose name starts with the letter A. This is particularly useful because it allows you to find files with certain names. 
<Br>
<Br>
## less
~~~
less ./technical/911report/preface.txt    //display whole file

 PREFACE
            We present the narrative of this report and the recommendations that flow from it to
                the President of the United States, the United States Congress, and the American
                people for their consideration. Ten Commissioners-five Republicans and five
                Democrats chosen by elected leaders from our nation's capital at a time of great
                partisan division-have come together to present this report without dissent.
            We have come together with a unity of purpose because our nation demands it.
                September 11, 2001, was a day of unprecedented shock and suffering in the history of
                the United States. The nation was unprepared. How did this happen, and how can we
                avoid such tragedy again?
~~~
It displays the contents in a txt file. It is particularly useful when you  want  to find the content in a file. 
~~~
less -N ./technical/911report/preface.txt //display whole file with line number
      1
      2
      3
      4             PREFACE
      5             We present the narrative of this report and the recommendations that flow from it to
      6                 the President of the United States, the United States Congress, and the American
      7                 people for their consideration. Ten Commissioners-five Republicans and five
      8                 Democrats chosen by elected leaders from our nation's capital at a time of great
      9                 partisan division-have come together to present this report without dissent.
     10             We have come together with a unity of purpose because our nation demands it.
     11                 September 11, 2001, was a day of unprecedented shock and suffering in the history of
     12                 the United States. The nation was unprepared. How did this happen, and how can we
     13                 avoid such tragedy again?
~~~
It displays the contents in a txt file with line numbers. This is particularly useful when you want to count line numbers of a file. 
~~~
less  -p happen ./technical/911report/preface.txt   //display file start with line which has first appearence of "happen"  

	      the United States. The nation was unprepared. How did this happen, and how can we
                avoid such tragedy again?
            To answer these questions, the Congress and the President created the National
                Commission on Terrorist Attacks Upon the United States (Public Law 107-306, November
                27, 2002).
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
                relating to the terrorist attacks of September 11, 2001," including those relating
                to intelligence agencies, law enforcement agencies, diplomacy, immigration issues
                and border control, the flow of assets to terrorist organizations, commercial
                aviation, the role of congressional oversight and resource allocation, and other
                areas determined relevant by the Commission. In pursuing our mandate, we have
                reviewed more than 2.5 million pages of documents and interviewed more than 1,200
                individuals in ten countries. This included nearly every senior official from the
~~~
It displays files with line which has first appearance of "happen". This is particularlly useful when you need to find certain lines containing certain words/substrings. 
<Br>
<Br>
## grep
~~~
grep -i "HaPPEn" ./technical/911report/preface.txt //display lines with "happen" case insensitive

	      the United States. The nation was unprepared. How did this happen, and how can we
                most complete account we can of the events of September 11, what happened and why.
~~~
This command line displays lines with "happen" case insensitive. This is helpful when you try to find all sentences with certain word.
~~~
grep -c "happen" ./technical/911report/preface.txt  //count the number of "happen"

2
~~~
This command line counts the numbers of the word "happen" in a txt file. This is helpful when you want to find whether if you are overusing a word or not. 
~~~
grep -n "happen" ./technical/911report/preface.txt  // dsiplay lines and line numbers of lines with "happen" case insensitive

12:                the United States. The nation was unprepared. How did this happen, and how can we
84:                most complete account we can of the events of September 11, what happened and why.
~~~
This command line displays lines and line numbers of lines with "happen" case insensitive. This not only helps you to find certain words in a text file, but also where they appear.  

