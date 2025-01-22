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
