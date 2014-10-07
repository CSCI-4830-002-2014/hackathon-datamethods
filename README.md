# Hackathon 10/6 - Data Methods and Design

# Team Members

* [Alexia Newgord](https://github.com/alne4294)             
* [Jake Charland](https://github.com/jakecharland)
* [Alex Tsankov](https://github.com/antsankov)
* [Michael Aaron](https://github.com/develra)

# Part 1: Data Science Fundamentals


## Q1: There are generally 2 situations you'll start from when approaching a question of data: a) You designed and collected the data yourself OR b) You have to work with a data set you've been given access to.  What do you think makes these 2 starting points different?  How might it change what analysis you'll do?

If you receive data that you haven't collected yourself, it is important to do an initial investigation to better understand it. It may also be faster to get started in the initial stages. Conversely, if you collect the data itself, you may have the opportunity to re-collect it if there were any problems with it.  Furthermore, if you do the collect the data itself, it may be inheritantly "cleaner" since the entire design is by a single individual and problems may be addressed early on.

## Q2: What factors go into deciding what data format to use?  Under what circumstances may you use different data types? (i.e., JSON, CSV, Key-Value Store, txt documents)

Factors to consider are:
* End-goal use cases - For example, where is the data going to be stored
* Relationship between data sets - JSON or NoSQL may be better for nested or hierarchical data. SQL is better and faster for relational database formats (where you can use joins, parallelization, etc. across columns).
* Data size - Extremely large data sets may be better processed using SQL databases, while smaller datasets may only need a single .csv spreadsheet.
* Data access - For example, if the same queries are called over and over again, a data store system that supports cacheing would be ideal

## Q3: Once you've chosen a format, you'll need to determine fields to capture and store.  A common approach for this involves determining what QUESTIONS you want to ask of your dataset.  For the following examples, please respond with which field(s) your may need to answer the questions needed:
1. You're working for a company that tracks data on public transportation, you know you'll want to be able to ask "What percentage of a time is a bus/train late?"
2. You're working for a school district, and you need to be able to help the principal answer the question "Which teachers are most successful at getting students interested in extra-curricular educational activities (e.g., Math Team, Quiz Bowl, Science Olypiad, Robot Building, etc)? 
3. You're starting a social networking website that helps friends choose what to do on a Friday night, and you need to be able to answer the question, "Who made the suggestion that led to the final decision?"

### Answers:
1. Expected arrival, actual arrival time, type of transit
2. Student activities, classes, teacher names, teacher's students, number of activities the student is involved in
3. Final decision, authors of suggestions, timestamp

## Q4: Now you need to decide how you'll query your data.  What are the costs and benefits of the following options: 
1. Store the data raw and load it into a Python or JavaScript Shell for analysis.  
2. Periodically dump the data into a database (like Mongo) and query it.
3. Build a webserver and write an API that dumps and queries that data in your database.

### Answers:
1. Costs: limited memory (not scalable), Benefits: low overhead to get started
2. Costs: overhead to dump data and database management, querying and comparisons require more steps, Benefits: relatively easy to query
3. Costs: transfer over network and hacking risks and maintaining web server/requests, Benefits: Easily accessible for many users


## Q5: You've now set up your database and have a website with 10,000 users, but have realized that you forgot a much needed field (say, an ID number for each user).  What do you do and how might different database designs have helped this situation?

Sometimes, you can concatenate different fields to make a unique field for users.  For SQL databases, you may need to rebuild the database by adding the field when migrating the old data to a new location. Alternatively, with many NoSQL databases, you can add a new field/column and populate it.

---------------

(For this section, you may need to do some online research to answer the questions.)

## Q6: What is a Baysian Classifier?  What is it used for?
This minimizes the probability of misclassification by using the Machine Learning strategy where the classifier is trained to identify a particular category based on past behavior. Unlike a naive classifier (which treats every event as independent), a good Baysian Classifier continues to learn throughout time.

## Q7: What is a simple graph you could generate to check for outliers in a dataset?
Histogram or Scatter plot


## Q8: What is a Null Hypothesis?
The null hypothesis is the hypothesis that "there is no significant difference between specified populations" and that "any observed difference being due to sampling or experimental error."

----------

Answer the following questions using this scenario: You just got a HUGE dataset from Spotify where each entry contains these fields -> [username, song, # of times played, user rating, genre]

## Q9: How would you figure out the most popular song?
Depending on your definition of popular, you could find the song that was played by the most unique users or the song that was played the most number of times.

## Q10: How do you determine what genre a certain user likes the most?
You would calculate the most popular genre based on the songs that he/she currently listens to.  You can also look at the distribution of genre and user rating.

## Q11: How do we match 2 users that we think may want to share playlists?
Compare two users' earlier activity (genre, user rating, etc.).

## Q12: What assumptions would you have before digging into Spotify data?  How would you test them?
There may be a difference between popularity of songs on Spotify and outside of Spotify.  There are no duplicate entries. Make a hypothesis and then check to see if it is true (deductive reasoning).

----------

Answer these last questions generally.

## Q12: What is a correlation and how do you find them in a data set?
You can look for positive/negative correlations (using covariance or regression models) or plot to identify general trends.

## Q13: How can correlations help us tell a story with our data? 
You can relate different fields together and possibly make inferences on the rationale behind it.  These correlations can help justify a hypthosesis.

## Q14: Let's think about data science as a way to tell a story about some data.  Why would I want to bring a second data set into my story?
You want to confirm that hypotheses hold up for complimenting data sets as well.  This may help conclusions to be generalized and add complexity to the theory.

## Q15: This one's just for fun.  How percent of the time do you expect to actually get the result you wanted?
65.666662%.  It depends on the circumstances and what stage of the process you are in.


# Part 2: Analyzing Your Data

While there are many tools to do this analysis, we will use the JS library Gauss to accomplish this task since everyone should have used it by now.

## Screenshot of Data in Gauss
![screenshot of data in gauss](image.png?raw=true) 

## Most Frequent Value
[cut and paste command used and the output it produced]

## Range of data
[cut and paste command used and the output it produced]

## Biggest Change
[cut and paste command used and the related snippet from the output]

## Shape of data
[Describe]

## Threshold
[Value]

## Percentage above/below
[Command and output]

## Yes/No + Justification
[Answer and any images/snippets to justify]

# Part 3: Project Design Exercise

## Link to the device or devices you're interested in using
* [Infrared Proximity Sensor Long Range - Sharp GP2Y0A02YK0F](https://www.sparkfun.com/products/8958)
* [Electret Microphone Breakout](https://www.sparkfun.com/products/9964)

## What it would measure and how?
* "Infrared proximity sensor made by Sharp. Part # GP2Y0A02YK0F has an analog output that varies from 2.8V at 15cm to 0.4V at 150cm with a supply voltage between 4.5 and 5.5VDC."  Senses objects up to 5 feet away.
* "This small breakout board couples a small electret microphone with a 100x opamp to amplify the sounds of voice, door knocks, etc loud enough to be picked up by a microcontroller’s Analog to Digital converter."

## Where you'd put it in the lobby?
We would put it near the projector so that there is a dialogue between individuals and the visualization.

## What problems could threaten the validity of your data?
Noise (literally background noise). Longevity of the devices.

## How often to sample and when to make a data dump?
You would sample when the measurements are being taken.  We would data dump whenever needed (before overflow).

## Resulting viz.
We can modify size and colors of some sort of graphic while proximity and sound measurements are being taken.  We could also use a map to identify locations within the lobby from which measurements are being collected.

## Timing trigger
Unnecessary because we would like constant collection.  The proximity sensor may serve as a trigger.

