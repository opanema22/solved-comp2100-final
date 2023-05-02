Download Link: https://assignmentchef.com/product/solved-comp2100-final
<br>
<strong>Question 2 – Binary Search Tree</strong>

Your Q2 directory contains code that implements a binary search tree with a set of integer                                                                                                                                                             numbers. The implementation has had the code for “                                                                                    ​<em>find</em>​”, “ ​<em>delete</em>​”, and “     ​<em>sumEvenNodes</em>​” removed.

You are required to complete the implementation replacing the missing code.  Your answer must be placed in your Q2 directory.

<strong>Tasks: </strong>

<ul>

 <li>[7 marks] Implement the “​<em>find</em>​” method. The method should return “​true​” if a tree contains a key, otherwise return “false​ ​”.</li>

 <li>[7 marks] Implement the “<em>delete</em>​ ​” method. Use successor to replace the target node if the target node has two children.</li>

 <li>[6 marks] Implement the “<em>sumEvenNodes</em>​ ​” method to print the sum of the nodes that have​ an even number of direct children (zero is an even number)​.</li>

</ul>

Check the provided comments and test classes (​Task1Test.java, Task2Test.java,

Test3Test.java​) for more details on implementation details, i.e. return type, input arguments, and return type.

You may create more methods if you need. Make sure that you do not move the files in Q2 directory into another directory.

<table width="624">

 <tbody>

  <tr>

   <td width="624"><strong>Handy tips </strong></td>

  </tr>

  <tr>

   <td width="624">Three possible cases in deletion and required actions:1.    If the target node has no childrena.    Delete the target node2.    If the target node has one childa.    Replace the target node with the child node3.    If the target has two children (subtrees)a.    Replace the target node with its successorb.    Delete successor in subtree</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Question 3 – Testing</strong>

Your Q3 directory contains code that implements two useful utilities. MyUtil.java​ file contains <em>parseDouble</em> method to extract the first number in an input string. MyStringUtil.java​ file contains <em>isMixedCase</em>​ to check whether an input string contains both uppercase and lowercase characters.

<strong>Tasks: </strong>

<ul>

 <li> Your first task for this question is to implement a <strong>minimum</strong>​<strong> number</strong> of JUnit test cases for ​<em>parseDouble</em> that is ​<strong>code complete</strong>​. Write your test case(s) in ​<em>test()</em> method in ​java<em>.</em>​ ​Use ​<em>assertEquals</em> to check the correctness of the implementation. All test cases should pass the JUnit test to get the full marks.</li>

 <li>Your second task for this question is to implement a <strong>minimum</strong>​<strong> number</strong> of JUnit test cases for ​<em>isMixedCase</em> that is ​<strong>branch complete</strong>​. Write your test case(s) in <em>test()</em> method in java​ ​<em>. </em>​Use <em>assertEquals</em>​ to check the correctness of the implementation. All test cases should pass the JUnit test to get the full marks.</li>

</ul>

<table width="624">

 <tbody>

  <tr>

   <td width="624"><strong>Handy tips </strong></td>

  </tr>

  <tr>

   <td width="624"><strong>Code complete</strong>​: with a code complete test, all statements need to be executed at least once during the test. <strong>Branch complete</strong>​: with a branch complete test, all possible branch condition statements need to be executed during the test. Branch complete is different from path complete, which needs to take into account all possible execution paths of a program.</td>

  </tr>

 </tbody>

</table>




<strong>Question 4 – Tokenizer, Parser </strong>

The theme of this question is developing a simple parser for LOGO programming language. LOGO controls the commands for movement and drawing of a pointer on the screen.

Assume that we have a grid with 11 x 21 cells, where 11 is the number of rows and 21 is the number of columns. A pointer is represented by one of the following characters:

<ul>

 <li>“​^​”: The pointer is facing the ​<em>NORTH</em>​ direction</li>

 <li>“​&gt;​”: The pointer is facing the ​<em>EAST </em>​direction</li>

 <li>“​&lt;”: The pointer is facing the ​ <em>WEST </em>​ ​direction</li>

 <li>“​v​”: The pointer is facing the ​<em>SOUTH </em>​direction</li>

</ul>




