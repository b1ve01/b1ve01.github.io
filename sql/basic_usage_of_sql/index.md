# [Home](/)
# [../Home/SQL](../)
# Basic usage of SQL
- # [Select](#select)
- # [Where](#where)
- # [Like](#like)
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## select
查詢所有數據
```
SELECT *
FROM table_1;
```
查詢特定列
```
SELECT column_1,column_2,...
FROM table_1;
``` 
<br/>  

## where
根據特定條件查詢
```
SELECT *
FROM table_1
WHERE condition_1 AND/OR condition_2;
```
標準數值運算符( = , != , < , <= , > , >= )
```
SELECT *
FROM table_1
WHERE column_1=1;
```
範圍内判斷
```
SELECT *
FROM table_1
WHERE column_1 (NOT) BETWEEN 1 AND 10;
```
列表内判斷
```
SELECT *
FROM table_1
WHERE column_1 (NOT) IN (1,3,5,7,9);
```
<br/>  

## like
