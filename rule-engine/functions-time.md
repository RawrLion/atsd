# Functions: time

## Overview

### The `date_parse` function
Converts the provided datetime string into a [Joda-time](http://joda-time.sourceforge.net/apidocs/org/joda/time/DateTime.html) DateTime object according to the specified format string and timezone (or offset from UTC).

Available timezones and their standard offsets are listed in [time zones](http://joda-time.sourceforge.net/timezones.html). If the timezone (or offset from UTC) is specified in the datetime string, and it differs from the timezone (offset) provided as the third argument, then the function will throw an exception.

### The `milliseconds` function
Converts the datetime string into UNIX time in milliseconds according to the specified format string and timezone (or offset from UTC).

### The `date_format` function
Converts timestamp to a formatted time string according to the format pattern and the timezone. 

## Syntax

```java
date_parse(string datetime[, string format[, string timezone]])
milliseconds(string datetime[, string format[, string timezone]])
date_format(long timestamp, string pattern, string timezone)
```

## Examples

```java
/* Returns true if the difference between the event time and start
time (ISO) retrieved from the property record is greater than 5 minutes. */
timestamp - milliseconds(property('docker.container::startedAt')) >  5*60000

/* Returns true if the specified date is a working day. */
date_parse(property('config::deleted')).dayOfWeek().get() < 6

/* Uses the server time zone to construct a DateTime object. */
date_parse("31.01.2017 12:36:03:283", "dd.MM.yyyy HH:mm:ss:SSS")

/* Uses the offset specified in the datetime string to construct a DateTime object. */
date_parse("31.01.2017 12:36:03:283 -08:00", "dd.MM.yyyy HH:mm:ss:SSS ZZ")

/* Uses the time zone specified in the datetime string to construct a DateTime object. */
date_parse"31.01.2017 12:36:03:283 Europe/Berlin", "dd.MM.yyyy HH:mm:ss:SSS ZZZ")

/* Constructs a DateTime object from the time zone provided as the third argument. */
date_parse("31.01.2017 12:36:03:283", "dd.MM.yyyy HH:mm:ss:SSS", "Europe/Berlin")

/* Constructs a DateTime object from the UTC offset provided as the third argument. */
date_parse("31.01.2017 12:36:03:283", "dd.MM.yyyy HH:mm:ss:SSS", "+01:00")

/* If the time zone (offset) is specified in the datetime string,
it should be exactly the same as provided by the third argument. */
date_parse("31.01.2017 12:36:03:283 Europe/Berlin", "dd.MM.yyyy HH:mm:ss:SSS ZZZ", "Europe/Berlin")

/* These expressions lead to exceptions. */
date_parse("31.01.2017 12:36:03:283 +01:00", "dd.MM.yyyy HH:mm:ss:SSS ZZ", "Europe/Berlin")
date_parse("31.01.2017 12:36:03:283 Europe/Brussels", "dd.MM.yyyy HH:mm:ss:SSS ZZZ", "Europe/Berlin")

/* Return formatted time string  "2017-02-22 11:18:00:000 Europe/Berlin" */
date_format(1487758680000L, "yyyy-MM-dd HH:mm:ss:SSS ZZZ", "Europe/Berlin")

```
