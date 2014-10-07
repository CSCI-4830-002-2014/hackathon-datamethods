# Hackathon 10/6 - Data Methods and Design

# Team Members

* [Jake White](github.com/jakewhite8)
* [nam](URL to this member's github account)
* [name-of-a-team-member](URL to this member's github account)
* [name-of-a-team-member](URL to this member's github account)
* [name-of-a-team-member](URL to this member's github account)

# Part 1: Data Science Fundamentals


## Q1: There are generally 2 situations you'll start from when approaching a question of data: a) You designed and collected the data yourself OR b) You have to work with a data set you've been given access to.  What do you think makes these 2 starting points different?  How might it change what analysis you'll do?

When the data set is was designed and collected by yourself, you know what questions you might ask and how to gathered data and you are immediately familiar with the data. When working with data you got access to, you have to initially analyze the data and discover how it was collected and designed.

(For the following set of questions we'll assume we're in situation A - you are going to design your own data collection.

## Q2: What factors go into deciding what data format to use?  Under what circumstances may you use different data types? (i.e., JSON, CSV, Key-Value Store, txt documents)

You must factor in what software you are going to be using to work with your data after collection You must also factor in what type of data types you are gathering because different data formats and good for different data types.

## Q3: Once you've chosen a format, you'll need to determine fields to capture and store.  A common approach for this involves determining what QUESTIONS you want to ask of your dataset.  For the following examples, please respond with which field(s) your may need to answer the questions needed:
1. You're working for a company that tracks data on public transportation, you know you'll want to be able to ask "What percentage of a time is a bus/train late?"

2. You're working for a school district, and you need to be able to help the principal answer the question "Which teachers are most successful at getting students interested in extra-curricular educational activities (e.g., Math Team, Quiz Bowl, Science Olypiad, Robot Building, etc)? 

3. You're starting a social networking website that helps friends choose what to do on a Friday night, and you need to be able to answer the question, "Who made the suggestion that led to the final decision?"

### Answers:
1. Schedule arrival time, actual arrival time, bus/train.
2. Teacher, # of students, # of students starting extra-curricular activities.
3. Student, student’s suggestion, student’s final decision, comments, timestamp.

## Q4: Now you need to decide how you'll query your data.  What are the costs and benefits of the following options: 
1. Store the data raw and load it into a Python or JavaScript Shell for analysis.  
2. Periodically dump the data into a database (like Mongo) and query it.
3. Build a webserver and write an API that dumps and queries that data in your database.

### Answers:
1. Simple/cheap to gather the data and then worry about analysis. But not very scalable.
2. Database will keep the data organized better and allow for specific queries. Lots of cost to query many times to discover things.
3. This would be expensive, but best for data consistency. API allows for easy accessibility as well.


## Q5: You've now set up your database and have a website with 10,000 users, but have realized that you forgot a much needed field (say, an ID number for each user).  What do you do and how might different database designs have helped this situation?

With a SQL database, a developer would have to add a column and this would be expensive because of changing the schema. With a NoSQL database like MonogDB, it is very simple to expand the database and just dump the new data in a new field.

---------------

(For this section, you may need to do some online research to answer the questions.)

## Q6: What is a Bayesian Classifier?  What is it used for?

Bayesian Classifier is a probabilistic classifier that is based on the Bayes’ theorem. It is used for probability modeling and applying the Bayes’ theorem to a data set.

## Q7: What is a simple graph you could generate to check for outliers in a dataset?

The best simple graph you could generate to check for outliers in a dataset is a scatterplot because you can easily see a point that is far from the fitted curve.

## Q8: What is a Null Hypothesis?

Null Hypothesis is testing if there is a relationship between two entities.

----------

Answer the following questions using this scenario: You just got a HUGE dataset from Spotify where each entry contains these fields -> [username, song, # of times played, user rating, genre]

## Q9: How would you figure out the most popular song?

The sum of the # of times a song was played and user rating.

## Q10: How do you determine what genre a certain user likes the most?

Average user rating per genre.

## Q11: How do we match 2 users that we think may want to share playlists?

Using the users most popular (most played) songs and matching with other users. Also, matching users favorite genres.

## Q12: What assumptions would you have before digging into Spotify data?  How would you test them?

Assumed that multiple rows for single user and would test that by doing count distinct on that column. We would assume that the data is already well formatted and clean because it is coming from Spotify.

----------

Answer these last questions generally.

## Q12: What is a correlation and how do you find them in a data set?

Correlation is the mutual relationship between two values. You can find them in a dataset by using both values in a visualization or statistics metric and seeing a matching pattern between the two. Can also use covariance. Regression.

## Q13: How can correlations help us tell a story with our data? 

Although correlation does not necessarily imply causation, it can help discover hidden variables.

## Q14: Let's think about data science as a way to tell a story about some data.  Why would I want to bring a second data set into my story?

A second dataset, would add to the sample size and if the story remains the same (results you discover), then it makes it even more accurate and validates your results even more.

## Q15: This one's just for fun.  How percent of the time do you expect to actually get the result you wanted?

10%


# Part 2: Analyzing Your Data

While there are many tools to do this analysis, we will use the JS library Gauss to accomplish this task since everyone should have used it by now.

## Screenshot of Data in Gauss
![screenshot of data in gauss](image.png?raw=true) 

## Most Frequent Value
315

## Range of data
-340 to 318

## Biggest Change
2871 to 2872
diff of 9.4

## Shape of data
steady positive slope, then short and very steep positive slope, and then flat.

## Threshold
At time 2766 and value 50.0

## Percentage above/below
almost 50%

## Yes/No + Justification
Yes, the signal I was looking for is there.

# Part 3: Project Design Exercise

## Link to the device or devices you're interested in using
* [sound sensor](http://www.dx.com/p/arduino-microphone-sound-detection-sensor-module-red-135533#.VDM8TEuWsds)

## What it would measure and how?
It would measure noise/sound level near the sensor.

## Where you'd put it in the lobby?
Right next to the visualization (TV).

## What problems could threaten the validity of your data?
Nothing would threaten the validity of the data.

## How often to sample and when to make a data dump?
Sample every .25 seconds and have a constant feed to the visualization.

## Resulting viz.
The sound level would result in drawing the line of the game. http://www.linerider1.net

## Timing trigger
A loud sound would trigger the data collection to begin because without someone directly interacting with the sensor, the visualization would be boring. A constant sound over a period of one minute would trigger the collection of data to stop.

