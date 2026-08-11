### LOW LEVEL DESIGN (LLD)

""" https://refactoring.guru/design-patterns/python """


| Pattern | Problem                      |
|------------- |-----------------------------|
|Strategy Pattern   |[S.O.L.I.D Principles](LLD/SOLID)
| Observer Pattern | Design Notify-Me Button Functionality |
| Decorator Pattern | Design  Pizza Billing System |
| Factory Pattern | Design  Parking Lot |
| Abstract Factory Pattern | Design  Snake n Ladder game |
| Chain of Responsibility Pattern | Design Elevator System |
| Proxy Pattern | Design Car Rental System |
| Null Object Pattern | Design Logging System|
| State Pattern | Design Tic-Tac-Toe game|
| Composite Pattern | Design BookMyShow & Concurrency handling |
| Adapter Pattern | Design Vending Machine |
| Singleton Pattern | Design ATM|
| Builder Pattern | Design Chess game|
| Prototype Pattern| Design File System|
| Bridge Pattern| Design Splitwise|
| Façade Pattern | Splitwise Simplify Algorithm / Optimal Accounting Balancing |
| Flyweight Pattern | Design CricBuzz / CricketInfo |
| Command Pattern | Design True Caller |
| Interpreter Pattern | Design Car Booking Service like Ola, Uber|
| Iterator Pattern | Design Online Hotel Booking System|
| Mediator Pattern | Design Library Management System|
| Memento Pattern | Design  Traffic Light System|
| Template Method Pattern | Design Meeting Scheduler |
| Visitor Pattern | Design Online Voting System|
|  | Design Inventory Management System|
|  | Design Cache Mechanism|
|  | Design LinkedIn |
|  | Design Amazon |
|  | Design Airline Management System |
|  | Design Stock Exchange System|
|  | Design Learning Management System|
|  | Design a Calendar Application|
|  | Design (LLD) Payment System|
|  | Design (LLD) Chat based system|
|  | Design Food delivery app like Swiggy and Zomato|
|  | Design Community Discussion Platform|
|  | Design Restaurant Management System|
|  | Design Bowling Alley Machine |
| |Design (LLD) Rate Limiter|




### HIGH LEVEL DESIGN (HLD)

| **Theory** |
|-----------------------------|
|  Learn About Network Protocols (TCP, Websocket, HTTP etc.)|       
|  Client-Server Vs Peer 2 Peer Architecture|
|  C.A.P Theorem|
|  Microservices Imp. Design Patterns (SAGA pattern, Strangl|er Pattern)
|  Scale from 0 to Million Users|
|  Design Consistent Hashing|
|  Design URL Shortening|
|  Back of the Envelope Estimation|
|  Design Key-Value Store|
|  SQL vs NoSQL, When to Use Which DB|
|  Design WhatsApp|
|  Design Rate Limiter|
|  Design Search Autocomplete System / Typeahead System|
|  Understand Message Queue , Kafka etc.|
|  What is Proxy Servers|
|  What is CDN|
|  Storage types: |
|  (Block Storage, File Storage, Object Storage (S3) , RAID)|
|  File System |
|  (Google File System, HDFS)|
|  Bloom Filter|
|  Merkle Tree , Gossiping Protocol|
|  Caching|
|  (Cache Invalidation, Cache eviction)|
|  How to Scale Database|
|  Sharding (Horizontal and Vertical)|
|  Partitioning|
|  Replication, Mirroring|
|  Leader Election|
|  Indexing etc.|


| Problems |
|-----------------------------|
| Design Notification System|
| Design Pastebin|
| Design Twitter|
| Design Dropbox|
| Design Instagram|
| Design YouTube|
| Design Google Drive|
| Design Web Crawler|
| Design Facebook News Feed / Newsfeed System |
| Design Ticket Master|
| Design NearByFriends or Yelp|

# Proxy Design Pattern

## Definition
The Proxy Design Pattern provides a surrogate or placeholder for another object to control access to it. This can be useful for various reasons, such as lazy initialization, access control, logging, or monitoring.

## Types of Proxies
1. **Virtual Proxy**: Delays the creation of a resource until it is needed.
2. **Protection Proxy**: Controls access to the original object based on permissions.
3. **Remote Proxy**: Represents an object that is in a different address space.

## Example
```python
class RealSubject:
    def request(self):
        return "RealSubject: Handling request."

class Proxy:
    def __init__(self, real_subject):
        self._real_subject = real_subject

    def request(self):
        # Additional functionality can be added here
        return self._real_subject.request()

# Client code
real_subject = RealSubject()
proxy = Proxy(real_subject)
print(proxy.request())  # Output: RealSubject: Handling request.
```

## Use Cases
- **Lazy Loading**: Load resources only when necessary.
- **Access Control**: Restrict access to certain functionalities.
- **Logging**: Monitor access to the real subject.

## Conclusion
The Proxy Design Pattern is a powerful tool for controlling access to objects and can enhance performance and security in software design.
