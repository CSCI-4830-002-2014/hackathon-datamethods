# Hackathon 10/6 - Data Methods and Design

# Team Members

* [Brian Newsom](https://github.com/briannewsom)
* [Peyman Mortazavi](https://github.com/peymanmortazavi)
* [Adrian Chen](https://github.com/adrian-chen)
* [Dawson Botsford](https://github.com/dawsonbotsford)

# Part 1: Data Science Fundamentals


## Q1: There are generally 2 situations you'll start from when approaching a question of data: a) You designed and collected the data yourself OR b) You have to work with a data set you've been given access to.  What do you think makes these 2 starting points different?  How might it change what analysis you'll do?
You can usually retest the data you collected. 
You know the methodology of collecting data since you collected it yourself and you know how valid it is.
When you are using somebody else's data, you'd want to check the accuracy of it using a known field or something similar.

(For the following set of questions we'll assume we're in situation A - you are going to design your own data collection)

## Q2: What factors go into deciding what data format to use?  Under what circumstances may you use different data types? (i.e., JSON, CSV, Key-Value Store, txt documents)
(1) Compatibility (2) Readibility (3) Size

## Q3: Once you've chosen a format, you'll need to determine fields to capture and store.  A common approach for this involves determining what QUESTIONS you want to ask of your dataset.  For the following examples, please respond with which field(s) your may need to answer the questions needed:
1. You're working for a company that tracks data on public transportation, you know you'll want to be able to ask "What percentage of a time is a bus/train late?"
2. You're working for a school district, and you need to be able to help the principal answer the question "Which teachers are most successful at getting students interested in extra-curricular educational activities (e.g., Math Team, Quiz Bowl, Science Olypiad, Robot Building, etc)? 
3. You're starting a social networking website that helps friends choose what to do on a Friday night, and you need to be able to answer the question, "Who made the suggestion that led to the final decision?"

### Answers:
1. (1) Schedule of buses/trains (2) actual arrival.
2. (1) Teacher, (2) Enrollment, (3) Number of students in the club, (4) national data on club sizes
3. (1) Suggestion (2) Name (3) Number of agreements

## Q4: Now you need to decide how you'll query your data.  What are the costs and benefits of the following options: 
1. Store the data raw and load it into a Python or JavaScript Shell for analysis.  
2. Periodically dump the data into a database (like Mongo) and query it.
3. Build a webserver and write an API that dumps and queries that data in your database.

### Answers:
1. Con: Slow, Pro: easy scripting
2. Pro: It's free and very quick. You can view data as data is coming. Con: More overload of the server.
3. Pro: Easibility of sharing, Con: Slower, needs server so costs more.


## Q5: You've now set up your database and have a website with 10,000 users, but have realized that you forgot a much needed field (say, an ID number for each user).  What do you do and how might different database designs have helped this situation?

If a NoSQL is used, we can simply just start using the new structure since NoSQL allows dynamic structures whereas SQL does not and we'd have to change the structure in database before doing anything.

---------------

(For this section, you may need to do some online research to answer the questions.)

## Q6: What is a Baysian Classifier?  What is it used for?
Bayesian Classifiers are essentially a probability function that allows us to predict the likeliness of something based upon some certain quality or class of qualities.  This means that given some data we can predict it's other contents based on a certain subset.  This is common and helpful in machine learning and training algorithms.

## Q7: What is a simple graph you could generate to check for outliers in a dataset?
Graph the points with a line of best fit through the center. Now you can determine the outliers by removing those farthest from the line.

## Q8: What is a Null Hypothesis? 

A null hypothesis is the hypothesis that there is no correlation between two sets of data.

------

Answer the following questions using this scenario: You just got a HUGE dataset from Spotify where each entry contains these fields -> [username, song, # of times played, user rating, genre]

## Q9: How would you figure out the most popular song?
For each username, add # of times played into a running sum across all users.

## Q10: How do you determine what genre a certain user likes the most?
Sum # of times played for each genre of music and find the largest sum. User rating can also be added into this function for additional complexity.

## Q11: How do we match 2 users that we think may want to share playlists?
Find users that have the at least 2 common genres (based on Q10).  

## Q12: What assumptions would you have before digging into Spotify data?  How would you test them?
Pop songs are played the most, party music is commonly played, certain users contribute most to the play counts. Most commonly played songs and find users total playcounts and compare them to random users.

----------

Answer these last questions generally.

## Q12: What is a correlation and how do you find them in a data set?
We can determine correlation by plotting both data sets and seeing if they increase or decrease together.

## Q13: How can correlations help us tell a story with our data? 
They help us define relationships between certain elements of our data and predict future data.

## Q14: Let's think about data science as a way to tell a story about some data.  Why would I want to bring a second data set into my story?
To find correlations/connections between distinct data.  Ensure that data is accurate and trustworthy.

## Q15: This one's just for fun.  How percent of the time do you expect to actually get the result you wanted?
Dawson 10% - Pessimist
Adrian 30% - Sad optimist

Either way - not as often as one might expect.

# Part 2: Analyzing Your Data

While there are many tools to do this analysis, we will use the JS library Gauss to accomplish this task since everyone should have used it by now.

## Screenshot of Data in Gauss
![screenshot of data in gauss](image.png?raw=true) 

## Most Frequent Value
set.distribution()

{ '0': 2,
'1': 8,
'2': 2,
'3': 2,
'4': 3,
'5': 4,
'6': 4,
'7': 22,
'8': 121,
'9': 3729 }

## Range of data
set.min(), set.max()
[0,9]

## Biggest Change
for (var i = 0; i < set.length; i++) {
    var currentChange = set[i] - set[i-1];
    if(currentChange > biggestChange) { biggestChange = currentChange; }
}

Biggest Change : 4

## Shape of data
Flat line !

## Threshold
3

## Percentage above/below
for ( var i = 0; i < set.length; i++) {
    if(set[i] > 3) { aboveCount++; } else { belowCount++;  }}
var abovePerc = aboveCount/set.length;
var belowPerc = belowCount/set.length;

ABOVE: 0.9964074929432897
BELOW: 0.00359250705671029

## Yes/No + Justification
[Answer and any images/snippets to justify]

# Part 3: Project Design Exercise

## Link to the device or devices you're interested in using
* [IR Distance sensor (x2 per doorway)](http://www.amazon.com/OSEPP-Proximity-Sensor-Arduino-Compatible/dp/B007OCGLVY)
* [Raspberry Pi](http://www.amazon.com/Raspberry-Pi-Model-512MB-Computer/dp/B00LPESRUK/ref=sr_1_1?s=electronics&ie=UTF8&qid=1412645804&sr=1-1&keywords=raspberry+pi)

## What it would measure and how?
[The amount of people walking in the door]

## Where you'd put it in the lobby?
[At the doorways]

## What problems could threaten the validity of your data?
[People walking in groups would be difficult/impossible to differentiate, multiple entrances causes issues if we didn't have one on every entrance.]

## How often to sample and when to make a data dump?
[Sample 10 times a second data dump immediatly. d3 and javascript can handle it]

## Resulting viz.
[Describe or link to example]

## Timing trigger
[Leave the hardware always listening. So trigger would be every time people enter.]

