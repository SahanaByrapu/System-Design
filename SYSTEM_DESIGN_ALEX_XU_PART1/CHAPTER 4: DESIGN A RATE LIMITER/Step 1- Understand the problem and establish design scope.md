##### Step 1 - Understand the problem and establish the design scope

Rate limiting can be implemented using different alogirthms, each with its pros and cons. The interactions between candidate and interviewer helps to clarify which type of rate limiters we wanted to build.

**Candidate:**   What kind of rate limiter are we going to design? Is it a client side rate limiter or server-side API rate limiter?

**Interviewer:** Great question. We focus on server-side API rate limiter.

**Candidate:**   Does the rate limiter throttle API requests based on IP, user ID or other properties?

**Interviewer:** The rate limiter should be flexible enough to support different sets of throttle rules.

**Candidate:**  What is the scale of the system? Is it built for a startup or a big company with a large user base?

**Interviewer:** The system must be able to handle a large number of requests.

**Candidate:**  Will the system work in a distributed environment? 

**Interviewer:** Yes.

**Candidate:**  Is the rate limiter a separate service or should it be implemented in application code?

**Interviewer:** It is a design decision up to you.

**Candidate:**  Do we need to inform users who are throttled?

**Interviewer:** Yes.

**Requirements:**

* Accurately limit excessive requests.
* Low latency. The rate limiter should not slow down HTTP response time.
* Use as little memory as possible.
* Distributed rate limiting. The rate limiter can be shared across multiple servers or processes.
* Exception handling. Show clear exceptions to users when their requests are throttled.
* High fault tolerance. If there are any problems with the rate limiter (for eg, cache server goes offline), it does not affect the entire system.
  
  