# [Exokernel: An Operating System Architecture for Application-Level Resource Management](http://web.eecs.umich.edu/~barisk/teaching/eecs582/end-to-end.pdf)

###### Dawson R. Engler, M. Frans Kaashoek, and James O’Toole Jr.


---

### What is the Problem? [Good papers generally solve *a single* problem]

The lower the level of a primitive, the more efficient it can be implemented, and the more latitude it grant to implementors of higher-level abstractions. However, there is no secure solutions that expose low level abstractions to the application developers.

### Summary [Up to 3 sentences]

In this paper, the authors offer application developers with low level abstractions of physical resources by building an application level resource management system that separates the protection from the management. The authors first indicate it is very difficult to customize the systems to a particular application with the purpose of optimization. The Exokernel, however, solves this by providing the applications control of resource management and the protection at the same time.

### Key Insights [Up to 2 insights]

- Protection of physical resources in traditional operating system limits the optimization and customization of higher level applications.
- Providing full control of the management at low level is not contradict to providing protection at the same time.

### Notable Design Details/Strengths [Up to 2 details/strengths]

- Multiple library OSes can co-exist in an Exokernel based system which might provide different abstractions upon the same feature. This benefits the application developers a lot since they can manage and optimize the resources better.

### Limitations/Weaknesses [up to 2 weaknesses]

- They indicate simple kernel provides reliability without a proof on that.
- Their conclusion on efficiency is draw on simple kernel while they only provide some of the functionalities with other functionalities to be developed later.

### Summary of Key Results [Up to 3 results]

- A resource management system is beneficial to high level application optimization and management.
- An Exokernel operating system called Aegis that ```1) tracking ownership of resources, 2) ensuring protection by guarding all resource usage or binding points, 3) revoking access to resources.```
- A library operating system called ExOS responsivle for ``` interprogram communications, virtual memory management and manipulating application specific sage handlers.```

### Open Questions [Where to go from here?]

- As indicated in the limitations sections, the authors state a lot of things without proof, i.e. simple kernel providing reliability.
- In this paper, the author only provides simple features in the ExOS, with the others left to be developed. Then, it is hard to prove the efficiency or even practicality.
- OS protection of physical resources, in another way of speaking, is also trying to isolated hardware resources for security concerns. In Exokernel system settings, is it going to be more vulnerable due to more power granted to the application/high level users.
