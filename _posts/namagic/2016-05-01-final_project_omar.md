---
author: namagic
layout: post
title: "Omar's Final Project"
---

Here is my delayed Friday update
<iframe src="https://trinket.io/embed/python3/946209e5a5" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Here is my final project
<iframe src="https://trinket.io/embed/python3/78d6646930" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

In this final project, I believe much of what I have learned this semester was put to the test. Using definite loops, while loops, nested functions, nested if statements, and even a little bit of API work. For this final project, I chose to work on a project that I could use for my work at the Development Finance Initiative. By capturing inflow and outflow data via IRS tax migration data, I can determine the aggregated income levels for those moving in and leaving a county. It is helpful to show our clients this information so that they can get a sense of what is happening in their county. Throughout this course, the two major themes that persisted are project planning and debugging. And in this final project, both persisted, but my attitude towards the latter definitely improved after having this opportunity to take on a project that applies to my work outside of this course.
	
From the beginning of this project, I had a clear idea of exactly what I intended to produce and I think one major planned takeaway from this final project is this idea of systematically working towards a final product. Since I had a clear idea, I knew how to break it up appropriately. Through the creation of milestones and using milestones as a living document, I can more thoroughly approach the larger goals. Prior to this course, this was not anything I had honestly fully attempted. For any project or assignment I have, I usually just dive in. For the most part, this method has worked really up and until this semester. Not only with this course but work, I am finally buying into this idea of milestones and project planning even though it already seems obviously important.
	
Although I created my plan, I was consistently behind my own self-imposed deadlines. I would attribute much of me being behind to underestimating the challenges imposed with using the csv module. However, using the milestones, I generally worked on this assignment on a daily basis. The days that I did not put in extensive effort, I was usually reading more on the csv documentation. I had used the documentation prior, but this was really the first time that I needed to understand a module more thoroughly. Whether I was reading the csv documentation, stackoverflow, or even reddit. What was most useful though was the documentation. The other sources helped guide my reading of the csv documentation though. The milestone approach definitely eased my work because I could focus on much smaller chunks at a time. 
	
As something I have heard consistently throughout this course, there are always bugs and always way to improve upon code. I was unfortunately unable to complete what turned out to be my hardest task, manipulating two csv documents simultaneously. I wanted to be able to subtract inflow and outflow information. Both csv files had the same headers, but this one piece I could not end up debugging. While I ended up being able to manipulate both simultaneously, the net migration variable kept printing out 0 when it was definitely not 0 (see line 205 in current.py). This inability to solve this problem led to drastically less powerful visuals.
	
To debug, it was a lot of googling and printing statements at various points. I believe most of my errors had to do with operating with lists inside of dictionaries or dictionaries inside of dictionaries. 
	
The largest hurdle I faced was dealing with the csv module. From realizing that all my code had to live under “with open” to learning about DictReader, I spent a lot of time playing around with the module to get what I wanted to print. Value errors popped up quite a bit which I solved with try/except statements. Key Errors were also pretty common. However, as I got further into this program, debugging became more challenging because of all the nesting. I was nesting if statements, for loops, and try/except statements and depending on where I placed those, I would either solve something or create new errors.

Although not a milestone, I realized that my outflow file had commas in the returns, exemptions, and agi columns. I thought this would relatively simple to fix, but I could not get passed this. I had to manipulate my data in excel. My closest attempt is found on line 20 in current.py. I learned for one that I could open two different csv files in the same line which would have cleaned up a good bit of my code. How it was supposed to work: my infile csv would be read and manipulated which would then be written into an outfile which would replicate the infile and have removed the commas.
	
Generally speaking, I was hoping to accomplish more particularly in the inability to calculate net numbers. If I could go back, I would have started on this aspect much earlier. I thought once I had figured out how to print my inflow and outflow numbers that printing out net flow would be simple. In fact, my original intent was to create a new csv file with the net flow numbers; however, this fell back to just being able to print them. Unfortunately I was not able to do either. In regards to the planning process, this is something I should have accounted for earlier as I was realizing that getting my inflow and outflow numbers to print already had provided a challenge. 
	
Another point in case in regards to project planning, I thought the visualization would come easy. And I think it would have been easy had I been able to figure out to create a net flow csv file. However I was getting lost in the nested functions, for loops, and returns in for loops to be able to get the value I was seeking. In this process, I continued to get some of the same errors that had halted my program previously. So at this point, my visual is a bland set of asterisks that actually is not printing out the needed information because I do not fully understand what is occurring with reader.next(). I think diagramming out the various loops in my project would be fruitful.

While I am not fully happy with my final project, I will say that this was by far my most enjoyable project throughout this course. Even though I could not execute my full plan, my attitude throughout this project was certainly better. Funnily, my frustration went to its greatest lows but its greatest highs. When I got code to execute properly, I was thoroughly elated. 

My greatest takeaway on this project however remains in the realm of project planning. Moving forward, I need to do a much better job determining how long something will take to do. And this does not apply only to my work in this course, but in general. I almost always underestimate how long it will take me to do something, so this course and this project embodied that general trend for me. I understand now why companies run an agile system. It forces you to break your goals down to manageable levels and prioritize the ones that need to get done. I placed too many of my important milestones nearer the due date which did not leave me enough time to readjust. Plus, no where in my milestones was I able to account for the time it would take me to learn the csv module let alone implement it properly. While I could have made my data a text file instead and used methods we learned in the course, I know moving forward, I use so much csv data, that this csv module provided a greater learning experience for me even though I could not fully execute. 

Having the opportunity to make a project directly applicable to work provided further motivation and generally got me more interested in Python. I am happy that I was able to tackle a new module even though I still do need a lot more work in it to become proficient. Moving forward I do plan on attending project nights so I could fully flesh out this project. Besides missing out on some of my milestones (not getting net flow, poor visuals), I also realized that this project would be beyond perfect if I could implement this in Excel. So that all a user has to do is enter in a county and an excel sheet automatically populates the needed information and creates the charts. I am not sure how adventurous that is, but getting help at the project nights will provide an additional boost for my eventual plan. In addition to project nights, I am going to actually create a stackoverflow account so I can post my own questions because I have read through so many stackoverflow posts that are somewhat near what I am attempting to do, but still far enough away to where I do not have the requisite logic in my code to execute. I enjoyed working on this project and am looking forward to this summer and the upcoming project nights to continue working on this project!