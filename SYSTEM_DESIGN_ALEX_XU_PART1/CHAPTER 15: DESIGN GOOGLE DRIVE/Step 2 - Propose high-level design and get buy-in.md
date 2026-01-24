### Step 2 - Propose high-level design and get buy-in.

Instead of showing high-level design view, we will start with simply building a single server and later dive into the concept of  scaling the system to milions to users.

lets start with a single server setup now:

* A web server to upload and download files.
* A database to keep track of metadata like user data, login info, files info etc.,
* A storage system to store files. We allocate 1 TB of storage space to store files.

Apache web server, MySQL database and diectory called drive/ as root directory to store uploaded files.

Under drive/ directory, there is a list of directories, known as namespaces. 
