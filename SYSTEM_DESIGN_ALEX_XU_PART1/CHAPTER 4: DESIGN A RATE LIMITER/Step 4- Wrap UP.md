##### Step 4: Wrap up

We discussed different algorithms of rate limiting and their pros/cons.

* Token Bucket
* Leaking Bucket
* Fixed window
* Sliding window log
* Sliding window counter


Then further, 
* System architecture
* Rate limiter in distributed environment
* Performance Optimization
* Monitoring

Similar to any system design interview questions, there are additional talking points that can be mentioned if time allows:

* Hard vs soft rate limiting.
     * Hard: The number of requests cannot exceed the threshold.
     * Soft: Requests can exceed the threshold for a short period.
* Rate limiting can be applied at different levels. In this chapter, we only talked about rate limiting at application level (HTTP:layer 7). It is possible to apply rate limiting at other layers.
For example, we can apply rate limiting by IP addtesses using Iptables (IP:Layer 3). Note: The Open Systems Interconnection model (OSI model) has 7 layers, layer 1: Physical Layer, layer 2: Data Link 3. Network 4. Transport 5. Session 6. Presentation 7. Application.

* Avoid being rate limited. Design your client with best practices:
    * Use client cache to avoid making frequent API calls.
    * Understand the limit and do not send too many requests in a short time frame.
    * Include code to catch exceptions or errors so your client can gracefully recover from exceptions.
    * Add sufficient back off time to retry logic.s
