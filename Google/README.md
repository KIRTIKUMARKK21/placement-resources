# Google
> Collection of coding questions asked by Google during placements at IITs

## Questions Index

* [Cookies](#1-cookies) [IIT-BHU'21]

## 1. Cookies

Alice loves cookies. One day while wandering, she came across a cookie-world that has $N$ cookies in it, numbered from $1$ to $N$. 
Each cookie has an energy count of $E_i$ and is stored at height $H_i$. Initially, Alice's energy is $K$, and after eating a cookie with energy $E_i$ her energy increases by $E_i$.

In each step, Alice can climb to a certain height and can eat a cookie and return to her original position, but climbing requires energy, and she can only climb height $H_i$ if her energy $K$ is greater than or equal to the height $H_i$.

### Task

Determine the maximum number of cookies she can eat and the maximum energy she can attain after each step.

$Notes$

* $1$-based indexing is followed.
* Alice can eat the cookies in any order as long as the cookie she is trying to eat currently is located at a height not greater than her current energy.

### Example

$Assumptions$

* $N = 6$
* $H = [6, 1, 3, 9, 15, 30]$
* $E = [3, 5, 1, 2, 4, 3]$
* $K = 9$

$Approach$

Cookies eaten by Alice to maximize her energy after each step are:

* At first, Alice will eat cookie with energy $5$ at a height of $1$ and her energy increases to $9 + 5 = 14$.
* Then Alice will eat cookie with energy $3$ at a height of $6$ and her energy increases to $14 + 3 = 17$.
* Then Alice will eat cookie with energy $4$ at a height of $15$ and her energy increases to $17 + 4 = 21$.
* Then Alice will eat cookie with energy $2$ at a height of $9$ and her energy increases to $21 + 2 = 23$.
* Then Alice will eat cookie with energy $1$ at a height of $3$ and her energy increases to $23 + 1 = 24$.
* Alice will not be able to eat cookie at a height of $30.$

Hence, the number of cookies eaten by Alice is $5$.

Therefore the answer is $[5, 14, 17, 21, 23, 24].$

### Function Description

Complete the `solve` function provided in the editor. This function take the following $4$ parameters and returns an array of integers:

* $N:$ Represents an integer denoting the number of cookies
* $H:$ Represents an integer array denoting the height of $i_{th}$ cookie as $H_i$ ( $1 \leq i \leq N$ )
* $E:$ Represents an integer array denoting the energy of $i_{th}$ cookie as $E_i$ ( $1 \leq i \leq N$ )
* $K:$ Represents an integer denoting Alice's initial energy

### Input Format

* The first line contains a single integer $T$ that denotes the number of test cases. $T$ also denotes the number of times you have to run the `solve` function on a different set of inputs.
* For each test case:
  - The first line contains an integer $N.$
  - The second line contains $N$ space-separated integers denoting the array $H.$
  - The third line contains $N$ space-separated integers denoting the array $E.$
  - The fourth line contains an integer $K.$

### Output Format

For every test case, print the number of cookies that can be eaten by Alice, followed by the maximum score she can attain after eating each cookie in a new line.

### Constraints

* $1 \leq T \leq 10$
* $1 \leq N \leq 10^5$
* $1 \leq K \leq 10^9$
* $1 \leq H_i, E_i \leq 10^5$

<table>
<tr>
<td> Sample Input </td>
<td> Sample Output </td>
</tr>
<tr>
<td>

```shell
1                            
5
3 2 6 8 10
2 1 2 3 1
3
```

</td>
<td>

```shell
5                            
5 6 8 11 12
```

</td>
</tr>
</table>

