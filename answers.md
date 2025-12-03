# CMPS 2200 Assignment 4
## Answers

**Name:** Caitlyn Gifford

- **1a.** With n nodes, the maximum depth of a d-ary heap is log<sub>d</sub>n.

- **1b.** In a d-ary heap, the work done by insert is O(log<sub>d</sub>n) and the work done by delete-min is O(d * log<sub>d</sub>n).

- **1c.** The heap size is |V|. 

We perform exactly |V| delete-min operations

O(|V| * d * log<sub>d</sub> |V|)

and up to |E| insert operations.

O(|E| * log<sub>d</sub> |V|)

 Therefore, the new bound on the work is 

 O(|E| * log<sub>d</sub>|V| +  |V| * d * log<sub>d</sub>|V|)

- **1d.** $d = |V|^\epsilon$


- **2a.**


- **2b.**


- **2c.**

- **2d.**

- **2e.**



- **3a.**


- **3b.**


- **3c.**
