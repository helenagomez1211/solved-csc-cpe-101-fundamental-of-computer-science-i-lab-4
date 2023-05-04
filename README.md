Download Link: https://assignmentchef.com/product/solved-csc-cpe-101-fundamental-of-computer-science-i-lab-4
<br>
<h1>Lab 4, CSC 101</h1>

This lab provides additional exercises on conditional reasoning and an introduction to loops.

Download <u>Lab4_Given_Files.zip</u>, from PolyLearn (place it in your <sub>CPE101</sub> directory, and unzip the file.

<h2>Conditionals</h2>

This part of the lab is structured a bit differently from what you have been asked to do in the past. The given files, in the <sub>patterns </sub>directory, include a “driver” and multiple pattern files. You will not (and should not) need to modify these files. The driver provides a mostly complete program but it needs a function to work properly. This is the function that you are to write. The pattern files provide text-based “images”.

letter

Each pattern file consists of an “image” made up of letters. For a given pattern, you must write a function that returns the correct letter for the row/column position specified (as the function’s arguments). This function will be called multiple times; once for each position in the pattern image.

As an example, pattern00 is made up entirely of repeated ‘A’ characters. As such, the <sub>letter</sub> function could be written as follows.

<table width="634">

 <tbody>

  <tr>

   <td width="634"> </td>

  </tr>

  <tr>

   <td width="634">   def letter(row, col):return ‘A’</td>

  </tr>

 </tbody>

</table>

In general, however, the <sub>letter</sub> function must determine which letter to return based on the row and column provided. In the pattern files, rows and columns are counted beginning at 0. As such, the top-left character is at <sub>row == 0</sub> and <sub>col == 0</sub>. So if the pattern consisted of all ‘A’ characters but with a single ‘G’ character in the top-left corner, then the <sub>letter</sub> function might look as follows.

<table width="634">

 <tbody>

  <tr>

   <td width="634">   def letter(row, col):</td>

  </tr>

  <tr>

   <td width="634">      if (row == 0 and col == 0):return ‘G’       else:return ‘A’ </td>

  </tr>

 </tbody>

</table>

Multiple Files and All That

You will write multiple versions of this <sub>letter</sub> function. Since the <sub>driver.py</sub> file will remain unchanged, you must place your <sub>letter </sub>function in a separate file. The name for this file is given below (for convenience, it is the name of the pattern).

Of course, for a given execution, the driver must be “told” which specific <sub>letter</sub> function to use. You will do this by importing the <sub>driver</sub> in your file and calling the <sub>compare </sub>Patterns function in the driver. To this function, you must pass your <sub>letter</sub> function (by specifying the name as you would a variable). The following code completes the “all A” pattern example discussed above.

<table width="634">

 <tbody>

  <tr>

   <td width="634"> import driver</td>

  </tr>

  <tr>

   <td width="634">    def letter(row, col):return ‘A’if __name__ == ‘__main__’:driver.comparePatterns(letter)</td>

  </tr>

 </tbody>

</table>

Patterns – What you need to do.

pattern00

The <sub>pattern00.py</sub> is complete. Just run the pattern to see the message.

python3 pattern00.py &lt; pattern00

pattern01

In <sub>pattern01.py</sub>, write the <sub>letter</sub> function that will generate the pattern image in <sub>pattern01</sub>.

pattern02

In <sub>pattern02.py</sub>, write the <sub>letter</sub> function that will generate the pattern image in <sub>pattern02</sub>.

pattern03

In <sub>pattern03.py</sub>, write the <sub>letter</sub> function that will generate the pattern image in <sub>pattern03</sub>.

pattern04

In <sub>pattern04.py</sub>, write the <sub>letter</sub> function that will generate the pattern image in <sub>pattern04</sub>.

pattern05

In <sub>pattern05.py</sub>, write the <sub>letter</sub> function that will generate the pattern image in <sub>pattern05</sub>.

pattern06

In <sub>pattern06.py</sub>, write the <sub>letter</sub> function that will generate the pattern image in <sub>pattern06</sub>.

pattern07

In <sub>pattern07.py</sub>, write the <sub>letter</sub> function that will generate the pattern image in <sub>pattern07</sub>.

The file runAllPaterns runs all patterns at once. This file is executable. Make sure it has an executable access specifier.

chmod +x runAllPaterns

./ runAllPaterns

<h2>Loops</h2>

This part of the lab introduces you to loops in Python. You are asked to edit a small program that uses various loops to accomplish a task.

Code Reading

In the <sub>loops</sub> directory you will find a file called cubesTable.py. Study the source code to see how it works.

Predict the output from the program if the user enters: <sub>9 3 0</sub> Run the code to see if your prediction is correct.

Then predict the output from the program if the user enters: <sub>-5 5 3 0</sub> Run the code to see if your prediction is correct.

Finally predict the output from the program if the user enters: <sub>-5 5 -9 3 0</sub> Run the code to see if your prediction is correct.

Enhancement #1

Enhance the <sub>get_first()</sub> function by adding a input validation loop similar to the one in the <sub>get_table_size()</sub> function. The loop should reject negative user inputs. Follow the format of the example output below.

<table width="634">

 <tbody>

  <tr>

   <td width="634">   Enter the value of the first number in the table: -3</td>

  </tr>

  <tr>

   <td width="634">   First number must be non-negative.Enter the value of the first number in the table: 2</td>

  </tr>

 </tbody>

</table>







Enhancement #2

Complete the <sub>show_table()</sub> function by implementing the code for a for loop that will display the desired table of cubes. For example, if the user enters 4 5 as the inputs, the table will look like this:

<table width="634">

 <tbody>

  <tr>

   <td width="634">   Number  Cube     5       125</td>

  </tr>

  <tr>

   <td width="634">6            2167            3438            512</td>

  </tr>

 </tbody>

</table>




Enhancement #3

Add a new function <sub>get_increment()</sub> that is similar to <sub>get_first()</sub>. It should display the prompt <sub>“Enter the increment between rows: “</sub>. The function should use an input validation loop to reject negative user inputs using the message <sub>“Increment must be non-</sub>

negative.”.

Modify the <sub>show_table()</sub> function so that it takes a third parameter that is the row increment in the table. Modify the counting loop so that it uses the row increment when displaying the table.

Modify the <sub>main()</sub> function so that it calls <sub>get_increment()</sub> and passes the result to <sub>show_table()</sub>. For inputs of <sub>4 5 3</sub> the table should now look like this:

<table width="634">

 <tbody>

  <tr>

   <td width="634">   Number  Cube</td>

  </tr>

  <tr>

   <td width="634">   5       1258       51211      133114      2744</td>

  </tr>

 </tbody>

</table>

Hint: To get the numbers to line up nicely (as shown above), I <sub>print </sub>the first number left justified in a column of six spaces. You can do that using the <sub>%-6d</sub> modifier, like this or use .format:

<table width="634">

 <tbody>

  <tr>

   <td width="634">   print (“%-6d  %d” % (first, first**3))</td>

  </tr>

  <tr>

   <td width="634"> </td>

  </tr>

 </tbody>

</table>

Enhancement #4 – Last one!

Enhance the <sub>show_table()</sub> function so that it displays the sum of all the cubes in the table on a separate line below the table, in the format <sub>“The sum of cubes is: x”</sub> (where x is the sum of cubes).




Testing

Run the <sub>cubesTableInst</sub> solution version and compare it against yours to make sure they work the same. You do not need to be make input files and compare using <sub>diff</sub>. Just make sure the functionality is the same.

<h2>Demonstration</h2>

Demonstrate running the code from each part of the lab to your instructor to have this lab recorded as completed. In addition, be prepared to show the source code to your instructor.

For first part run all patterns by using given file:

./ runAllPaterns

<h2>Submission</h2>

Demo and submit all your .py files in PolyLearn (7 patterns and cubesTable.py)