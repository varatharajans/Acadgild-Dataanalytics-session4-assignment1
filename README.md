# Acadgild-Dataanalytics-session4-assignment1

df1 = data.frame(CustId = c(1:6), Product = c(rep("TV", 3), rep("Radio", 3)))
df2 = data.frame(CustId = c(2, 4, 6), State = c(rep("Texas", 2), rep("NYC", 1)))
df1 #left table
df2 #right table
For the above given data frames and tables perform the following operations:
1. Return only the rows in which the left table have match
2. Return all rows from both tables, join records from the left which have matching keys in the right table.

Ans

> df1 = data.frame(CustId = c(1:6), Product = c(rep("TV", 3), rep("Radio", 3)))
> df2 = data.frame(CustId = c(2, 4, 6), State = c(rep("Texas", 2), rep("NYC", 1)))
> df1 #left table
  CustId Product
1      1      TV
2      2      TV
3      3      TV
4      4   Radio
5      5   Radio
6      6   Radio
> df2 #right table
  CustId State
1      2 Texas
2      4 Texas
3      6   NYC
  
> merge(x=df1,y=df2,by="CustId", all=TRUE)
  CustId Product State
1      1      TV  <NA>
2      2      TV Texas
3      3      TV  <NA>
4      4   Radio Texas
5      5   Radio  <NA>
6      6   Radio   NYC

