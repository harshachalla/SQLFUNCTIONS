SQL Date Functions
DATEADD() Function
The DATEADD() function adds a time/date interval to a date and then returns the date.

Syntax
DATEADD(interval, number, date)


interval	        Required. The time/date interval to add. Can be one of the following values:

                  year, yyyy, yy = Year
                  quarter, qq, q = Quarter
                  month, mm, m = month
                  dayofyear = Day of the year
                  day, dy, y = Day
                  week, ww, wk = Week
                  weekday, dw, w = Weekday
                  hour, hh = hour
                  minute, mi, n = Minute
                  second, ss, s = Second
                  millisecond, ms = Millisecond

example: SELECT DATEADD(month, 2, '2017/08/25') AS DateAdd;

    output: DateAdd
        2017-10-25 00:00:00.000
        
example:2 SELECT DATEADD(month, -2, '2017/08/25') AS DateAdd;

    output: DateAdd
            2017-06-25 00:00:00.000

