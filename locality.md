# [The Locality Principle](http://web.eecs.umich.edu/~barisk/teaching/eecs582/locality.pdf)

###### Peter J. Denning

---

### What is the Problem? [Good papers generally solve *a single* problem]

Multiprogramming sometimes leads to a sudden collapse called thrashing as the multiprogramming level rises, running upon architecture using virtual memory and paging.

### Summary [Up to 3 sentences]

Locality principle was discovered by trying to solve the thrashing problem. It describes some data clustering properties when running the program in both spatial and time perspectives. It has been widely adopted to different domains in computer science. 

### Key Insights [Up to 2 insights]

- Static analysis upon single program is not going to find out the reason of sudden collapse in multiprogramming. Dynamic testing and static analysis both are important to profile and understand how a system works.
- Data locality is a universal property of not only programs running upon virtual memory and paging architecture, but also systems having components with various capacity and capability. 

### Notable Design Details/Strengths [Up to 2 details/strengths]

- Locality principles greatly speed up the computing process by reuse data in unit with high capability.
- Locality exploitions power up computing in an average speaking level in real world senario instead of having theoretical guarentees.

### Limitations/Weaknesses [up to 2 weaknesses]

- Sometimes, reaching locality might include too much overhead.

### Summary of Key Results [Up to 3 results]

- Virtual memory and paging need to be well scheduled in case of management program using up all the CPU resources.
- Data has features of spatial or temporal locality can be processed much faster due to high frequent reusing data in cach unit.

### Open Questions [Where to go from here?]

- Data locality principle, as one of the most important principles applied to all fields of computer science area, is it highly dependent upon the low level architecture that we have today (which does not change much since 1960). Or is it a more scientific principle in computing neglect of the basic architecture.