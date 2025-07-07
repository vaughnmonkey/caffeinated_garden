---
{"dg-publish":true,"permalink":"/Knowledge/Programming/MS-Excel/","tags":["microsoft","Excel","databases","csv"]}
---


>[!sources]-
>- Academic Sources:
>	- 
>
>- 

# Useful functions 
##### Combines multiple cells into 1 cell with that first input being what separates the cells from one another.
```
=TEXTJOIN(";",TRUE,F53:F143)
```

##### Determine if there are duplicate Cells in the column 
```
=IF(COUNTIF(A:A,"="&A3)>1,"2","0")
```

###### Alternating spacing for rows
```
=MOD(ROW(A1),2)
```
- use this along with data filter to have an adjustable gap 



# What is Excel?
- annoying 
	- not really I love it and its super useful
