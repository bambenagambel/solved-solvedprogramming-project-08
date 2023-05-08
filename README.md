Download Link: https://assignmentchef.com/product/solved-solvedprogramming-project-08
<br>
This assignment will give you more experience on the use of functions and dictionaries. You will practice them by processing a file from a real-life dataset. In general, any time you find yourself copying and pasting your code, you should probably place the copied code into a separate function and then call that function. Problem Statement Given a data file of 507 individuals and their physical attributes (weight, height, etc. from the body dataset at http://www.amstat.org/publications/jse/datasets/), create two linear regression models and their correlation:

• between a person’s BMI and their age.

• between a person’s weight and a combination of physical attributes. The authors propose the following formula: o -110 + 1.34(ChestDiameter) + 1.54(ChestDepth) + 1.20(BitrochantericDiameter) + 1.11(WristGirth) + 1.15(AnkleGirth) + 0.177(Height) Background BMI is short for Body Mass Index, is a measure based on a person’s weight and height. It is used as a estimator of healthy body weight (see http://en.wikipedia.org/wiki/Body_mass_index ) Linear regression is a form of regression analysis in which the relationship between one or more independent variables and another variable, called the dependent variable, is modeled by a least squares function, called a linear regression equation. A linear regression equation with one independent variable represents a straight line when the predicted value (i.e. the dependant variable from the regression equation) is plotted against the independent variable: this is called a simple linear regression. For example, suppose that a straight line is to be fit to the points (yi, xi), where i = 1, …, n; y is called the dependent variable and x is called the independent variable, and we want to predict y from x. Least Squares and Correlation The method we are going to use is called the least squares method. It takes a list of x values and y values (the same number of each) and calculates the slope and intercept of a line that best matches those values. See http://easycalculation.com/statistics/learn-regression.php for an example. To calculate the least squares line, we need to calculate the following values from the data:

• sumX and sumY: the sum of all the X values and the sum of all the Y values

• sumXY: the sum of all the products of each corresponding X,Y pair

• sumXSquared and sumYSquared: the sum of the square of every X value and the sum of the square of every Y value • N: the number of pairs The calculation then is:

• slope=(N*sumXY – (sumX*sumY))/(N*sumXSquared – (sumX)2)

• intercept = (sumY – (slope*sumX)) / N We will also then calculate the correlation coefficient, and indication of how “linear” the points are (how much, in total, the points are correlated as a line). That calculation is:

• corr = (N*sumXY – (sumX*sumY)) / sqrt((N*sumXSq – (sumX)2) * (N*sumYSq – (sumY)2)) The correlation value ranges between -1 and 1. A negative value means an inverse correlation, a positive value a positive correlation. Values near -1 or 1 are “good” correlations, values near 0 are “bad” correlations. See http://easycalculation.com/statistics/learn-correlation.php Project Description

• gather the data from the provided file ‘body.data’. The file ‘body.txt’ describes the data.

• For the BMI calculation, Age will be the x values, BMI the y values. The BMI calculation must be done with a function. o BMI is not a value found in the data. You will have to calculate it using the data. o Get the units right when you calculate the BMI!

• For the formula, Weight will be the x values and the formula results the y values. The calculation of the formula must be done with a function. o all units are correct as provided in the data for the formula

• calculate the slope and intercept of a linear regression line for those two measures. Print those two values for both measures. The calculation must be done with a function.

• calculate the correlation between the x and y data for both measures. Print the correlation. The calculation must be done with a function. Extra Credit (5 points)

• Plot the individual entries using matplotlib for both measures.

• Plot the calculated regression lines through the data. Deliverables proj08.py – your source code solution (remember to include your section, the date, project number and comments in your program).

1. Please be sure to use the specified file name, i.e. “proj08.py”

2. Save a copy of your file in your CSE account disk space (H drive on CSE computers). 3. You will electronically submit a copy of the file using the “handin” program: http://www.cse.msu.edu/handin/webclient Notes and Hints:

• Don’t try to tackle this project all at once. Complete one function (or part of a function) and test it out.

• Test your least squares function on known data to make sure it works

• You should test your functions before using them in the program. Create some small lists of known x and y values, for example [1,2,3,4,5] for both x and y. The slope and intercept of that should be obvious, as should the correlation. If you don’t get the required answers, fix the function before moving on. Create a small data file with only two or three entries and test that you can parse it correctly. Testing functions will make your life easier.

• Matplotlib details. Look at the book chapter on angel, but remember: o import pylab o pylab.plot(xList, yList, options) o for options, you can select the color and the type of ‘pip’ that shows up in the plot such as ‘ro’ (red circles). o pylab.show() will show the plot. Be sure to plot everything (car values and lines) before you call show.