# [END-TO-END ARGUMENTS IN SYSTEM DESIGN](http://web.eecs.umich.edu/~barisk/teaching/eecs582/end-to-end.pdf)

###### J.H. Saltzer, D.P. Reed and D.D. Clark*

---

### What is the Problem? [Good papers generally solve *a single* problem]

Some functionalities provided at low levels of a system might have little value compared to the cost of implementing them at such low levels. A new system design principal of end-to-end arguments should be proposed to replace the original designs in certain circumstances in distributed computer systems.

### Summary [Up to 3 sentences]

End-to-end arguments propose that only necessary functions should be provided in a communication subsystems.
Desired functions can be and better be implemented by the users who know the their requirements better.
To justify the arguments, the authors provide case studies on topic include bit error recovery, security using encryption, duplicate message suppression, recovery from system crashes, and delivery acknowledgement.

### Key Insights [Up to 2 insights]

- Implement complex and powerful functions in low levels may be painful for both the users and the developers. For developers, it is hard to write complex and correct program at low level. For users, those with simple requirements have to afford the equal cost as those with higher demands, since the communication subsystems is the same.
- In layered communication protocols, end-to-end arguments can used as a criteria of deciding which layer a function should be assigned to.

### Notable Design Details/Strengths [Up to 2 details/strengths]

- End-to-end arguments enables the simplest implementation for the communication subsystems.
- End-to-end arguments leave the implementation of functions to the users who know the requirements best

### Limitations/Weaknesses [up to 2 weaknesses]

- The end-to-end arguments might not work to certain systems such as speech communication system.
- Implementing functions at higher levels usually have higher cost at performance than implementing it at lower levels.

### Summary of Key Results [Up to 3 results]

- End-to-end arguments provide more simple yet higher performance solution to problems like bit error recovery, security using encryption, duplicate
message suppression, recovery from system crashes, and delivery acknowledgement.
- End-to-end arguments have limitations on certain systems such as real time speech communication system.
- End-to-end arguments provide a criteria to assign functions to layers in layered communication protocols.

### Open Questions [Where to go from here?]

- In this paper, the author provide several use cases for the end-to-end arguments with reasoning the advantages of using such principal. However, it is vague on how simple should the functions at low level be. Simpler implementation at low level is a trade off for better customization and flexibility at higher level, with a cost of performance. Therefore, too simple a implementation at low level will lead to suffering of performance and reimplementation of the same things at high level. Maybe a more detailed criteria should be proposed for the developers to determine the assignment of functions.
