What we will be designing is a ticket booking system like BookMyShow.

To design a high level diagram for any question, we follow the below steps:

1) Understand the problem statement and scope down the problem.
2) High level design of the system.
3) Design deep dive.
4) Wrap up with improvements.

**1) Understand the problem statement and scope the problem**

1) Would this application be a mobile or web application or both?
Ans: Both, the mobile app as well as a well application.

2) At what scale would this system be? How much of a traffic are we expecting?
Ans: Assume scale to be as big as any other booking apps like BookmyShow etc..

3) In the peak times, do we intend to do somekind of limiting?
Ans: We can think about that.

4) So, we would be storing the information about the theatres, as well as the screens in the theaters and also the number of seats in the theatre.
Ans: Yes.

5) Would we need some logging/ monitoring and telemetrics ?
Ans: We can look at this if the time permits at the end.


For the next steps, look at the HLD diagram that we have come up, in the .drawio file.

**Data Layer Discussion**

We will be using the a combination of the relation database system, as well as a NOSQL database system.
- To store information like the threaters, the location, movies etc.. we can use the relational database system.
- To store information about a particular movie information, the reivews etc.. we can go for non-relational databases since the information such as these would not have any relations.


One thing that we have to highlight here is the ways of locking:
- There are 2 ways of locking in multi threading namely:
- Optimistic locking.
- Pesimistic locking.

**1) Optimistic locking:**
- In optimistic locking, you are optimistic that there would not be a change in the resource that you accessed unless you have commited the changes.
- In the optimistic locking, before you commit your changes you check if the resource you accessed to change is the same state as you took you.
- If in the case where the resource would have changed, you either retry again with the new updated resource or you fail.
- We would more often use optimistic locking in the places where we do not expect a lot of concurrent access to a resource.

**2) Pesimistic locking:**
- In the pesimistic locking we are more strict that only one thread can access a resource and until the thread has completed its execution no other thread would be able to access that particular resource.
- In the pesimistic locking we would be using the a lock which would lock the resource and then finally release it when the activity on that resource is completely done.
- We will be using the pessimistic locking in the cases where we will have more curcurrent access to the resources.