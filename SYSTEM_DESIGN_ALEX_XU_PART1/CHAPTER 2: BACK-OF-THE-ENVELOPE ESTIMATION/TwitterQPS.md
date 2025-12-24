
Below are the numbers for the purpose of exercise only not real numbers.

**Assumptions:**

* 300 million monthly users
* 50% of users use twitter daily
* Users post 2 tweets per day on average
* 10 % of tweets contain media
* Data is tored for 5 years.

**Estimations:**

**Query per second(QPS) estimate:**
* Daily active users (DAU) = 300 million * 50% = 150 million
* Tweets QPS = 150 million * 2 tweets / 24 hours / 3600 seconds =~3500
* Peek QPS= 2* QPS = ~7000
  
We will only **estimate media storage** here

* Average tweet size:
    * tweet_id 64 bytes
    * text.    140 bytes
    * media.    1 MB
* Media storage: 150 million * 2 * 10% * 1MB = 30 TB per day
* 5-year media storage: 30 TB *365*5 = ~55 PB