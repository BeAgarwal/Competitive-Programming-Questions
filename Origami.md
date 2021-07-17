<h3>Origami</h3>

Given a matrix of m x n and a folding direction, determine what the matrix will look like when folded in the given way.

Given four points on a piece of paper, assume the top left corner has a value of 1, and going in a clockwise direction, each corner increases in value by 1.

![origami0](https://user-images.githubusercontent.com/46283159/126033953-f14284b2-8d64-4cee-921b-b0568d0c66be.png)

<b>Input Format</b>

- The first line is the number of test cases (t)
- The first line of each test case is the size of the matrix (m n)
- The second line of each test case is the folding direction from point c to d
- For the next m lines, each line is the row of that matrix with n values

<b>Constraints</b>
<pre>
- 1 ≤ c, d ≤ 4 and c ≠ d
- 1 ≤ m, n, t ≤ 1,000,000
- 0 ≤ value inside the matrix (v) ≤ 9
- When folded, if the value of vij that is folded over vi'j' are not the same, we considered it asymmetrical (see Sample 3)
- If a side has the size of 1, we cannot fold perpendicularly to that side.
</pre>
<b>Output Format</b>

For each test case, print the number of the test case starting with 1 followed by the list the resulting matrix of the folded paper. Use a hyphen symbol (-) for disappearing spaces. If the paper cannot be folded symmetrically, list “error.”

<b>Sample Input 1</b>
<pre>
1
1 1
1 2
0
</pre>
<b>Sample Output 1</b>
<pre>
1
error
</pre>
<b>Sample Output 1 Explanation</b>

The matrix has size 1x1, so it’s not foldable.

![image](https://user-images.githubusercontent.com/46283159/126034010-68f2fa55-a848-417c-9065-538822c1c3d2.png)

<b>Sample Input 2</b>
<pre>
1
3 3
1 3
0 1 2
1 3 1
2 1 0
</pre>
<b>Sample Output 2</b>
<pre>
1
--2
-31
210
</pre>

<b>Sample Output 2 Explanation</b>

If we fold it from corner 1 to corner 3, the numbers match the opposite numbers, so we can fold it symmetrically. The top left part has disappeared, so it is replaced with a hyphen symbol (-) in the output.

![image](https://user-images.githubusercontent.com/46283159/126034044-1ab989c7-5cd0-48ef-af04-d9cf9037f668.png)

**Sample Input 3**
<pre>
1
1 2
1 2
5 6
</pre>
**Sample Output 3**
<pre>
1
error
</pre>

**Sample Output 3 Explanation**

We have a foldable matrix. However, when we fold from corner 1 to corner 2, the values inside the matrix are different (5 and 6), so we cannot fold it symmetrically.

![image](https://user-images.githubusercontent.com/46283159/126034069-1f8ffe03-729d-4ce0-b17f-a26e6e0e80e3.png)

**Sample Input 4**
<pre>
1
1 3
1 2
1 2 1
</pre>
**Sample Output 4**
<pre>
1
-21
</pre>
**Sample Output 4 Explanation**

The numbers match each other in the opposite side.

![image](https://user-images.githubusercontent.com/46283159/126034091-c70d697f-edbb-491c-a06a-59d55c36eab1.png)
