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

- **2b.** It is unchanged going from k=1 to k=2. But ASPS(i,j,2) can be written as min(APSP(i,j,1), ASPS(i,2,1) + APSP(2,j,1)). Because we want to see if the shortest path from i to j does not use vertex 2 as an intermediate, or if it's shorter to use 2 as an intermediate. In this case, using 2 as an intermediate did not make the path shorter.


- **2c.** APSP(i,j,k) = min(APSP(i,j,k-1), APSP(i,k,k-1) + APSP(k,j,k-1)). The shortest path from i to j using vertices {0,...,k} is either the same as the best path when we would only use vertices {0,...,k-1} or it is a path that does include vertex k at least once. In the latter case, we would find the optimal path from i to k, and the optimal path from k to j, and add them. The minimum of these two cases is the shortest path from i to j.

- **2d.** k = -1 to n-1, meaning k has n+1 values. With n choices for i, n choices for j, and n+1 choices for k, total subproblems would be n*n*(n+1) = n*(n^2 + n) = n^3 + n^2 = O(n^3). Each subproblem takes O(1) work, meaning total work is O(n^3).

- **2e.** The dynamic programming algorithm has work O(|V|^3), and Johnson's algorithm runs in O(|V||E|log|E|) work. For sparse graphs with a small |E|, Johnson's algorithm is faster. Dense graphs where |E| is on the order of |V|^2 make the dynamic programming algorithm preferable. 

|V|^3 < |V|*|V|^2*log(|V|^2).

- **3a.**


- **3b.**


- **3c.**
