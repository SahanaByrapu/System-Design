#### Step 1 - Understand the problem and establish design scope.

Designing a Google Drive is a very big project, it is important to ask questions to narrow down the scope.

**Candidate:** What are the most important features?
**Interviewer:** Upload and Download files, file sync and notifications.

**Candidate:** Is this a mobile app, web app or both?
**Interviewer:** Both

**Candidate:** Do files need to be encrypted?
**Interviewer:** Yes, files in the storage must be encrypted.

**Candidate:** Is there is a file size limit?
**Interviewer:** Yes, the files must be 10 GB or smaller.

**Candidate:**  How many users does the product have?
**Interviewer:** 10M DAU


**Features to Focus:**

* **Add Files.**  The easiest way is to drag and drop files into Google Drive.
* **Download Files**
*  **Sync** Files across multiple devices. When a file is added to one device, it is automatically synced to other devices.
*  See **file revisions**.
*  **Share** files with your friends, family and coworkers
*  Send **notification** when a file is edited, deleted or shared with you.

**Features not Focused:**

* Google doc editing and collaboration. Google doc allows multiple people to edit the same document simultaneousl.

Apart from clarfiying requirements, it is important to understand **non-functional** requirements.

* **Reliability:** extremely important, Data loss is not acceptable.
* **Fast sync speed:** If file sync takes too much time, users will become impatient and abandon the product.
* **Bandwidth usage:** If a product takes a lot of unnecessary network bandwidth, users will be unhappy, especially when users are on mobile data plan.
* **Scalability:** The system should be able to handle high volume of traffic.
* **High availability:** users should still be able to use the system when some servers are offline, slowed down or unexpected network errors.


**Back of the envelope estimation:**

* Assume the application has 50 million signed up users and 10 million DAU.
* Users get 10 GB space.
* Assume users upload 2 files per day. The average file size is 500 KB.
* 1:1 read to write ratio.
* Total space allocated: 50 million * 10 GB = 500 Petabyte.
* QPS for upload API: 10 million * 2 uploads / 24 hours /3600 seconds = ~240.
* Peak QPS = QPS * 2 = 480.

