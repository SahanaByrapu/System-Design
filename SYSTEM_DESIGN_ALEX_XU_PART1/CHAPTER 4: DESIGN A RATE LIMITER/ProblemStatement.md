#### DESIGN A RATE LIMITER

In a network system, **rate limiter** is used to limit the traffic sent by the client or a service.
In the HTTP world, a rate limiter limits the number of client requests allowed to be sent over a specified period.
If the API request count exceeds the threshold defined by the rate limiter, all the excess calls gets blocked.

**Here are a few examples:**

* A user can write no more than 2 posts per second.
* You can create a maximum of 10 accounts per day from same IP adress.
* You can claim rewards no more than 5 times a week from the same device.

**Benefits of using an API rate limiter:**

* Prevent resource starvation by **Denial of Service(DOS) attack**: ALmost all APIs published by large tech companies enforce same form of rate limiting. For example, Twitter limits the number of tweets to 300 per 3 hours, Google docs APIs limits to 300 read requests per user per 60 seconds. A rate limiter prevents DOS attacks, either intentional or unintentional, by blocking excess calls.
* **Reduce cost:** Limiting excess requests means fewer servers and allocating more resources to high priority APIs.
 This is important for companies that uses paid third party APIs. For eg, you are charged on a per-call basis for the following external APIs:
check credit, make a payment, retrive health records etc., Limiting the number of calls is essential to reduce the costs.
* Prevent servers from being overloaded. To reduce server load, a rate limiter filter out excess requests caused by botss or user behaviour.


