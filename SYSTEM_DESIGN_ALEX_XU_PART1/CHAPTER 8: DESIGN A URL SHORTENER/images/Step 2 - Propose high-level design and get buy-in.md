#### Propose high-level design and get buy-in

**API Endpoints**

API Endpoints facilitate the communication between client and servers. We will design the APIs REST-style. 

A URL shortner primary needs two API endpoints.

1. URL Shortening: To create a new short URL, a client sends a POST request, which contains one parameter: the original long URL. The API looks like this:

