# Twitter replies scraper
A Python[Selenium] way to scrape replies to a tweet.

Using social media data to sentiment analysis or other NLP related tasks is very common in these days and the very useful data are contained, afaik, 
in tweets/post and replie/comments.
Twitter APIs allow you to download tweets, but does not give you a way to scrapet the replies to a specific tweet: that notebook is here to fix this gap.

## Use

Just fill these fields:

    target_tweet='Full url of the tweet you want to scrape'

    twitter_usr="@your_twitter_username"

    twitter_pass='your_twitter_password'


with your login informations and url of the tweet you want to scrape and execute the full notebook. The scraped replies will be wrapped up in a dataframe.

## Requirements

You only need Selenium, webdriver manager and Pandas:

    pip install selenium
    pip install pandas
    pip install webdriver-manager


## TODO

#### The cookies 'quasi-wall' does note seems to bother the scraping process, but there is the 'acceppt all cookies'

    cookies_btn_xpath='/html/body/div[1]/div/div/div[1]/div/div/div/div/div/div[2]/div[1]/div/span/span'

#### Beyond the 'load more replies' there is some replies containing strong language and other stuff that Twitter does not want you to see. 

Expecially in the case of sentiment analysis and other NLP task those can be very useful. So:
TODO: add the kind of words you mother does not want you to use to the dataset.
