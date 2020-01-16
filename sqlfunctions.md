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
<dt>SQL Server DATEDIFF() Function</dt>

<dd>The DATEDIFF() function returns the difference between two dates.</dd>

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
