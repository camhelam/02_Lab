# 02_Lab
Main Lab 2 - Pizza
Background

You have been elected as President of the Pizza Council of BYUSA. Your primary responsibility is determining how many pizzas should be ordered for each BYUSA event. To make things easier, you decided to write a C++ program to help you do the calculations.
Reminder

For all main labs, before you start coding 1) read through the entire specification, 2) view the help video for the lab, and 3) think through at a high level how your full solution will look. Then start coding. Also, remember to carefully review the style guide in learning suite, as more of the style requirements now pertain to this lab and this increases with future labs.
Requirements
Part 1 - Count Your Many Pizzas (20 points)

    Prompt the user for the number of guests attending the event.
    Determine and report the number of large, medium, and small pizzas you need to order.
    For every 7 guests, order one large pizza
    For every 3 guests left over, order one medium pizza
    For every 1 guest left over, order one small pizza

Part 2 - Serving Size (15 points)

    Compute and report the total area of pizza (in square inches) you need to purchase. Do not round these values.
    Compute and report the total area of pizza (in square inches) each guest can eat. Do not round these values.

Part 3 - Supplementing the Budget (40 points)

    Prompt the user for the percent of the total price to be paid as a tip. The tip percentage will be input as a whole integer from 0 to 100.
    Compute and report the total cost (including tip) of all the pizzas, rounding to the nearest dollar. Note: Changing the value type into an int alone will not round to the nearest dollar. See the end of the "Notes" section below.

Implementation

Use const double PI = 3.14159 as π (pi) as C++ does not have a predefined value for π.

Use the following values for the pizza:
Pizza 	Price 	Diameter
Large 	$14.68 	20 inches
Medium 	$11.48 	16 inches
Small 	$7.28 	12 inches
Items Graded by the TA's Inspection (25 points)
Style

The TA will check for adherence to the Style Guidelines. The style criteria "Header Comments", "Format", "Test Cases", "Variables and Constants" and "Miscellaneous" from the style guide all apply to this lab. While there are still a number of style issues that are not yet applicable, there are a lot more than in lab #1. For example you must use constants for what otherwise might look like magic numbers (radius, pi, costs, 7, 3, etc).
Special Requirements:

None
Notes
Note on running your code

The test cases start with just the number of pizzas, so you can start there and then build up. Also, you can test your code as many times as you like.
Note on rounding

Consider the code shown below:

double arbitraryValue = 3.14159;
int anInt = arbitraryValue;

cout << anInt << endl;

This code prints the number 3 as you might expect, but not for the reason that you might think. C++ does not round the value, it merely drops the decimal part. Thus

double arbitraryValue = 2.71828;
int anInt = arbitraryValue;

cout << anInt << endl;

prints the value 2, not 3 as we might hope. A common way to trick c++ into rounding is to add 1/2 before the conversion, like this:

double arbitraryValue = 2.71828;
int roundedValue = arbitraryValue + 0.5;

cout << anInt << endl;

2.71828 + 0.5 is 3.21828. When we drop the decimal part we are left with 3 as we would hope for the rounded value. Conveniently this also works with 3.14159: 3.14159 + 0.5 = 3.64159, which when we drop the decimal part leaves just 3.

While this is sufficient for this lab, note that this approach does not work for negative numbers. It also requires some adaptation to work if you want to round to the nearest 1000th or something like that.
Sample Output

When you run the program in the case where there are 303 guests and you want to give a 15% tip, it must look like:

Please enter the number of guests: 303

43 large pizzas, 0 medium pizzas, and 2 small pizzas will be needed.

A total of 13735 square inches of pizza will be purchased (45.3301 per guest).

Please enter the tip as a percentage (i.e. 10 means 10%): 15


The total cost of the event will be: $743
