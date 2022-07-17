# Twist-the-Permutation

Petya got an array 𝑎 of numbers from 1 to 𝑛, where 𝑎[𝑖]=𝑖.

He performed 𝑛 operations sequentially. In the end, he received a new state of the 𝑎 array.

At the 𝑖-th operation, Petya chose the first 𝑖 elements of the array and cyclically shifted them to the right an arbitrary number of times (elements with indexes 𝑖+1 and more remain in their places). One cyclic shift to the right is such a transformation that the array 𝑎=[𝑎1,𝑎2,…,𝑎𝑛] becomes equal to the array 𝑎=[𝑎𝑖,𝑎1,𝑎2,…,𝑎𝑖−2,𝑎𝑖−1,𝑎𝑖+1,𝑎𝑖+2,…,𝑎𝑛].

For example, if 𝑎=[5,4,2,1,3] and 𝑖=3 (that is, this is the third operation), then as a result of this operation, he could get any of these three arrays:

𝑎=[5,4,2,1,3] (makes 0 cyclic shifts, or any number that is divisible by 3);
𝑎=[2,5,4,1,3] (makes 1 cyclic shift, or any number that has a remainder of 1 when divided by 3);
𝑎=[4,2,5,1,3] (makes 2 cyclic shifts, or any number that has a remainder of 2 when divided by 3).
Let's look at an example. Let 𝑛=6, i.e. initially 𝑎=[1,2,3,4,5,6]. A possible scenario is described below.

𝑖=1: no matter how many cyclic shifts Petya makes, the array 𝑎 does not change.
𝑖=2: let's say Petya decided to make a 1 cyclic shift, then the array will look like 𝑎=[2,1,3,4,5,6].
𝑖=3: let's say Petya decided to make 1 cyclic shift, then the array will look like 𝑎=[3,2,1,4,5,6].
𝑖=4: let's say Petya decided to make 2 cyclic shifts, the original array will look like 𝑎=[1,4,3,2,5,6].
𝑖=5: let's say Petya decided to make 0 cyclic shifts, then the array won't change.
𝑖=6: let's say Petya decided to make 4 cyclic shifts, the array will look like 𝑎=[3,2,5,6,1,4].
You are given a final array state 𝑎 after all 𝑛 operations. Determine if there is a way to perform the operation that produces this result. In this case, if an answer exists, print the numbers of cyclical shifts that occurred during each of the 𝑛 operations.

Input
The first line of the input contains an integer 𝑡 (1≤𝑡≤500) — the number of test cases in the test.

The descriptions of the test cases follow.

The first line of the description of each test case contains one integer 𝑛 (2≤𝑛≤2⋅103) — the length of the array 𝑎.

The next line contains the final state of the array 𝑎: 𝑛 integers 𝑎1,𝑎2,…,𝑎𝑛 (1≤𝑎𝑖≤𝑛) are written. All 𝑎𝑖 are distinct.

It is guaranteed that the sum of 𝑛 values over all test cases does not exceed 2⋅103.

Output
For each test case, print the answer on a separate line.

Print -1 if the given final value 𝑎 cannot be obtained by performing an arbitrary number of cyclic shifts on each operation. Otherwise, print 𝑛 non-negative integers 𝑑1,𝑑2,…,𝑑𝑛 (𝑑𝑖≥0), where 𝑑𝑖 means that during the 𝑖-th operation the first 𝑖 elements of the array were cyclic shifted to the right 𝑑𝑖 times.

If there are several possible answers, print the one where the total number of shifts is minimal (that is, the sum of 𝑑𝑖 values is the smallest). If there are several such answers, print any of them.
