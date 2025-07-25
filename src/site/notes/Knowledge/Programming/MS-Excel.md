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



# Useful Shortcuts

#####  Expand / Collapse All
1. Select the full sheet with Ctrl + A.
2. To collapse all groups, press Alt + A + H.
3. To expand them, press Alt + A + J.

# What is Excel?
- annoying 
	- not really I love it and its super useful

## Excel Features 

### Power Query 
- What is it?
	- Excel feature to gather, transform and shape data
	- ETL tool (Extract Transform Load)
		- Extract -> Get Data 
			- From Table/Range
			- CSV
			- TXT
			- Another excel workbook
			- From folder
			- Outside/Online sources
		- Transform
			- sort 
			- remove columns
			- remove rows
			- split columns
			- change case 
			- unpivot columns
			- append data
			- merge data
			- change data types
			- Group & Aggregate
		- Load
			- To Table 
			- PivotTable Report
			- Connection Only
				- to be used by other Queries 
			- To Data Model ([[Knowledge/Programming/MS-Excel#Power Pivot\|MS-Excel#Power Pivot]]) 
- Native to excel since 2016
	- can be used independently from Power Pivot
- Why use Power Query?
	- Can store way more data than regular worksheets
	- Has Powerful transformation tools (some usable in excel others not)
	- Update with one click of a button

- Examples 
	- importing data 
	- Power Query might use a query language called "M-Code"? 
		- don't know what that is but tutorial guy claims I won't need it.
	- underneath the column headers there is a small bar that shows some stats about the column
		- ![Pasted image 20250724143600.png](/img/user/Knowledge/Programming/Pasted%20image%2020250724143600.png) 
	- Icon in the header indicates the data type of the column
	- 


### Power Pivot

- What is Power Pivot
	- also known as the Data Model 
	- Accessed from Data or Power Pivot Tab
	- Create Pivot Tables from multiple tables stored in the model
- Why use it?
	- Store millions of rows of data 
	- relationships between tables (seems like SQL-light)
	- Powerful formula language called [[Knowledge/Programming/MS-Excel#DAX\|MS-Excel#DAX]] 

### DAX

- What is DAX?
	- the formula language used by Power Pivot
	- 