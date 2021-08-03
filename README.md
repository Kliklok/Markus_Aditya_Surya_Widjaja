<!-- CONTACT Section Starts -->
### PROFILE

<!-- Add your details -->
Nationality: Indonesian (Singapore PR)
&nbsp;&nbsp; ✉️: markus.widjaja@yahoo.com
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [LinkedIn](https://www.linkedin.com/in/markus-aditya-surya-widjaja-499b00113/) 

<!-- CONTACT Section Ends -->

<!-- ABOUT Section Starts -->
### ABOUT
<!-- Add link to your picture -->
<!-- Add your details -->

I am __Markus Aditya Surya Widjaja__, a data analyst trainee/ civil engineer with a newfound interest for data analytics. Looking to enter into a more digital and technology-driven field especially those related to science and engineering. An independent and fast learner who is experienced in handling multiple tasks, able to think critically and comfortable with communicating technical content to laymen. Believe in comprehensive problem understanding and clear communication as key drivers of success.

<!-- Add link to the sections -->
[Education](#education) <br>
[Projects](#projects) <br>
[Experience](#experience) <br>
[Skills](#skills) <br> 

<!-- ABOUT Section Ends -->

<!-- EDUCATION Section Starts -->

### EDUCATION
<!-- Add your details -->
##### RISE by BCG (Business and Data Analytics Specialisation)                       
Mar 2021- Sep 2021: 6 months (Ongoing)
- Introduction to TSQL, Python (Pandas, Scikit), PowerBI
- Structured Problem Solving and Agile Framework

##### M.Sc. in Civil Engineering at National University of Singapore (Transportation Engineering Specialisation)			   
Aug 2018 – Jul 2019: 1 year
-	Transportation demand forecasting methods
-	Basic understanding of Vehicular Routing Problem algorithms (VRP)

##### B.Eng (Merit) in Civil Engineering at National University of Singapore	                
Aug 2012 – Jul 2016: 4 years
-	Undergraduate ASEAN Scholarship Recipient

<!-- EDUCATION Section Ends -->

<!-- PROJECTS Section Starts -->
### PROJECTS
<!-- Add your details -->
I'm doing some data related projects to slowly build my portfolio.

#### Visualisation and data wrangling project

###### Formula One: Track & Thrill
A simple passion project on visualising Formula One data to find out where the most exciting race locations are. For fans, teams and drivers alike. A simple dashboard that can serve a starting point to asnwer several business questions such as:<br>
1. Where should the next Formula One race be held to attract the most viewership and revenue?
2. Which circuit need modification to improve the excitement factor of the race?
3. How should we plan the race schedule for the season? 
4. How do we plan our coverage/filler content? Which teams or driver should we focus on in each event?<br>

For the fans, it may give them some insights on:
1. On which circuits can I see more actions? Which races should I watch?
2. Which teams have the most competitive cars? On which circuits?
3. Who are the drivers to look out for?

Tools used: Python (Pandas), Power BI<br>
Dataset: Kaggle.com<br>

The charts below visualise the data of F1 races between 2017 season to 2021 season (up to Austrian GP) by using a slicer for race year. The dataset itself contains race results from 1950 to 2021. <br>

![F1 Most Exciting Circuit V2](https://user-images.githubusercontent.com/85226680/125777723-79830ff1-8586-40fd-b14d-00d635346acd.png)
![Team wins per circuit V2](https://user-images.githubusercontent.com/85226680/125777717-0f8991d9-4063-4576-b977-6e780bde99c5.png)
![Driver wins per circuit V2](https://user-images.githubusercontent.com/85226680/125777719-485835fc-cae2-48d8-8c6a-70ee94317f99.png)
![Shares of points won per circuit](https://user-images.githubusercontent.com/85226680/125777713-4aaf1cd3-603b-400b-bb72-465d42f3d944.png)

Some guiding questions can be asked to set a direction for a continuation of this project:
1. How does pitstop/racing incident affect the ranking?
2. How does the racing weather/ time of the season affect the ranking?
3. Deep dive on each circuit characteristics. How do we profile the circuits? Length/number of straights? slow/medium/fast corners? Length and location of pitlanes? Elevation of tracks?
4. How well does the number of overtakes correlates with the number of viewerships/ticket sales?

Learning points: Wrangling the data frame too much makes the visualisation in Power BI inflexible as the relation between the aggregated values and the different IDs is lost
On the other hand, Power BI is unable to sort values within partition/groupby column, as the 'Top N' filter function is applied before the data aggregation in the chart i.e. instead of showing the constructor with the highest number of win (Top N=1) for each circuit, it is showing the constructor with the highest number of win (Top N=1) throughout ALL circuits and then, its number of win for each respective circuit.

[Click here to view codebase, pbix file and csv datasets](https://github.com/Kliklok/Markus_Aditya_Surya_Widjaja/tree/Projects/F1)

#### A/B testing mini project

###### Cookie Cats Retention Strategy
A mini project done during the RISE program to test the best level for setting the gate of the game. Dataset contained user data with number of rounds played and retention status. <br>

Brief: Cookie Cats is a popular mobile puzzle game where players complete a task and level up. While leveling up, players encounter gates which force players to wait before continue playing or make in game purchases. <br>
Business Problem: Revenue from in-game purchases has been declining over time and total number of active players declining, with players uninstalling the game after playing for a few days.<br>
Hypothesis: players are churning because the first gate encounter at level 30 is too early. A/B test is performed comparing 2 groups of players, one encounter the gate at level 30 and the other, at level 40. <br>

Tools used: Python (Pandas, matplotlib, numpy)
Dataset: Kaggle.com

The two groups are defined as Group A (gate at Level 30) and Group B (Gate at level 40). The sum of number of rounds of game played are checked for normality first by plotting the histogram and qq plot as shown below and shapiro test. All plots and tests indicate that the data is non-normal.
![Normality Checks](https://user-images.githubusercontent.com/85226680/128043661-8f027583-6a60-4b39-b751-1b7f0cba9343.png)

Both groups are then tested for equality of variances with levene test, which shows that the variances are equal. The 2 groups is then tested with mann-whitney U test for 2-tailed test which yield the result below

![Twotailedtest](https://user-images.githubusercontent.com/85226680/128043671-c4d88c57-b40f-415f-8c1a-2f97fe40bcad.png)

Notice that with the 2 tailed test, H1 is rejected. Which means that changing the gate to level 40 would not yield any meaningful improvement. The 2 groups are then also tested for 1-tailed test as the mean of sum of rounds of game played of group A (gate 30) is noticably higher than that of group B (gate 40). Here we can see that for 1 tailed test, we can see that H1 is accepted and that putting the gate at level 30 would give a higher sum of rounds of game played than that of group B.

![Onetailedtest](https://user-images.githubusercontent.com/85226680/128043665-8792653e-b971-4063-8dbd-0d56db838d39.png)

Bootstrap resampling is also done with size of 40000 and 1000 samples for each group to further remove outliers and verify the significance test result above. We can clearly see below that the mean retention rate at both 1 day and 7 day are higher in group A than that of group B

![Retention Rate Distribution](https://user-images.githubusercontent.com/85226680/128043667-8bec1fa9-06ee-4d3c-868e-903b3d95e034.png)

[Click here to view codebase, charts and csv datasets](https://github.com/Kliklok/Markus_Aditya_Surya_Widjaja/tree/main/Cookie%20Cats)

<!-- PROJECTS Section Ends -->

<!-- EXPERIENCE Section Starts -->
### EXPERIENCE
<!-- Add your details -->
##### Web Structures Pte Ltd
Structural Engineer<br>
Aug-2019 to Mar-2021: 1 year 7 Months
Project highlights: HDB Bukit Panjang N6C15, SIT New Punggol Campus

Managed various aspects of different projects which include structural RC and steel analysis and design, underground structure and foundation design, design reports and drawings production and compilation, external works submission, conservation building Addition & Alteration (A&A) works and general project coordination with client, architect and contractor. 

##### KTC Civil Engineering & Construction Pte Ltd
Project Engineer<br>
Aug-2016 to Jun-2018: 1 year 11 Months
Project highlights: LTA Contract T312 Construction of Sungei Bedok Station & Tunnel for Thomson-East Coast Line – Contract Value $418 million

The lead engineer responsible for visualisation design of construction sequence proposals and presentations, the drawing submission tracking lists which was essential in transforming a 2 months submission delay into a 1 month excess supply of approved drawings, the planning and development of utility diversion proposals to reduce utility gaps from 26 to 11 that is critical to excavation safety, coordination of fabrication drawings from 10 different subcontractors and the material reallocation study which reduced wastage and removed 3 months procurement lead time out of project critical path.
<!-- EXPERIENCE Section Ends -->

<!-- FEATURED Section Starts -->
## SKILLS
<!-- Add your details -->
##### Data Analytics Skills 
T-SQL, Python (Pandas, Scikit), Power BI, Statistics, Data Wrangling, Data Reporting, Storytelling, Dashboard Design, Machine Learning, A/B Testing, Hypothesis Testing
##### Engineering Software 
AutoCAD, Etabs, SAFE, Tedds, SAP2000, PLAXIS 2D, SIDRA, VISUM
##### Media Skills
Photography, audio recording & editing
##### Language
Fluent in English and Bahasa Indonesia 

<!-- FEATURED Section Ends -->
