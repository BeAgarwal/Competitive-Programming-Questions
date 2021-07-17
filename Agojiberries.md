<h3>Agojiberries</h3>

Two Agoji friends, Red and Green, are playing their favorite game called Agojiberry Picking. (You can see examples of Agojis in “Agoji Print” problem.)

Here is the rules of the game:

- There are N Agojiberry trees placed in a row. Each tree has a predetermined number of berries.
- Red and Green will take turns choosing one tree on either end of a row and pick all the berries from that tree.
- After the berries have been picked, the tree will magically disappear from the row, and berries cannot be picked from it again.
- Red always starts the game.
- The player who picks the most Agojiberries wins the game. The game is considered a tie if both players pick the same number of Agojiberries.

After playing the game for a while, both Red and Green decide they want to add a new rule:

- If the number of Agojiberries in the trees on both ends are the same, the players may pick all the berries from both trees. (They still can pick only one tree when both trees have the same number of berries.)
Red and Green are experts at this game and will play the game optimally.

Can you predict the result of each game before and after the introduction of the new rule?

<b>Input format</b>

The first line is the number of testcases (T).

The first line for each test case is the number of trees (N).
Followed by the second line which will contain N numbers separated with a single space, representing the number of Agojiberries in each tree.

There will be at most 25 testcases.
For at least 60% of the testcases, there will be at most 100 trees.
For all testcases, there will be at most 500 trees, and the sum of all Agojiberries in all trees will not exceed 10^9.

<b>Output format</b>

The winner of the game <b>without</b> the new rule, followed by the winner of the game <b>with</b> the new rule separated by a single space.

Use <i><b>Red</b></i> or <i><b>Green</b></i> to output the winner. In case of a tie, please list <i><b>Tie</b></i>.

<b>Sample Input</b>
<pre>
2
2
1 1
3
1 999 1</pre>

<b>Sample Output</b>
<pre>
Tie Red
Green Green</pre>

<b>Explanation of Sample Output</b>

There are two testcases.

<b>For the first testcase:</b>
<pre>
2
1 1
</pre>
In this game there are two trees with 1 berry each.

Without the new rule, Red can pick from either tree and earn 1 berry. Green will then pick from the remaining tree, ending the game with each player having 1 berry.

With the new rule, Red can pick from both trees, leaving Green with no tree to pick from, which will end the game with Red having 2 berries and Green having none.

<b>For the second testcase:</b>
<pre>
3
1 999 1
</pre>
In this game there are three trees.

Without the new rule, Red can pick from a tree on any end and earn 1 berry. However, after Red picks, Green will be able to pick from the tree with 999 berries, thus winning the game. (Note that a player must pick from at least one tree during the player's turn.)

With the new rule, Red can now pick from trees on both sides of the row, as the number of Agojiberries is the same. However, with 2 berries, Red cannot win as Green will be able to pick from the tree with 999 berries.
