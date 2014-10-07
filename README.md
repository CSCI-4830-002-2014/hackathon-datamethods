## Q1: There are generally 2 situations you'll start from when approaching a question of data: a) You designed and collected the data yourself OR b) You have to work with a data set you've been given access to.  What do you think makes these 2 starting points different?  How might it change what analysis you'll do?

If you're given data, the analysis methods are limited by the availability and schema of the data. Often you decide what is important based on what's available. When you're collecting data, you have to decide what data is necessary and what the most accurate way of collecting it is.
 
 (For the following set of questions we'll assume we're in situation A - you are going to design your own data collection)
 
 ## Q2: What factors go into deciding what data format to use?  Under what circumstances may you use different data types? (i.e., JSON, CSV, Key-Value Store, txt documents)
 [provide response here]
 
CSV and will be better if the data schema will not change over time. If it does, the unstructured nature of JSON and text files would be better if the data schema is going to change. Key-value storing is very fast and helpful for when data is expensive.

 ## Q3: Once you've chosen a format, you'll need to determine fields to capture and store.  A common approach for this involves determining what QUESTIONS you want to ask of your dataset.  For the following examples, please respond with which field(s) your may need to answer the questions needed:
 1. You're working for a company that tracks data on public transportation, you know you'll want to be able to ask "What percentage of a time is a bus/train late?"
 2. You're working for a school district, and you need to be able to help the principal answer the question "Which teachers are most successful at getting students interested in extra-curricular educational activities (e.g., Math Team, Quiz Bowl, Science Olypiad, Robot Building, etc)? 
 3. You're starting a social networking website that helps friends choose what to do on a Friday night, and you need to be able to answer the question, "Who made the suggestion that led to the final decision?"

 ### Answers:
1. Bus Identifier, routes, predicted arrival time, actual arrival time, 
2. Teacher name, Students, Activities per student
3. Authors, Friends, Suggestions, Final Decisions, Time
 
 ## Q4: Now you need to decide how you'll query your data.  What are the costs and benefits of the following options: 
 1. Store the data raw and load it into a Python or JavaScript Shell for analysis.  
 3. Build a webserver and write an API that dumps and queries that data in your database.
 
1. The data will not be stored for a long period of time and can only be analyzed in the moment. The data can be easily analyzed with complex frameworks and is optimal for displaying visualizations in real-time.
2. It is more costly than dumping it into a shell, but the data can be stored permanently across many servers without compromosing time. Complex analysis is difficult due to sharding.
3. It is costly to scale and takes time, but it is optimized for specific use case. Queries can be very complex and data is easy to keep track of. It is more expensive to maintain than NoSQL.
 
 ## Q5: You've now set up your database and have a website with 10,000 users, but have realized that you forgot a much needed field (say, an ID number for each user).  What do you do and how might different database designs have helped this situation?

NoSQL database designs would have made this process easier because new fields could just be added to each object. Otherwise, migrate the data to a new database that has the needed fields.
 
 ---------------
 
 (For this section, you may need to do some online research to answer the questions.)
 
 ## Q6: What is a Baysian Classifier?  What is it used for?
It is a feature/variable that is measured independently of other features. A probable identity/result of an instance composed of many factors can be determined by analyzing the combining the probabilities that each classifier is that identity independently.
 
 ## Q7: What is a simple graph you could generate to check for outliers in a dataset?
A box plot.
 
 ## Q8: What is a Null Hypothesis?
A statement that assumes initially that there is no relationship between two measures of data.
 
 ----------
 
 
 
I COLLABORATED FOR PART TWO AND THREE IN THE FORK OF LOGAN BATES.
 
