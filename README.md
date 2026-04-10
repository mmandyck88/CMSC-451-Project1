The first project involves benchmarking the behavior of Java implementations of two of the following sorting algorithms, bubble sort, selection sort, insertion sort, Shell sort, merge sort, quick sort or heap sort. You must post your selection of the two algorithms that you chose in the "Ask the Professor" conference. Every student must have a unique combination of algorithms..
You must write the code to perform the benchmarking of the two algorithms that you selected. You do not have to write the sorting algorithms yourself, you may take them from some source, but you must reference your source.
You must identify some critical operation to count for each algorithm that reflects the overall performance and modify each of the two sorting algorithms so that they count that operation. In addition to counting critical operations you must measure the actual run time in nanoseconds.
In addition, you should examine the result of each call to verify that the data has been properly sorted to verify the correctness of the algorithm. If the array is not sorted, an exception should be thrown.
It should also randomly generate data to pass to the sorting methods. It should produce 40 data sets for each value of n, the size of the data set and average the result of those 40 runs. The exact same data must be used for both sorting algorithms. It should also create 12 different sizes of data sets. Choose sizes that will clearly demonstrate the trend as n becomes large. Be sure that the data set sizes are evenly spaced so this data can be used to generate graphs in project 2
This project should consist of two separate programs. The first of those programs should perform the benchmarking described above and generate two data files, one for each of the two sorting algorithms.
The benchmarking program must be written to conform to the following design:
The purpose of the methods in the abstract class AbstractSort are as follows:
 The method sort is an abstract method that must be implemented in both of your classes
that contain the sorting methods that you have selected
 The startSort method should be called before the sort begins and it should initialize the
counter and record the starting time of the sort
 The endSort method should be called after the sort ends and it should compute the
elapsed time of the sort
 The incrementCount method should be called whenever the critical operation that you
selected is executed and it should increment the critical operation counter
 The getCount method should return the final value of the counter
 The getTime method should return the elapsed time
The output files should contain 12 lines that correspond to the 12 data set sizes. The first value
on each line should be the data set size followed by 40 pairs of values. Each pair represents the
critical element count and the time in nanoseconds for each of the 40 runs of that data set size.
The values on each line should be delimited by spaces.
The second program should produce the report. It should allow the user to select the input file
using JFileChooser. The report should contain one line for each data set size and five columns
and should be displayed using a JTable. The first column should contain the data set size the
second the average of the critical counts for the 40 runs and the third the coefficient of variance
of those 40 values expressed as a percentage. The fourth and fifth column should contain similar
data for the times. The coefficient of variance of the critical operation counts and time
measurement for the 40 runs of each data set size provide a way to gauge the data sensitivity of
the algorithm.
