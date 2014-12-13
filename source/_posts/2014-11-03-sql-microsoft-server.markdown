---
layout: post
title: "sql(microsoft server)"
date: 2014-11-03 17:31:45 +0800
comments: true
categories: DB Job
---

It happens that I need to work with Microsoft SQL server, then problem comes ...

## Some tips about SQL:

* join multiple tables
``` sql
	SELECT p.Name, v.Name
	FROM Production.Product p
	JOIN Purchasing.ProductVendor pv
	ON p.ProductID = pv.ProductID
	JOIN Purchasing.Vendor v
	ON pv.BusinessEntityID = v.BusinessEntityID
	WHERE ProductSubcategoryID = 15
	ORDER BY v.Name;
```

* remove deplicated rows
``` sql
	SELECT MIN(RowId) as RowId, Col1, Col2, Col3 
	FROM MyTable
	GROUP BY Col1, Col2, Col3
```

<!-- more -->

* move Table from one datebase to another
``` sql
	SELECT * 
	INTO DestinationDB..MyDestinationTable 
	FROM SourceDB..MySourceTable 
```

* select count greater than
```sql
	SELECT * 
	  FROM db.table 
	GROUP BY someField
	HAVING COUNT(someField) > 1
```

* substring
``` sql
	SELECT LastName, SUBSTRING(FirstName, 1, 1) AS Initial
	FROM Person.Person
	WHERE LastName like 'Barl%'
	ORDER BY LastName;
```
* convert
``` sql
	CONVERT(data_type(length),expression,style)
```

* insert from one table to another
``` sql
	INSERT INTO table2
	(column_name(s))
	SELECT column_name(s)
	FROM table1;
```

* extract date from datetime
``` sql
	DATEPART(DATOFYEAR, field)
```

* compare date
``` sql
	SELECT *
	FROM STUDENTS
	WHERE BIRTHDAY > '1992-07-01'  -- born later than that
```


## Some tips about Microsoft SQL server:

[Output query results to a seperate file](http://stackoverflow.com/questions/3169220/export-query-result-to-csv-file-in-sql-server-2008)

## Some tips about unicode encoding in Python
``` python
	import codecs
	f = codecs.open('unicode.rst', encoding='utf-8')
	for line in f:
	    print repr(line)
```