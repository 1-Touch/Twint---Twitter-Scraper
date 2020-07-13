
Twint is an advanced Twitter scraping tool written in Python that allows for scraping Tweets from Twitter profiles without using Twitter's API.

Twint utilizes Twitter's search operators to let you scrape Tweets from specific users, scrape Tweets relating to certain topics, hashtags & trends, or sort out sensitive information from Tweets like e-mail and phone numbers. I find this very useful, and you can get really creative with it too.

Twint also makes special queries to Twitter allowing you to also scrape a Twitter user's followers, Tweets a user has liked, and who they follow without any authentication, API, Selenium, or browser emulation.

tl;dr Benefits
Some of the benefits of using Twint vs Twitter API:

Can fetch almost all Tweets (Twitter API limits to last 3200 Tweets only);
Fast initial setup;
Can be used anonymously and without Twitter sign up;
No rate limitations.
Limits imposed by Twitter
Twitter limits scrolls while browsing the user timeline. This means that with .Profile or with .Favorites you will be able to get ~3200 tweets.

Git:

git clone https://github.com/twintproject/twint.git

cd twint

pip3 install . -r requirements.txt

Pip:

pip3 install twint

or

pip3 install --user --upgrade 

git+https://github.com/twintproject/twint.git@origin/master#egg=twint


Pipenv:


pipenv install git+https://github.com/twintproject/twint.git#egg=twint

Basic Examples and Combos.

A few simple examples to help you understand the basics:

twint -u username - Scrape all the Tweets from user's timeline.

twint -u username -s pineapple - Scrape all Tweets from the user's timeline containing pineapple.

twint -s pineapple - Collect every Tweet containing pineapple from everyone's Tweets.

twint -u username --year 2014 - Collect Tweets that were tweeted before 2014.

twint -u username --since 2015-12-20 - Collect Tweets that were tweeted since 2015-12-20.

twint -u username -o file.txt - Scrape Tweets and save to file.txt.

twint -u username -o file.csv --csv - Scrape Tweets and save as a csv file.

twint -g="48.880048,2.385939,1km" -o file.csv --csv - Scrape Tweets from a radius 
of 1km around a place in Paris and export them to a csv file.

twint -u username -es localhost:9200 - Output Tweets to Elasticsearch

twint -u username -o file.json --json - Scrape Tweets and save as a json file.

twint -u username --database tweets.db - Save Tweets to a SQLite database.

twint -u username --followers - Scrape a Twitter user's followers.

twint -u username --following - Scrape who a Twitter user follows.

twint -u username --favorites - Collect all the Tweets a user has favorited.

