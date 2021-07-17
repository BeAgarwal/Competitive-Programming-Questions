<h3>Ransomeware</h3>

Your friend is a victim of a ransomware attack, and each message in his chat history has been encrypted. Each message was replaced by an encrypted message, plus the first 20 letters of the original message and a mysterious number.

Your friend would like to recover the chat messages but does not want to pay the attacker, so he asked for your help. You retrieved a copy of the ransomware, and after reverse-engineering it, you found the following:

The encryption was performed by swapping letter pairs in the message. For example, if the software decided to swap the letters "A" and "K," then all "A"s would be replaced with "K"s, and all "K"s would be replaced with "A"s. Spaces are left intact, and each message is encrypted independently, meaning the letter pairs learned in the first message cannot be used to decrypt the second message.

The mystery number is a 31-bit integer computed from the original message using the following algorithm:
<pre>
x = 424242  
for each letter in the message:  
  x = ((x << 5) + x) + ch  
  x = x & 0x0FFFFFFF</pre>
Whereas:

- ch is the character in each message (space = 0, A/a = 1, B/b = 2 and so on)
- << is the bitwise left shift operator
- & is the bitwise AND operator
- For example, the mystery number for "AB CD" is 145701404.

Input format

On the first line, the integer T represents the number of messages. Then for each message, there are three lines:

1. The encrypted message
2. The first 20 letters of the original message
3. The mystery number

<b>Constraints</b>

1 ≤ T ≤ 100

Each message contains only uppercase English letters (A to Z) and spaces. There is no punctuation.

Each message is at least one character long and no more than 1,000 characters long.

It is guaranteed that only the correct decryption of the message will result in the specified mystery number.

For each message, there are at most eight distinct characters for which their counterparts are not revealed in the first 20 letters of the original message.

Output format

The decrypted message (one line for each chat message)

<b>Sample Input</b>

<pre>
2 
UVKKQ UQX DIV BQH DIV BQH UDTTB XUDP DIV BQH AQRZM PURC XVVLVZA 
HELLO HOW ARE YOU AR 
62071285 
CUSSD FDMSO 
HELLO WORLD 
55125742
</pre>

<b>Sample Output</b>

<pre>
HELLO HOW ARE YOU ARE YOU HAPPY WHAT ARE YOU DOING THIS WEEKEND 
HELLO WORLD
</pre>
Explanation of Sample Output

The input contains two messages, so the output must contain two lines.

The first line is the decrypted message from lines 2-4 of the input. The second line is the decrypted message from lines 5-7 of the input. (Since the example message is less than 20 letters long, it is the same as "the first 20 letters of the original message" given in the input.)
