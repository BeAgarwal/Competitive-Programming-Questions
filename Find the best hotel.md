<h3>Find the best hotel</h3>

Agoda is looking forward to expanding business into a new country. This country has N cities which are connected using N-1 roads. The roads are built so that all cities are interconnected.

Agoda plans to launch a platform that will allow new hotels to register into the system. It also will allow tourists to search for hotels in which they want to stay.

Each tourist is in one of N cities. They want to find the cheapest cost for a one-night hotel stay, so they start searching on Agoda.

The total cost of staying in a hotel for one night comprises two parts:

1. The cost of a taxi to go to the hotel (the cost of the gas times the distance from the tourist's location to the hotel).
2. The cost of a single room per night at the hotel.

Your task is to implement a program that supports two operations:

1. H <b>\<name> \<u> \<c></b> A new hotel named name located at city u has registered into the platform. The hotel costs c for a single room per night.
2. Q <b>\<v></b> A tourist located in city v asks the platform to find the best hotel price. In this operation, output the hotel which has the best total cost in a format of <hotel-name> <total-cost>.

<b>Input format</b>
The first line: the number of cities (N) and the cost of the gas for the taxi ride to the hotel (G).

The next N-1 lines: three values of u v d. This means there is a road between city u and v with a distance of d.

The next line: the number of operations (K).

The next K lines: each line contains the operation as described above.

<b>Output format</b>
For each query operation, output the name of the cheapest hotel and the total cost to stay at that hotel for a night.

<b>Note:</b>
The first operation must be a hotel registration.

Hotel names consist only a-z, A-Z or 0-9.

If multiple hotels cost the same to stay for a night, the platform will choose the hotel that registered first.

  <b>Constraints:</b>
<pre>
N <= 50,000

K <= 200,000
</pre>
Total combined length of hotel names <= 200,000

The distance between cities <= $10^6$

The cost for a single room per night <= $10^6$

                                             
<b>Sample Input</b>
  <pre>
5 2
1 2 1
2 3 1
3 4 1
4 5 1
4
H AgodaTestHotel1 3 10
Q 5
H AgodaTestHotel2 1 5
Q 5
</pre>
<b>Sample Output</b>
<pre>
AgodaTestHotel1 14
AgodaTestHotel2 13
</pre>
  
<b>Explanation of Sample Output</b>
  
In the first tourist query, there is only one hotel, so the cost of staying at that hotel, if the tourist is in city 5, is calculated as follows: 2 (for gas) x 2 (the distance from city 3 to city 5) + 10 (the cost of the room) = 14.

The second tourist query is made after another hotel registers into the system. If the tourist is in city 5, this hotel will cost 2 (gas) x 4 (distance from city 1 to city 5) + 5 (cost of the room) = 13, which is less than staying at the first hotel.
