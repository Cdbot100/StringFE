README File for Program CAPJKE and spreadsheet mtml computation

Program CAPJKE reads in defect data and computes the jacknife 
estimator for the data. The estimator is the expected number of 
total defects (or total defective) components.
The expected number of remaining defects is performed 
using the following calculation:
   E(rem.defects) = E(total defects) - number of known defects.

Spreadsheet mtml computation contains a macro that loads in the defect
data.  Step by step instructions are given in the spreadsheet to
determine the mtml estimator and the expected number of remaining
defects.


INPUT:

1. The filename.

2. The data for program CAPJKE and spreadsheet mtml computation
   is a text file (*.txt or *.dat) in the following format:
     -  The first row contains the number of columns
        (the number of reviewers or test sites) followed by 
        the number of rows (number of defects or defective components).
     -  The remaining rows correspond to defects (or defective components).  
        A row contains a sequence of 0's or 1's 
         - a 1 indicates that the reviewer or test site found the defect 
          (or found a defect in the component), otherwise a 0 is given.

An example of a data file follows:
 3      10
 0   0   1
 0   0   1
 0   1   0
 1   0   0
 1   0   0
 1   1   0
 0   1   0
 0   1   1
 1   1   1
 1   1   1

OUTPUT:

FOR Program CAPJKE

To the screen:
The computed jacknife estimator.
Expected remaining defects (defective components).

To a dummy.fil:
Average p-hat = ___
Interpolated population estimate is     
 with standard error ___
Approximate 95 percent confidence interval  ___   to    ___


