# Day21-50-days-coding-challenge

Problem 1: Pascal's Triangle – K-th Row

Problem Statement:
Given an integer rowIndex, return the k-th row of Pascal's Triangle (0-indexed).

Constraints:
0 ≤ rowIndex ≤ 33

Approach:
Use a single list initialized with [1].
Update the list from right to left for each new row.
This keeps space complexity to O(k).

Examples:
Input: rowIndex = 3
Output: [1, 3, 3, 1]

Input: rowIndex = 0
Output: [1]

Problem 2: Valid Parenthesis String

Problem Statement:
Given a string s with '(', ')' and '*', return true if it can be a valid parenthesis string.

Constraints:
1 ≤ s.length ≤ 100

Rules:
'*' can act as '(', ')' or an empty string "".
Parentheses must match correctly as per the usual rules.

Greedy Approach:
Maintain two bounds: low and high, to track the min and max number of open brackets.
Iterate through the string:
'(' increases both low and high
')' decreases both low and high
'*' decreases low and increases high
If high becomes less than 0, the string is invalid.
If low is 0 at the end of iteration, the string is valid.

Examples:
Input: "()" → Output: true
Input: "()" → Output: true
Input: "())" → Output: true
