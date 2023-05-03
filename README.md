Download Link: https://assignmentchef.com/product/solved-cs2123-data-structures-midterm-1-recursion-program
<br>
<span style="font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">Given the high weight of this problem you should start early and ask questions if you get stuck. Be sure to not share code with any other students. This assignment should be the work of you and you alone. </span><strong style="font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">Cheating will result in a zero.</strong>

<ul>

 <li><strong>Description</strong></li>

</ul>

Jethro and Cleatus are quarantined at home and bored. They spend most of their day sitting at their computer monitor working or browsing the internet in their small apartment. Out of boredom Jethro begins counting the number of steps needed to reach each location in their small apartment. After seeing that taking different paths from their computer to their coffee maker yields different numbers of steps a question dawns on them. They want to know what is the fewest number of steps needed to reach <strong>all </strong>of the locations in their small apartment starting from their computer.

Fortunately, Jethro is quite skilled at ASCII art. So they model their room with ASCII characters. A space ‘ ’ can be moved through. An asterisk ‘*’ is a wall or furniture that cannot be traversed (no climbing over furniture!). Going up, down, left, right one space takes exactly one step (we’ll assume no diagonal movements for that sake of simplicity). For example, here is a possible model of their room:

**************

<table width="107">

 <tbody>

  <tr>

   <td width="99">*</td>

   <td width="8">*</td>

  </tr>

  <tr>

   <td width="99">*        *</td>

   <td width="8">*</td>

  </tr>

  <tr>

   <td width="99">*        *</td>

   <td width="8">*</td>

  </tr>

  <tr>

   <td width="99">* ***</td>

   <td width="8">*</td>

  </tr>

  <tr>

   <td width="99">*</td>

   <td width="8">*</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>***** *</li>

 <li>*** *</li>

</ul>

**************

Assume that (0, 0) is the upper lefthand corner. For the sake of simplicity you can assume the apartment is enclosed in ‘*’ characters and that Jethro’s computer is located at (1,1).

Jethro is still new to programming and wants to hire you to write the program to label all of the ‘ ’ locations in their apartment with the minimum number of steps needed to reach them. To keep with the ASCII art theme you’ll use the letters A-Z Such that:

‘A’ is 0 steps

‘B’ is 1 step ‘C’ is 2 steps

…

‘Y’ is 24 steps

‘Z’ is 25 (or more) steps

For example, after running your algorithm on it, the apartment above should look as follows:

**************

*ABCDEFGHIJKL*

*BCDE*GHIJKLM*

*CDEF*HIJKLMN*

*DE***IJKLMNO*

*EFGHIJKLMNOP*

*FGHIJ*****PQ*

*GHIJK***SRQR*

************** Example 2:

**********************************

<ul>

 <li>*</li>

</ul>

**********************************

After applying your algorithm (we don’t count past ’Z’ since Jethro has a pretty small apartment):

**********************************

*ABCDEFGHIJKLMNOPQRSTUVWXYZZZZZZZ*

********************************** Example 3:

*******

<ul>

 <li>*</li>

</ul>

**** *

<ul>

 <li>* *</li>

</ul>

*******

After applying your algorithm (unreachable ’ ’ areas should remain unchanged):

*******

*ABCDE*

****EF*

<ul>

 <li>*FG*</li>

</ul>

*******

<strong>3     Problems</strong>

<strong>PROBLEM 1: (5 points)</strong>

Write a brute force recursive definition/idea for this problem. Specifically write a recursive algorithm attempts to update the symbol located at (<em>x,y</em>) where

0 ≤ <em>x &lt; MAXWIDTH,</em>0 ≤ <em>y &lt; MAXHEIGHT </em>and then is recursively called on all adjacent locations.

<strong>Hint 1: </strong>From any given space, you need to try to continue moving up, down, left, and right. DO NOT try to travel diagonally.

<strong>Hint 2: </strong>Your algorithm CAN move into a wall or furniture spot, but upon recognizing it as uncountable, it should return from that call.

<strong>Hint 3: </strong>It will help to pass the distance traveled so far from the start.

<strong>PROBLEM 2: (5 points)</strong>

To make sure you understand how this recursion will work, draw a recursion tree diagram if the room were just 4 x 5 with no furniture. Start your tree at position (1, 1)

*****

<ul>

 <li>*</li>

 <li>*</li>

</ul>

*****

<strong>Hint 1: </strong>Here’s the first 2 levels of your recursive call tree (the order of the calls on the 2nd level will depend on your pseudocode):

<strong>PROBLEM 3: (5 points)</strong>

Write a RECURSIVE program in C that implements your recursive algorithm.

The program must compile and run on the fox servers. Use valgrind on your program to try to find all possible defects before submitting.

<strong>Hint 1: </strong>chars can be treated like small valued integers. In particular, it may be helpful to use ‘+’ and ‘<em>&lt;</em>=’ with your chars.

Your program must output the base room first, and then the updated room when done, like so:

Base room:

**************

<table width="107">

 <tbody>

  <tr>

   <td width="99">*</td>

   <td width="8">*</td>

  </tr>

  <tr>

   <td width="99">*        *</td>

   <td width="8">*</td>

  </tr>

  <tr>

   <td width="99">*        *</td>

   <td width="8">*</td>

  </tr>

  <tr>

   <td width="99">* ***</td>

   <td width="8">*</td>

  </tr>

  <tr>

   <td width="99">*</td>

   <td width="8">*</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>***** *</li>

 <li>*** *</li>

</ul>

**************

Room after algorithm:

**************

*ABCDEFGHIJKL*

*BCDE*GHIJKLM*

*CDEF*HIJKLMN*

*DE***IJKLMNO*

*EFGHIJKLMNOP*

*FGHIJ*****PQ*

*GHIJK***SRQR*

**************

<strong>PROBLEM 4: (5 points)</strong>

What is the runtime complexity of your algorithm? We want to see HOW you arrived at your answer and if you are taking everything into account.

<strong>4     Deliverables:</strong>

Submit the following on Blackboard:

<ul>

 <li>a PDF, TXT, DOC file containing your answers for #1 and #4. Separate each problems answer with a few blank lines and give each a heading with its problem number.</li>

 <li>a PNG, JPG, PDF, or PPT file that is your answer for #2. Name the file so that it includes ”answer2” in its file name</li>

 <li>c which is the implementation for problem #3.</li>

</ul>


