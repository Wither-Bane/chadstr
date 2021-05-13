# chadstr.h
### Chad Strings - The Chad way to handle strings in C.

One str(...) macro to handle them all. //not completely finished

### Examples Usage:
```c
int table = 13;
int id = 37; 
str test1 = str("SELECT * FROM ", table, " where person_id ", id);
str test2 = str(test1);         //copies test1 to test2
str test3 = str(test2, test1); // returns concat of test2 and test1

test2 = test1; // acceptable, but wrong since test2 now points to test1 not copies it.

str(*test1); // returns char* to use in printf like functions
Ex: puts(str(*test1)); // prints test1;

free(test1); // will free memory for whole str.
```
