<div align="center">

## Showing formatted date/time


</div>

### Description

Shows how to display the date and time in a pleasent format
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jason Myerscough](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jason-myerscough.md)
**Level**          |Beginner
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C, C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+, UNIX C\+\+
**Category**       |[System Services/ Functions](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/system-services-functions__3-23.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jason-myerscough-showing-formatted-date-time__3-6489/archive/master.zip)





### Source Code

```
/* shows how to display the system time
 * coded by jason m
 * 30/06/03
 * [jase@linuxmail.org]
 */
#include<stdio.h>
#include<time.h>
int main(void)
{
	char days[][10] = {"Sunday",
				 "Monday",
				 "Tuesday",
				 "Wednesday",
				 "Thursday",
				 "Friday",
				 "Saturday"
				};
	char months[][20] = {"January",
				 "February",
				 "March",
				 "April",
				 "May",
				 "June",
				 "July",
				 "August",
				 "September",
				 "October",
				 "November",
				 "December"
				};
	time_t tme;
	struct tm *system_time;
	tme = time(NULL); /* get the sys time in system calender format */
	system_time = localtime(&tme); /* system_time will point to a tm structure created by
					* the compiler
					*/
	printf("The current time is: %.2d:%.2d:%.2d\n", system_time->tm_hour, system_time->tm_min, system_time->tm_sec);
	printf("The current date is: %s %d %s %d \n", days[system_time->tm_wday], system_time->tm_mday, months[system_time->tm_mon], (system_time->tm_year + 1900));
	return 0;
}
```

