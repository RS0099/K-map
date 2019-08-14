# K-map
Java code to solve 4*4 K-map without don't cares
Logic behind the code-
    first form all possible combinations of 16 elements , then 8 elements , then 4 ,then 2 and finally the simplified expression for 1. 
I have used a 3d array in which one layer of array contains the k-map, while the second layer contains the value for 1. The value contains information whether the 1 is used before or not (in forming a combination).  0->value is  used  ,  1-> not used [note- these values are in second layer i.e. map[][][1]  ]. 
While making a combination ,it checks if even a single 1 is there in combinationg which is not used (if yes form the combination). 
I have used the ^(XOR OPERATOR)  to obtain which value is  (ABCD)cancelled. 
The extra 2 rows and columns (array is 6 by 6) are for storing the AB and CD value 
(00 01  11  10). 
 
Each expression is evaluated as a 4 length string (order ABCD) , in which a 0 value indicates complement (0 at B place,i.e. second , indicates B’), while 
1 indicates its value (1 at B place indicated B) , and an empty value indicates that that term must not be used. Eg- 10 1  is AB’D. note the blank space at the 3 position.  
 
