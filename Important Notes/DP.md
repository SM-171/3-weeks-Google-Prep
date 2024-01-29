## Dynamic Programming
Used to optimize solution of a problem by identifying repetition of sub-problems.

### Methods
1) Tabulation: 
- bottom-up DP (Starts with the base case and goes to the required answer)
2) Memoization: 
- top-down DP (start with the required value ---> go to base-case ---> backtrack)
- Store the value of sub-problems in a map/table
- **NOTE IMP**: The dimensions of the dp array are the number of variable values in the recursive code</br>
Example: if f(ind, target) where both ind and target are variable then, we will have a 2-D DP array;

**Converting recursion to memoization**
1) Declare 'dp' data structure to hold values.
2) Same the final result in a 'dp'.
3) After base cases, check if subproblem is solved previously. Return stored value if available.

### Important Questions
1) [Cherry Pick](https://leetcode.com/problems/cherry-pickup-ii/description/)

2) [Minimum Number of Moves to Make Palindrome](https://leetcode.com/problems/minimum-number-of-moves-to-make-palindrome/)

3) [Distinct Subsequences](https://leetcode.com/problems/distinct-subsequences/description/)

4) [Shortest Common Supersequence](https://leetcode.com/problems/shortest-common-supersequence/)

5) [Minimum Insertion Steps to Make a String Palindrome](https://leetcode.com/problems/minimum-insertion-steps-to-make-a-string-palindrome/description/)

6) **VV IMP** [Edit Distance](https://leetcode.com/problems/edit-distance/description/)

7) [Wildcard Matching](https://leetcode.com/problems/wildcard-matching/)

8) [Minimum Cost to Cut a Stick](https://leetcode.com/problems/minimum-cost-to-cut-a-stick/)
- TBD: Tabulation solution

9) [Burst Balloons](https://leetcode.com/problems/burst-balloons/description/)