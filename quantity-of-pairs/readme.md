### Task:
Given 4 natural numbers: $x_1, x_2, x_3, x_4$;
Calculate how many pairs ($x_1, x_2, x_3, x_4$) exist such as $x_1 + x_2 + x_3 + x_4 = k$, where k - any natural number;

### Solution
Let we have some number of pairs ($x_1, x_2, x_3, x_4$), sum of all elements in each pair equals to k. 
Divide pair of 4 elements into 2 pairs: $(x_1, x_2)$ and $(x_3, x_4)$. Let $S_1 = x_1 + x_2$, $S_2 = x_3 + x_4$. Obviously that $S_1 + S_2 = k$, so our task could be simplified: we should calculate, how many pairs of numbers $S_1$ and $S_2$ with sum = k exists, and then calculate, in how many ways numbers $S_1$ and $S_2$ could be formed from other natural numbers.
If $S_1 = a$, then $S_2 = k - a$. Number of pairs $(x_1, x_2)$ such that $x_1 + x_2$ = a equals to a + 1, so:

![image](https://github.com/vladstudennikov/cpp-projects/assets/91913216/b43ad2ff-cbab-495d-9e17-c5186af6cc70)

![image](https://github.com/vladstudennikov/cpp-projects/assets/91913216/424dedd2-aa20-4f67-b912-a2fbc9b1b86e)

Conclusion: for fixed number $S_1 = a$ there are (a + 1)(k - a + 1) variants to choose 2 pairs of numbers with sum of all elements equals to k. But "a" could be any number from 0 to k, so using combinatoric laws we can get next formula for calculating  the number of all pairs ($x_1, x_2, x_3, x_4$) with sum = k:

![image](https://github.com/vladstudennikov/cpp-projects/assets/91913216/414bfd38-588e-441d-9010-58b71d0b354c)

