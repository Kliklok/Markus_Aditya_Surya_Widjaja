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

I am __Markus Aditya Surya Widjaja__, a Data analyst and civil engineer who advocates the application of data analytics and automation in the construction industry. Passionate in exploring machine learning use-cases for the construction business. Experienced in handling multiple tasks, able to think critically and analytically and comfortable with communicating technical content to laymen. Able to grasp new concepts and skills quickly.

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
Mar 2021- Sep 2021: 6 months (Graduated with Merit) [Credentials here](https://www.credly.com/badges/e4234328-e7b4-461d-953f-8fd0bc6a5f24?source=linked_in_profile)
-	Data manipulation/wrangling, analytics and visualisation
-	SQL, Python (Pandas, Scikit), PowerBI
-	Machine Learning, Capstone project completed with distinction

##### M.Sc. in Civil Engineering at National University of Singapore (Transportation Engineering Specialisation)			   
Aug 2018 – Jul 2019: 1 year
-	Specialisation in Transportation Engineering 
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

#### Multivariate Time Series Prediction

###### Market Price Prediction
A simple project on predicting the market value of Japan Yen (JPY) using VARMA and Long Short-Term Memory (LSTM) deep-learning model.<br>

Brief: Predicting the adjusted close values of "JPY=X" for the next 5 days, using the market data of several funds and other currency from the last 10 years (2011 to September 2021): <br>

Tools used: Python (Pandas, scipy, keras, etc.) <br>

The market data are checked for correlation with JPY data and are converted to their principal components with PCA as shown below <br>
![PCA](https://user-images.githubusercontent.com/85226680/141155931-93b6c064-1402-484b-b919-772aa070ee15.png)

The data from 2011 to 2018 is useed to train the model and the remaining data from 2019 to 2021 is used as test set. The VARMAX model  result is shown below with rmse of 2.336. <br>
![VARMAX](https://user-images.githubusercontent.com/85226680/141155933-b6393b93-a47b-449f-91da-ede4ac1faab2.png)
![VARMAX2](https://user-images.githubusercontent.com/85226680/141155938-5d6fc59d-29b1-4593-8d4a-a2e4c7a9da0f.png)<br>

Using the same train and test set, the LSTM model is used with SGD optimiser. This model improves the rmse to 1.06.<br>
![LSTM](https://user-images.githubusercontent.com/85226680/142771485-6e6ad59e-5ec9-4118-87f2-723dc5982459.png)<br>
The model is then used to predict the values for the next 5 days. <br>
![LSTM Prediction](https://user-images.githubusercontent.com/85226680/142771484-31a16a01-02a3-42be-aa35-5ac233ed8b23.png)<br>

[Click here to view codebase, charts and csv datasets](https://github.com/Kliklok/Markus_Aditya_Surya_Widjaja/tree/main/Multivariate%20Prediction)

#### HR Analytics (BCG RISE Capstone Project)

###### Improving visibility and talent management on a multinational mining company (completed with distinction [credentials here](https://www.credly.com/badges/182236de-b950-4c20-96e9-c66c3e3851ae?source=linked_in_profile))
A final capstone project done during the RISE program to propose solutions to better manage the organisation and provide efficient recommendation to managers on managing employees <br>

Brief: HR leadership has less visibility in the current workforce management process, which caused high dependency on line managers and individual teams. The client is looking for: <br>
1. Visualisation of talent database to enable efficient talent conversation <br>
2. Employee profiling to facilitate talent development and management <br>

Tools used: Python (Pandas, scipy, etc.), Microsoft Power BI

As the project involves real client and employee data, native files and datasets are not shared.

#### A/B testing mini project

###### Cookie Cats Retention Strategy (TOP 2 group [credentials here](https://www.credly.com/badges/21619132-967c-404c-a03a-6744faa1df8a?source=linked_in_profile))
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

<!-- PROJECTS Section Ends -->

<!-- EXPERIENCE Section Starts -->
### EXPERIENCE
<!-- Add your details -->
##### Obayashi Corporation Asia-Pacific Regional Headquarters (APRHQ)
Data Management & Analytics Assistant Manager<br>						  
Jan 2022 – Present

•	Spearheaded the data pipeline setup for monthly project reports for than 30 ongoing APAC projects under 5 different overseas subsidiaries as the first step towards reporting automation and analytics.Led the ongoing study to improve the data collection workflow for multiple pipelines.
•	Led the development of Power BI reports and dashboards to transform and digitalise the company's way of monitoring regional projects.
•	Initiated trials to improve the data collection workflow for multiple pipelines.
•	Collaborated with project management software provider on customising multiple Power BI reports to ensure effective data presentation on site.
•	Created multiple custom visualisations in Power BI using Python language to suit business needs.

##### Web Structures Pte Ltd
Structural Engineer<br>
Aug-2019 to Mar-2021: 1 year 7 Months
Project highlights: HDB Bukit Panjang N6C15, SIT New Punggol Campus

•	Obtained approval from 5 authority agencies (LTA, PUB, HDB, BCA and NParks) for the design, coordination of external drainage and road works.<br>
•	Facilitated 5 concurrent projects in carrying out ad-hoc design items and report consolidation.<br>
•	Clawed back a 2-months delay of RFI and RFA submission response by generating key metrics, providing visibility and maintaining the submission data.<br>
•	Started the detailed design process for the Addition and Alteration (A&A) works of a conservation building which includes the foundation strengthening in preparation for authority submission.<br>
•	Accommodated Qualified Person (QP) for the inspection, verification design, drawing production and report submission of retention works to BCA.<br>
•	Maintained coordination with client, architect, contractor, M&E consultants and project site staff to generate solutions for site issues.<br>

##### KTC Civil Engineering & Construction Pte Ltd
Project Engineer<br>
Aug-2016 to Jun-2018: 1 year 11 Months
Project highlights: LTA Contract T312 Construction of Sungei Bedok Station & Tunnel for Thomson-East Coast Line – Contract Value $418 million

•	Transformed a 2-months submission delay into a 1-month excess supply of approved drawings by initiating and maintaining drawing submission tracking lists.<br>
•	Reduced utility gaps from 26 to 11 and improve the excavation safety by spearheading the planning and development of a diversion proposal to 4 utility agencies (Singtel, PUB water, PUB sewer and SP).<br>
•	Removed 3 months procurement lead time out from potential project critical path and reduce wastage by identifying the opportunity for material reallocations.<br>
•	Designed visualisation for construction sequence proposal and presentation.<br>
•	Managed the production and development of fabrication drawings with more than 10 subcontractors via weekly alignment meetings to ensure efficient site coordination and timely approval.<br>
•	Administered the development and coordination of design matters which consist of deep foundation elements, deep excavation, drain diversion and traffic diversion for site feasibility.<br>

<!-- EXPERIENCE Section Ends -->

<!-- FEATURED Section Starts -->
## SKILLS
<!-- Add your details -->
##### Data Analytics Skills 
SQL, Python (Pandas, Scikit), Power BI, Power Query, Power Automate, Statistics, Data Wrangling, Data Reporting, Storytelling, Dashboard Design, Machine Learning, A/B Testing, Hypothesis Testing
##### Engineering Software 
AutoCAD, Etabs, SAFE, Tedds, SAP2000, PLAXIS 2D, SIDRA, VISUM
##### Media Skills
Photography, audio recording & editing
##### Language
Fluent in English and Bahasa Indonesia 

<!-- FEATURED Section Ends -->
