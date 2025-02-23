## Subset Sum Enumeration – An Interesting Approach  

Given a set of integers S and a target sum T, the goal is to determine whether there exists a subset of S whose sum equals T.  

An intriguing variation of this problem is not just to check for existence of such a subset but to enumerate all possible subsets whose sum is exactly T.

We will focus our discussion on the set of the first N natural numbers. Therefore, our set $S_n$ will consist of the integers from 1 to n, represented as:  

$$ S_n  = \lbrace 1, 2, 3, ... , n \rbrace $$

#### Example  
Consider the set  S = \{1, 2, 3, 4, 5\}  and the target sum T = 5 . The subsets that sum to 5 are:  

-  \{1, 4\} 
-  \{2, 3\}  
-  \{5\}  

### Lexicographical Ordering

To systematically enumerate subsets, we define a **lexicographical ordering** on subsets. Given two subsets A and B, we say that A is **lexicographically smaller** than B if one of the following conditions holds:  

1. A is a **proper prefix** of B, meaning all elements of A appear at the beginning of B.  
2. There exists an index i where A and B differ for the first time, and the i-th element of A is smaller than the i-th element of B.  

#### Example  

Consider the set S = {1,2,3,4,5} and its subsets:  

{% raw %}

$$ A = \lbrace 1,3 \rbrace, B = \lbrace 1,4 \rbrace, C = \lbrace 2,3 \rbrace $$
<!-- $$ A = \lbrace 1,3 \rbrace, B = \lbrace 1,4 \rbrace, C = \lbrace 2,3 \rbrace \$$ -->

{% endraw %}

- A is lexicographically smaller than B because they first differ at index 2, where 3 < 4.  
- B is lexicographically smaller than C because they first differ at index 1, where 1 < 2.
- A is lexicographically smaller than C because they first differ at index 1, where 1 < 2.  

Thus for the set  S = \{1, 2, 3, 4, 5\}  and the target sum T = 5 . The subsets that sum to 5 in lexicographical order are :  

- \{1, 4\} 
- \{2, 3\} 
- \{5\}


