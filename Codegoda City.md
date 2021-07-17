<h3>Codegoda City</h3>

Codegoda City is preparing to welcome back international tourists. The city is full of attractions, many of which can be reached through several bi-directional connections. However, some attractions are connected through only one pathway. These one-path connections are called Goji Connections, and the local mayor is concerned that once tourism is open, these connections may produce large crowds that inhibit social distancing.

The mayor wants to expand these one-path connections to create more connections and safer tourism. However, Codegoda City has never mapped all the Goji Connections. Please help the local mayor to find all the Goji Connections so international travel to Codegoda City can start again!

<b>Input Format:</b>

First line: N represents the number of attractions.

Next N lines: attraction number, colon, then attraction numbers separated by commas.

Ex. 2:3, 4 means that Attraction 2 is connected to Attraction 3 and Attraction 4.

<b>Output Format:</b>

First line: C - number of Goji Connections

Next lines: list of Goji connections in ascending order by number of the first attraction. The connection starts from the attractions with lower number.

For example, this is a valid output:
<pre>
2
1-4
3-5
</pre>
and these are not valid:
<pre>
2 
3-5
1-4
2
4-1
3-5
</pre>
<b>Sample Input:</b>
<pre>
4
1: 2
2: 1, 3, 4
3: 2, 4
4: 2, 3
</pre>
<b>Sample Output:</b>
<pre>
1
1-2</pre>
