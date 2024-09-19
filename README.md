java c
CMPINF 0401 Intermediate Programming
Assignment 1
Topics: Review of expressions, conditions, loops and I/O
Online: Wednesday, September 4, 2024
Due: All source (.java) files and a completed Assignment Information Sheet zipped into a single file and submitted via Canvas by 11:59PM on Friday, September 20, 2024.
Late Due Date: 11:59PM on Monday, September 23, 2024.
Submission Note 1: The Canvas site will not accept any submissions after the Late Due Date. Be sure to submit whatever you have completed before the late deadline.
Submission Note 2:  Your .zip file should contain only .java files and your Assignment Information Sheet.  There should be no project files, .class files or project subdirectories in the .zip file.  Also, your TA must be able to compile your program from the command line using the javac command. Test your files to make sure this will work (especially if you use an IDE such as NetBeans for development). If the TA cannot compile your program as submitted you will receive minimal credit!
You are enjoying your life in Victorian England and have saved up some money, so you have decided to open a small shoppe dedicated to your favourite detective, Sherlock Holmes. Since your shoppe is small and you do not have any employees, you stock only a few select items:
Sherlock Holmes Books
2 pounds ( = 480 pence) each (regular)
50 shillings ( = 600 pence) each (autographed)
Sherlock Holmes Pipes
16 shillings (= 192 pence) each
or
A box of 4 for 3 pounds ( = 720 pence)
Genuine Deerstalker Caps
30 shillings ( = 360 pence) each
Knowing that Holmes loved puzzles, you decide to give discounts to anyone who can correctly solve a riddle that you pose to them. If they answer correctly, they will get the following discounted prices:
Sherlock Holmes Books
2 pounds ( = 480 pence) each (regular) [ no discount ]
45 shillings ( = 540 pence) each (autographed)
Sherlock Holmes Pipes
14 shillings (= 168 pence) each
or
A box of 4 for 54 shillings ( =  648 pence)
Genuine Deerstalker Caps
30 shillings ( = 360 pence) each  [ no discount ]
In addition to individual discounts, detectives who solve the riddle will also get a 5% discount on the final bill (rounded to the nearest pence)
Since Victorian England did not use a decimal system of currency, in your store window you remind your patrons of the currency values:
Note: Recall the currency used
1 penny (pence) = basic unit of currency
1 shilling = 12 pence
1 pound = 20 shillings ( = 240 pence)
Your assignment is to write a Java program that will simulate transactions between you and some of your customers.  The program should:
1) Ask if there is another customer to be waited on. If so, continue; if not, quit the program.
2) Welcome the customer and show them your price list.
3) Pose your riddle to the customer. This may be any riddle you wish to ask – you may look one up or you may make up your own. However, the answer should be simple (ex: a number, or just a couple of words).
4) If the customer answers correctly, congratulate them and show them the updated price list (with the discounts). Adjust the prices of the items accordingly. If the customer answers incorrectly, tell them this fact but don't tell them the correct answer – just let them know that they will be subject to the normal prices for the items.
5) Allow the customer to order items from the menu. This process should be iterative, with the customer possibly changing their order until finalizing it prior to checking out. For example, a customer could order 2 books and change their mind, deciding to order 5 books, or deciding not to order any books at all. Your ordering should allow for these possible changes for all items. For simplicity, uniformity and to be helpful, purchases will be managed in the following way:
> Purchases of pipes will always be made by number of individual items. If a customer wishes to buy a box of 4, they should specify 4 and your program should automatically detect that as 1 box of 4. Furthermore, for any number of pipes, K, you should automatically count as many whole boxes as you can before charging by the individual item. For example, if a customer asks for 10 pipes, this should be 2 boxes plus 2 single pipes. Think about how you can do this in a fairly simple way.
> At any point in the process the customer can ask to see the price list. In this case you will show them the prices that apply to them (either regular or discounted) just as you did initially.
> At any point in the process the customer can ask to see the itemized subtotal. The itemized subtotal should show all of the current purchases, including the number purchased of each item, their individual costs, and the total. However, it is not finalized until the customer decides to check out. Note that items that are NOT purchased should not be shown here.
> At any point in the process the customer can ask to check out. At this point the current orders are finalized and your program should continue with 6) below.
For an idea of how a customer transaction might proceed, see my sample output in file a1out.txt (in folder Files/Assignments/Assignment1 on Can代 写CMPINF 0401 Intermediate Programming Assignment 1Java
代做程序编程语言vas)
6) Once a customer opts to check out, tabulate the total and show the itemized bill (with unit and subtotal prices for each item) on the display. As with the subtotal display, only show items on the bill that have actually been purchased (in a real store you would not see any items that you did NOT actually buy).  If the 5% overall discount applies show that on a separate line with the amount discounted (remember that this should be rounded to the nearest pence).  See the example output in a1out.txt.
7) Ask the customer for some money, input the amount, and give the customer their change (by showing it on the display). The payment should be an iterative process – the customer enters an amount in pounds, shillings or pence (only one currency at a time) and the amount is added to the total. The loop should continue until the total value entered equals or exceeds the total bill.  During the process you should tell the user how much has been paid and how much still remains on their bill. If change is given, you will always give the minimum number of coins back (so you give larger currency before smaller currency). For example, if a customer's total bill is 410 pence and they pay with 2 pounds ( = 480 pence), they have overpaid by 70 pence. However, rather than giving them change of 70 pence, the change should be 5 shillings and 10 pence. See how this process works in the example output in a1out.txt.
8) Go back to 1) and do it all again (i.e. there is a big loop in your main program that can handle many customers).
For some example runs, see file a1out.txt (in folder Files/Assignments/Assignment1 on Canvas)
Important Requirements and Notes:
Clearly there are a few places in your program where loops are required. We discussed (or will discuss) several different looping constructs in lecture – choose one that is appropriate for the task at hand (more than one correct answer is possible).  See course notes and handouts and your text for help with loops.
You will also need to do some math to calculate totals and discounts and to convert currency. Think carefully about how you can do these things in relatively simple ways.
Be careful about handling special cases with regard to input. If the value the user enters is invalid your program should handle it in some reasonable way.  For example, you should not allow a user to purchase a negative number of any item, or to choose an invalid menu option. However, you can assume that the type of the data the user enters will always be valid (i.e. if you are expecting a number the user will not enter a non-numeric string). Some special cases are demonstrated in the example runs in file a1out.txt.
Use the Scanner class for your input. We will see later how we can get input into our programs in other ways as well.
Format your code nicely (indenting, etc) and be sure to use comments to explain your code where appropriate. Minimally you should have your name, course, section and a brief explanation at the beginning of your program. 
Your output should also be nicely formatted (make the user wants to run your program). In particular, your itemized bill must be presented in a nice, readable way.  See file a1out.txt for some example output.  There are several ways to format output in Java.  See your text and online documentation for some help with this.
Be sure to electronically fill out your Assignment Information Sheet, and to submit all materials (including the Assignment Information Sheet) in a single .zip file via Canvas. A template for this is posted in folder Files/Assignments on Canvas. Note that the TA should be able to compile and run your program directly after unzipping your files. If there are any problems with your submission you will lose some points.   
If you are interested in doing some extra credit, you can enhance your program in many ways. Here are some examples:
Have a list of riddles and choose one riddle randomly for each customer.
If the user answered the riddle correctly, show after the total their itemized overall savings. In other words, for a customer who answered the riddle correctly you should calculate the bill both with and without the discounts, and the difference is the amount the customer saved.  Show this total but also show the individual savings for each different item.
The Sherlock Holmes Books item as listed is not specific to any single book. Improve this option by having a list of books and allowing the user to select one or more specific books from the list. In this case you should also show the individual books selected in the final bill.
Be sure to mention any extra credit that you do on your Assignment Information Sheet. The maximum possible extra credit for this project is 10 points (out of 100). This total could be earned by any of the above options done very very well or combinations done not as well. Don’t do more work than you will get credit for.
Be sure to look at the a1out.txt file for ideas about the look and feel of your program. Your program DOES NOT have to look exactly like the sample run, but it should have the same functionality and should be well-formatted.







         
加QQ：99515681  WX：codinghelp
