# WolveReview



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <img width="582" alt="wolvereview" src="https://user-images.githubusercontent.com/47559612/86100732-3aea3400-ba87-11ea-8f6f-fea63f964809.png">
  <p align="center">
    <a href="https://wolvereview.herokuapp.com"><strong>WolveReview.com »</strong></a>
        <br />
        <br />
    WolveReview is a website that provides course data including course overview, course reviews and sentiment analysis to students. Data are scrapped from the official University of Michigan subreddit, /r/uofm.
  </p>
</p>

## About The Project

<img width="1370" alt="Screen Shot 2020-06-30 at 4 33 58 AM" src="https://user-images.githubusercontent.com/47559612/86103653-09736780-ba8b-11ea-9b73-f15c4c0a4b07.png">

Every semester, nervous UofM students gather around Reddit, the front page of the internet, to seek guidance for their semester course loads. The most helpful feedback they could find are real reviews from actual students, which are often hard to find. Students intensively search the internet for answers, wasting their valuable time.

WolveReview was built for one reason, to save everyone's time. WolveReview scraps old reddit threads ranging back to 2018 and assorts the scrapped data into a one page.

### Built With

* [Express](https://expressjs.com/) for API
* [Bootstrap](https://getbootstrap.com) for Frontend
* [MongoDB](https://www.mongodb.com/) for Backend

## Usage
### Data Scraping
<img width="532" alt="example" src="https://user-images.githubusercontent.com/47559612/86107890-750c0380-ba90-11ea-9dfd-8a65b9cc4af4.png">
The official University of Michigan subreddit, /r/uofm, hosts a megathread at the beginning of each semester where students can ask about their course loads or any related questions. 

I used [PRAW](https://praw.readthedocs.io/en/latest/index.html), a Python-based Reddit API wrapper, to extract the course question and answers from the reddit metadata. 
### Sentiment Analysis
Sentiment analysis is conducted using [VADER](https://github.com/cjhutto/vaderSentiment)(Valence Aware Dictionary and sEntiment Reasoner), which is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media. VADER classifies each text as positive, neutral, or negative. Sentiment analysis is done for each replies in a question, and the ratio of each positive/netural/negative entries are reflected in the sentiment analysis wheel. 

### Keyword Analysis
Keyword analysis is conducted using [pke](https://github.com/boudinfl/pke), a python-based keyphrase extraction toolkit. Specifically, TextRank method has been used to analyze the assorted text for each courses. The resulting keywords list has been reviewed manually to provide users with accurate information.
