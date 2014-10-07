# Hackathon 10/6 - Data Methods and Design

# Team Members

* [Marc Simpson](https://github.com/masi8397)


# Part 1: Data Science Fundamentals


## Q1: There are generally 2 situations you'll start from when approaching a question of data: a) You designed and collected the data yourself OR b) You have to work with a data set you've been given access to.  What do you think makes these 2 starting points different?  How might it change what analysis you'll do?

It depends on your starting point in where you are. If the data is given to you, then you are immediately going into cleaninc and analyzing your data. If You are designing and collecting the data yourself then there are several steps in what you want to collect and how to collect it. Analysis would change because you might be grabbing different data if you are in A, and B you are given data.

(For the following set of questions we'll assume we're in situation A - you are going to design your own data collection)

## Q2: What factors go into deciding what data format to use?  Under what circumstances may you use different data types? (i.e., JSON, CSV, Key-Value Store, txt documents)

Whichever would give you the clearest path in what you need to do to understand the data you collect. If it is structured and consistent data then that would be a reason to use another data type.

## Q3: Once you've chosen a format, you'll need to determine fields to capture and store.  A common approach for this involves determining what QUESTIONS you want to ask of your dataset.  For the following examples, please respond with which field(s) your may need to answer the questions needed:
1. You're working for a company that tracks data on public transportation, you know you'll want to be able to ask "What percentage of a time is a bus/train late?"
2. You're working for a school district, and you need to be able to help the principal answer the question "Which teachers are most successful at getting students interested in extra-curricular educational activities (e.g., Math Team, Quiz Bowl, Science Olypiad, Robot Building, etc)? 
3. You're starting a social networking website that helps friends choose what to do on a Friday night, and you need to be able to answer the question, "Who made the suggestion that led to the final decision?"

### Answers:
1. actual run time, bus/train number, driver
2. students in a specific class who participate in activities, total students, teacher name, course
3. name of suggestor,activities, decision, # of successful/unsuccessful

## Q4: Now you need to decide how you'll query your data.  What are the costs and benefits of the following options: 
1. Store the data raw and load it into a Python or JavaScript Shell for analysis.  
2. Periodically dump the data into a database (like Mongo) and query it.
3. Build a webserver and write an API that dumps and queries that data in your database.

### Answers:
1. Cost: data is dirty, needs to be parsed, write program. Benefit: efficient, no fear of corruption
2. Cost: time consuming, how to load the data. Benefits: collaboration, more benefit storing
3. Cost: Takes time, data restricted to cleaning data. Benefits: automated, perminant storage


## Q5: You've now set up your database and have a website with 10,000 users, but have realized that you forgot a much needed field (say, an ID number for each user).  What do you do and how might different database designs have helped this situation?

Store the data using an identifier. Assign values to specific fields. 

---------------

(For this section, you may need to do some online research to answer the questions.)

## Q6: What is a Baysian Classifier?  What is it used for?

A simple probabilistic classifier based on applying Bayes' theorem (from Bayesian statistics) with strong (naive) independence assumptions.

## Q7: What is a simple graph you could generate to check for outliers in a dataset?

Scatter plot

## Q8: What is a Null Hypothesis?

Statement you want to prove wrong.

----------

Answer the following questions using this scenario: You just got a HUGE dataset from Spotify where each entry contains these fields -> [username, song, # of times played, user rating, genre]

## Q9: How would you figure out the most popular song?

number of times played, merge dupliates.

## Q10: How do you determine what genre a certain user likes the most?

sum of song played by genre.

## Q11: How do we match 2 users that we think may want to share playlists?

compare the most played songs.

## Q12: What assumptions would you have before digging into Spotify data?  How would you test them?

user on the computer vs computer playing songs w/out supervision. The longevity of no activity.

----------

Answer these last questions generally.

## Q12: What is a correlation and how do you find them in a data set?

a similar trend in the data and look for similiar data points.

## Q13: How can correlations help us tell a story with our data? 

you can find what everyone is wanting/likes/what you are trying to find to be able to accomodate what the data says.

## Q14: Let's think about data science as a way to tell a story about some data.  Why would I want to bring a second data set into my story?

To be able to prove what your hypothises is and further approve of what you are trying to do with the data trend.

## Q15: This one's just for fun.  How percent of the time do you expect to actually get the result you wanted?

A long long time, the more time you spend on retrieving your data, the better results you will get.


# Part 2: Analyzing Your Data

# I did not have enough time to get to this, and loading the data took way too long.

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
* [motion sensor board that displays light with movement](http://www.learningaboutelectronics.com/Articles/Arduino-motion-sensor-light-circuit.php)


## What it would measure and how?
Measures your movements and depending on what your movement is it shines a different light.

## Where you'd put it in the lobby?
Right above one of the screens on the south side of the lobby.

## What problems could threaten the validity of your data?
Maybe periods of low movement or how far away someone is to the sensor might get weird results.

## How often to sample and when to make a data dump?
Setting up 6 hour time limit and then that would do a data dump so it wouldnt be an overload, or it would collect very valid data.

## Resulting viz.

* [D3](http://bl.ocks.org/mbostock/3943967)

## Timing trigger
YES. So that the data we collect would be really good and there wouldnt be time where it is dead and it detects like the lights going off or something minor.

