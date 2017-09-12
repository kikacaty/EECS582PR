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

- UberTrace, which is the end-to-end request tracing component that Mystery Machine relies on, uses sampling to reduce overhead. However, sampling reduces the probability that individual logging systems monitor the same set of requests. In order to perform targeted request monitoring, UberTrace propagates the decision about whether or not to monitor a given request through all logging subsystems along the path of the request.
- A key strength of The Mystery machine is that it discovers and updates dependencies in a request automatically. This is a key feature because the underlying logging infrastructure is constantly evolving.

### Limitations/Weaknesses [up to 2 weaknesses]

- The Mystery Machine could recompute model changes incrementally rather than from scratch to account for the changes in the request model.
- The Mystery Machine makes the assumption that the segments in a call graph are acyclic. It is unclear how the system design would need to be changed in the presence of cycles (e.g., what happens when the same <event, task> pair appear more than once in a request trace).

### Summary of Key Results [Up to 3 results]

- There is significant variation in the contribution of major end-to-end performance components (servers, network, and client) to the critical path. One can use this variation to provide differentiated service (e.g., prioritizing service where the server has no slack, whereas deprioritizing those where network and client latency will likely dominate).
- Slack tends to remain stable for a given user across multiple Facebook sessions, so past slack information can be used to predict the slack of the current connection.

### Open Questions [Where to go from here?]

- The performance properties analyzed by the Mystery machine are fairly high-level. One interesting direction would be to extend this work to gather more information in a targeted way to do more low-level performance debugging (e.g., what code is responsible for the slow down?).
- The scope of the work can be extended to look into end-to-end performance analysis for mobile platforms in addition to the desktop.
