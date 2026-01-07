**Step1 - Understand the problem and establish design scope**

Asking clarification questions is the first step to tackle any system design interview question.

**Candidate:** What are the characteristics of unique IDs?
**Interviewer:** IDs must be unique and sortable.

**Candidate:** For each new record, does ID increment by 1?
**Interviewer:** The ID increments by time but not necessarily only increments by 1. IDs created in the evening are larger than those created in the morning on the same day.


**Candidate:**  Do IDs only contain numerical values?
**Interviewer:** Yes, that's correct.


**Candidate:**  What is the ID length requirement?
**Interviewer:** IDs should fit into a 64-bit.

**Candidate:**  What is the scale of the system?
**Interviewer:** The system should be able to generate 10,0000 IDs per second.

It is important to understand the requirements and clarify ambiguities. For this interview question, the requirements are listed as follows:

* IDs must be unique and sortable.
* ID's must be numeric
* ID's must fit into 64-bit
* Ability to generate over 10,000 unique IDs per second.
