# SQL Date Functions
<dl>
<dt>DATEADD() Function</dt>
<dd>The DATEADD() function adds a time/date interval to a date and then returns the date.</dd>

<dt>Syntax</dt>

</dl>

```
DATEADD(interval, number, date)
```

### interval	---->        Required. The time/date interval to add. Can be one of the following values:

                 * year, yyyy, yy = Year
                 * quarter, qq, q = Quarter
                 * month, mm, m = month
                 * dayofyear = Day of the year
                 * day, dy, y = Day
                 * week, ww, wk = Week
                 * weekday, dw, w = Weekday
                 * hour, hh = hour
                 * minute, mi, n = Minute
                 * second, ss, s = Second
                 * millisecond, ms = Millisecond

<dl>
<dt>example:1</dt> 
<dd>SELECT DATEADD(month, 2, '2017/08/25') AS DateAdd;</dd>
<dt>output:</dt>
 </dl>

 ```
DateAdd
2017-10-25 00:00:00.000
```

 <dl>
 <dt>example:2</dt> 
<dd>SELECT DATEADD(month, -2, '2017/08/25') AS DateAdd;</dd>
<dt>output:</dt>
</dl>

```
DateAdd
2017-06-25 00:00:00.000
```

<dl>
<dt> DATEDIFF() Function</dt>

<dd>The DATEDIFF() function returns the difference between two dates.To calculate the difference between two dates in years, months, weeks, etc., you use the DATEDIFF() function</dd>

<dt>Syntax</dt>
</dl>

```
DATEDIFF(interval, date1, date2)
```

<dl>
<dt>example:1  </dt>
<dd>SELECT DATEDIFF(year, '2017/08/25', '2011/08/25') AS DateDiff;</dd>
         <dt> output:</dt>
         </dl>

``` 
6
```
<dl>
<dt>DATENAME() Function</dt>
<dd>The DATENAME() function returns a **string** , NVARCHAR type, that represents a specified date part e.g., year, month and day of a specified date.</dd>
<dt>SYNTAX</dt>
</dl>

```
DATENAME(date_part,input_date)
```
<dl>
<dt>example:1</dt>
<dd>SELECT DATENAME(year, '2018-05-10') [datename];</dd>
<dt>output:</dt>
</dl>

```
datename
2018
```

#### note: Remember the output 2018 is not an integer it is a **character string** 

<dl><dt>DATEPART() function</dt>
<dd>The DATEPART() function returns an integer which is a part of a date such as a day, month, and year.</dd>

<dt>SYNTAX</dt>
</dl>

```
DATEPART ( date_part , input_date )
```

<dl>
<dt>
example:1</dt>
<dd>SELECT DATEPART(year, '2018-05-10') [datepart],</dd>
<dt>output:</dt>
</dl>

```
datepart
2018
```

#### note: Remember the output 2018 is not an integer it is a **INTEGER**

## DATENAME() vs. DATEPART()
Note that DATENAME() is similar to the DATEPART() except for the **return type**. The DATENAME() function returns the date part as a **character string** whereas the DATEPART() returns the date part as an **integer.**

<dl>
<dt>example:</dt>
<dd>SELECT DATEPART(year, '2018-05-10') + '1' [datepart], DATENAME(year, '2018-05-10') + '1' [datename] ;</dd>
<dt>output:</dt>
</dl>

```
datepart    datename
----------- -----------
2019        20181
```
<dl>
<dt> DAY() function</dt>
 <dd>The DAY() function returns an integer value which represents the day of a month (1-31) of a specified date.</dd>

<dt>SYNTAX</dt>
</dl>

```
DAY(input_date)
```
<dl>
<dt>example:1</dt>
<dd>SELECT DAY('2030-12-01') [DAY];</dd>

<dt>output:</dt>
</dl>

```
DAY
1
```
<dl>
<dt>The DAY() function will return 1 if the input date contains only time part:</dt>

<dt>example:<dl/dt>
<dd>SELECT DAY('10:20:30') [DAY];</dd>

<dt>output:</dt>
</dl>

```
DAY
1
```

### note: similarlly month() and year() works like day() but in year() if the input is only time format the output will return **1900**

<dl>
<dt>GETDATE() function</dt>
<dd>The GETDATE() function returns the current system timestamp as a DATETIME value without the database time zone offset. The DATETIME value is derived from the Operating System (OS) of the server on which the instance of SQL Server is running.</dd>

<dt>SYNTAX</dt>
</dl>

```
GETDATE()
```

<dl>
<dt>example:1</dt>
<dd>SELECT GETDATE() current_date_time;</dd>

<dt>output:</dt>
</dl>

```
current_date_time
2019-04-28 15:13:26.270
```
<dl>
<dt>To get the current date, you can use the CONVERT() function to convert the DATETIME value to a DATE as follows:</dt>

<dt>example :1</dt> 
<dd>SELECT CONVERT(DATE, GETDATE()) [Current Date];</dd>

<dt>output:</dt>
</dl>

```
Current Date
2019-04-28
```

<dl>
<dt>To get the current time only, you can use the CONVERT(), TRY_CONVERT(), or CAST() function to convert the result of the GETDATE() function to a time:</dt>

<dt>example:1 </dt>

<dd>SELECT CONVERT(TIME,GETDATE()),TRY_CONVERT(TIME, GETDATE()),CAST(GETDATE() AS TIME);</dd>

<dt>output: </dt>
</dl>

```
gives current time 
```