We can control the movement and drawing of the pointer by the following commands:

<ul>

 <li>LEFT: Turn the direction of the pointer by 90 degrees to the left</li>

 <li>RIGHT: Turn the direction of the pointer by 90 degrees to the right</li>

 <li>PENUP: Set the status of the pointer to be leaving no trail, when it moves</li>

 <li>PENDOWN: Set the status of the pointer to be leaving a trail, when it moves</li>

 <li>FORWARD(​<em>n</em>​): Move the pointer along the direction it is pointing by ​<em>n</em>​ cells</li>

 <li>BACK(<em>n</em>​ ​): Move the pointer in the reverse direction it is pointing by <em>n</em>​ ​ cells</li>

 <li>FORWARD_TO_END: Move the pointer along the direction until it reaches the boundary of the grid</li>

 <li>BACK_TO_END: Move the pointer in the reverse direction until it reaches the boundary of the grid</li>

</ul>




The grammar of simplified LOGO language is given by:

&lt;Command&gt; := LEFT <sup>|</sup>​ RIGHT ​   <sup>|</sup>​ PENUP ​ <sup>|</sup>​ PENDOWN ​ <sup>|</sup>​ FORWARD(&lt;num&gt;) ​ <sup>|</sup>​ BACK(&lt;num&gt;)​

| FORWARD_TO_END | BACK_TO_END

&lt;Exp&gt; := &lt;Command&gt;;  &lt;Exp&gt;  <sup>|</sup>​  &lt;Command&gt;;​

where &lt;num&gt; is an integer literal.

(Check the example 1 on the next page)

<strong>Example 1: </strong>

<ul>

 <li>Initial screen: (in the example, the pointer is initially positioned with ​<em>NORTH </em>​direction at the center of the grid with PENUP status​)</li>

</ul>

#####################

#####################

#####################

#####################

#####################

##########^##########

#####################

#####################

#####################

#####################

#####################




<ul>

 <li>Input:</li>

</ul>

<strong>PENUP</strong>​; ​<strong>LEFT</strong>​; ​<strong>FORWARD</strong>​(10); ​<strong>PENDOWN</strong>​; ​<strong>RIGHT</strong>​;  ​<strong>BACK</strong>​(3);




<ul>

 <li>Output:</li>

</ul>

#####################

#####################

#####################

#####################

#####################

.####################

.####################

.####################

^####################

#####################

#####################


































(Check the example 2 on the next page)

<strong>Example 2: </strong>

<ul>

 <li>Initial screen: (in the example, the pointer is initially positioned with <em>SOUTH</em>​ ​ direction at the center of the grid with PENUP status)​</li>

</ul>

#####################

#####################

#####################

#####################

#####################

##########v##########

#####################

#####################

#####################

#####################

#####################




<ul>

 <li>Input:</li>

</ul>

<strong>PENDOWN;</strong>​ ​<strong>BACK_TO_END</strong>​;




<ul>

 <li>Output:</li>

</ul>

##########v##########

##########.##########

##########.##########

##########.##########

##########.##########

##########.##########

#####################

#####################

#####################

#####################

#####################




where an empty cell is represented by character “​#​”, a cell with the trail of the pointer is represented by character “​.​”, and the pointer is initially with PENUP status. Note that you do not need to consider cases where FORWARD(n) and BACK(n) can go beyond the boundary of the grid.






















(Check your tasks on the next page)




<strong>Tasks: </strong>




<ul>

 <li>[10 Marks] Complete “​<em>next</em>​()” methods in “​java​” to extract an input expression into tokens.</li>

 <li>[10 Marks] Complete “​<em>parse</em>​()“ method in “​java​” to parse an input expression by computing the final position of the pointer and marking the pointer movement on the screen.</li>

 <li>[10 Marks] Complete “​<em>trace</em>​()” method in “java​”​ to return a string showing the trail of the pointer, its current position and direction.</li>

</ul>




Please check the expected results of these methods from the JUnit test files:

TokenizerTest.java, ParserTest.java, ScreenTest.java​.




For 1) – 3), you should modify the required methods within Q4 directory. You can make any additional method if you need while completing the tasks. Make sure that you do not move the files in Q4 directory into another directory.