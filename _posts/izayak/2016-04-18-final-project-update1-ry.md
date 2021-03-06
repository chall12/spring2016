---
author: izayak
layout: post
title: "Ruotong's Final Project Update 1"
---

In my plan, I want to build a dictionary of list of dictionaries, like a tree structure. The top is the 6 airlines, the second level are sentiment, negative reasons and tweets etc., and the third level are sentiments and negative reasons' counts.   
At first I wanted to include content of tweets together, but after trying loaded the data in two ways (copy and paste and upload), the tweets' materials cann ot be handled well, there are always errors. This is not anticipated.  
1) For the location column, the comma can be handled as " " will be added automatically. But for tweets it will not.  
2) Lots of lines of tweets will use more than one lines. And after fixing those one by one which is quite cumbersome and time-consuming (*is there a better way to deal with it?*) the file still will not work i.e. errors exist.  
So then I deleted the tweets column and some other information that I am not interested in such as location and time zone and upload this newly file to cloud 9. Now the file can work well.   
I have worked out one dictionary of lists of dictionaries. And I plan to finish basic descriptive statistics analysis about this dictionary. And after that is done, I want to try to finish one visualizaion tryout. If have time, I will try to work with tweets. Now I am thinking part tweets with one airlines and sentiment separately, hope it will be easier to deal with the data cleaning and loading.


*Milestones*  

- [x] (new1) Set up cloud 9  
- [x] (new1) Load data file (part: loaded concised version of one data file)  
- [ ] (new1) Data cleaning (part: tried data cleaning)  
- [x] (new1) Build lists and dictionaries to get information from the data (part: built nested dictionaries, also need dictionaries of negative reason and airlines etc. separately)  
- [ ] (new1) Make readable tables based on dictionaries, thinking of alignment  
- [ ] Try one simple descriptive statistics calculation and do visualization on a particular data file (In my mind the first try would be calculation the total number of complaints towards different airlines in data file airline.csv, and make a histogram.)  
- [ ] Do more descriptive statistics analysis such as summary statistics (max, min, mean, etc.)   
- [ ] Think more ways to do data visualization through text printouts  
- [ ] (new1) Before using regex with tweets, find a way to make tweets' materials loaded successfully  
- [ ] Use regex to deal with texts (i.e. tweets in airline.csv and gopdebate.csv)  
- [ ] Use functions to make some parts of the program concise  
- [ ] Generalize the program to make it work for different data files: make some variables flexible; add conditionals; let the user input which columns map to what kind of data etc.  
- [ ] Make a text-based interface  
- [ ] Add help text (think of in what way to achieve that)  
- [ ] The user should be able to perform any number of supported actions and then exit the program  
- [ ] Check if the program is well-formatted (comments, organized, readable), error and bug free  

