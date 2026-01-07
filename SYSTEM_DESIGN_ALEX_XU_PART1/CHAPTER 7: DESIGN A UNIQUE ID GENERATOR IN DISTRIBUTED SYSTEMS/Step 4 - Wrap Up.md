#### Step 4 - Wrap up

* Discussed different approaches to design a unqiue ID generator :
      * multi-master replication
      * UUID
      * Ticket server
      * Twitter snowflake-like unique ID generator.
  
 * If there is extra time at the end of the interview, here are a few additional points:
    * **Clock synchronization:** In our design, we assume ID generation servers have the same clock. This assumption might not be true when a server is running on multiple cores. The same challenge exists in multi-machine scenarios. Network Time Protocol is the most popular solution to this problem.
    * **Section length tuning:** For example, fewer sequence numbers but more timestamp bits are effective for low concurrency and long-term applications.
    * **High availability:** Since an ID generator is a mission-critical system, it must be a highly available.