
--This is a shell script to automate testing.

--To use this script use
./runSuite testList yourProgram


------
The testList is a file that containing a list of test names separated by a newline.
Each test name would have .in and .out files that contain input and expected output respectively.

Suppose my list file is 2 lines.

myTest
myTest1000

./runSuite testList yourProgram
Both tests will be run and runSuite will also expect the files 

myTest.in
myTest.out
myTest1000.in
myTest1000.out

runSuite will only report failed tests.
It will print out:

Test failed:
Input: (contents of input file)
Expected: (contents of output file)
Actual: (actual program output)