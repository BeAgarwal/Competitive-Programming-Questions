<h3>Agoji Print</h3>
Agoda has its own line of emojis called Agojis, and because every Agodan loves Agojis, now everyone wants Agoji stickers! To fulfill this request, the People Team director wants to print N Agojis.

Agojis come in M unique styles, and for each style, there is a minimum A requirement and a maximum B requirement (0 < A, A ≤ B) for printing.

In order to print the Agojis, you must calculate the number of distinct ways that N Agojis can be printed, while satisfying the minimum and maximum requirement for each unique style of Agoji. Since the answer could be a very large number, please calculate your answer using mod 1e9+7.

<b>Input Format</b>
The first line contains two integers, N and M (total Agojis and types of Agojis).

The second line (M) contains two integers, A and B (minimum and maximum requirements of 0 < A ≤ B ≤ N for Agojis of ith type in ith line).

<b>Constraints:</b>
<pre>
1 ≤ N ≤ 1e6

1 ≤ M ≤ 16

0 < A ≤ B ≤ N
</pre>
<b>Output Format</b>
A single integer (using mod 1e9+7) that represents the number of distinct ways the Agojis can be printed.

<b>Sample Input</b>
<b>Sample 1</b>
<pre>9 3
2 4
2 4
2 4</pre>
<b>Sample 2</b>
<pre>
6 2
3 3
3 3</pre>
<b>Sample 3</b>
<pre>4 2
3 4
2 4</pre>
<b>Sample Output</b>
<b>Sample 1</b>
<pre>
7
</pre>
<b>Sample 2</b>
<pre>
1
</pre>
<b>Sample 3</b>
<pre>
0
</pre>
<b>Explanation of Sample Output:</b>

In the first test case, the requirement is to print 9 Agojis from three types of Agojis. Let's say these Agojis are as follows:

<img width="180" alt="agoji1" src="https://user-images.githubusercontent.com/46283159/126032516-f4246c73-a2bb-4266-9e47-106c7165e16f.png"><img width="180" alt="agoji2" src="https://user-images.githubusercontent.com/46283159/126032490-658c928e-b27b-471b-b1a0-942a4a67e8e5.png"><img width="180" alt="agoji3" src="https://user-images.githubusercontent.com/46283159/126032492-02307893-d8b0-4774-9f83-7fdb715362df.png">

For each Agoji, the minimum requirement is 2 and the maximum requirement is 4, so we can print them in the following combinations:
<pre>
2 + 3 + 4
2 + 4 + 3
3 + 2 + 4
3 + 3 + 3
3 + 4 + 2
4 + 2 + 3
4 + 3 + 2
</pre>

Now, we can see there are 7 ways in total to print the Agojis.
