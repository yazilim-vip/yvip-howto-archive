# date

date command is used to display the system date and time. date command is also used to set date and time of the system. By default the date command displays the date in the time zone on which unix/linux operating system is configured.You must be the super-user (root) to change the date and time.

            
| Format option | Part of Date | Desciption | Example Output |
|:------:|:------:|------|:------:|
| date +%a  | Weekday | Name of weekday in short (like Sun, Mon, Tue, Wed, Thu, Fri, Sat) |  Mon |
| date +%A  | Weekday |   Name of weekday in full (like Sunday, Monday, Tuesday)  |  Monday |
| date +%b  | Month  |  Name of Month in short (like Jan, Feb, Mar )   | Jan |
| date +%B  | Month  |  Month name in full short (like January, February)   | January |
| date +%d  | Day  |  Day of month (e.g., 01)  |  04 |
| date +%D  | MM/DD/YY  |  Current Date; shown in MM/DD/YY  |  02/18/18 |
| date +%F  | YYYY-MM-DD  |  Date; shown in YYYY-MM-DD  |  2018-01-19 |
| date +%H  | Hour  |  Hour in 24-hour clock format  |  18 |
| date +%I  | Hour |   Hour in 12-hour clock format |   10 |
| date +%j  | Day |   Day of year (001..366)  |  152 |
| date +%m  | Month  |  Number of month (01..12) (01 is January)   | 05 |
| date +%M  | Minutes |   Minutes (00..59)   | 52 |
| date +%S  | Seconds  |  Seconds (00..59)    |18 |
| date +%N  | Nanoseconds |   Nanoseconds (000000000..999999999)  |  300231695 |
| date +%T  | HH:MM:SS   | Time as HH:MM:SS (Hours in 24 Format) |   18:55:42 |
| date +%u  | Day of Week |   Day of week (1..7); 1 is Monday    | 7 |
| date +%U  | Week  |  Displays week number of year, with Sunday as first day of week (00..53)   | 23 |
| date +%Y  | Year   | Displays full year i.e. YYYY    2018 |
| date +%Z  | Timezone  |  Time zone abbreviation (Ex: IST, GMT)   | IST |



