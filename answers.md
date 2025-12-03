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

For k = -1: no intermediate vertices

    APSP(0,0,-1) = 0
    APSP(0,1,-1) = -2
    APSP(0,2,-1) = 2
    APSP(1,0,-1) = -2
    APSP(1,1,-1) = 0
    APSP(1,2,-1) = 1
    APSP(2,0,-1) = 2
    APSP(2,1,-1) = 1
    APSP(2,2,-1) = 0

For k = 0:

    APSP(0,0,0) = 0 (0->0->0 = 0 + 0)
    APSP(0,1,0) = -2 (0->0->1 = 0 + -2)
    APSP(0,2,0) = 2 (0->0->2 = 0 + 2)
    APSP(1,0,0) = -2 (1->0->0 = -2 + 0)
    APSP(1,1,0) = -4 (1->0->1 = -2 + -2) < 0
    APSP(1,2,0) = 0 (1->0->2 = -2 + 2) <1
    APSP(2,0,0) = 2 (2->0->0 = 2 + 0)
    APSP(2,1,0) = 0 (2->0->1 = 2 + -2) <1
    APSP(2,2,0) = 0 (2->0->2 = 2 + 2) > 0

For k = 1:

    APSP(0,0,1) = -4  (0->1->0 = -2 + -2)
    APSP(0,1,1) = -6 (0->1->1 = -2 + -4)
    APSP(0,2,1) = -2 (0->1->2 = -2 + 0)
    APSP(1,0,1) = -6 (1->1->0 = -4 + -2)
    APSP(1,1,1) = -8 (1->1->1 = -4 + -4)
    APSP(1,2,1) = -4 (1->1->2 = -4 + 0)
    APSP(2,0,1) = -2 (2->1->0 = 0 + -2)
    APSP(2,1,1) = -4 (2->1->1 = 0 + -4)
    APSP(2,2,1) = 0 (2->1->2 = 0 + 0)

For k = 2:

    APSP(0,0,2) = -4 (0->2->0 = -2 + -2)
    APSP(0,1,2) = -6 (0->2->1 = -2 + -4)
    APSP(0,2,2) = -2 (0->2->2 = -2 + 0)
    APSP(1,0,2) = -6 (1->2->0 = -4 + -2)
    APSP(1,1,2) = -8 (1->2->1 = -4 + -4)
    APSP(1,2,2) = -4 (1->2->2 = -4 + 0)
    APSP(2,0,2) = -2 (2->2->0 = 0 + -2)
    APSP(2,1,2) = -4 (2->2->1 = 0 + -4)
    APSP(2,2,2) = 0 (2->2->2 = 0 + 0)

- **2b.**


- **2c.**

- **2d.**

- **2e.**



- **3a.**


- **3b.**


- **3c.**
