---
description: >-
  Read a quick reference to cron syntax and learn about the options that SRE.ai
  supports.
---

# Cron syntax

## Allowed fields

```
 # ┌────────────── second (optional)
 # │ ┌──────────── minute
 # │ │ ┌────────── hour
 # │ │ │ ┌──────── day of month
 # │ │ │ │ ┌────── month
 # │ │ │ │ │ ┌──── day of week
 # │ │ │ │ │ │
 # │ │ │ │ │ │
 # * * * * * *
```

***

## Allowed values

<table><thead><tr><th width="374">Field</th><th>Value</th></tr></thead><tbody><tr><td>second</td><td>0-59</td></tr><tr><td>minute</td><td>0-59</td></tr><tr><td>hour</td><td>0-23</td></tr><tr><td>day of month</td><td>1-31</td></tr><tr><td>month</td><td>1-12 (or names)</td></tr><tr><td>day of week</td><td>0-7 (or names, 0 or 7 are Sunday)</td></tr></tbody></table>

***

## Using multiple values

You may use multiple values separated by a comma. \
\
The following example runs every minute 1, 2, 4, and 5:

```
1,2,4,5 * * * *
```

***

## Using ranges

You may define a range of values.&#x20;

The following example runs every minute to 1 from 5:

```
1-5 * * * *
```

***

## Using step values

You can use step values with ranges by following a range with '/' and a number. For example, writing `1-10/2` produces `2,4,6,8,10`. You can also place steps after an asterisk, so to specify 'every two minutes,' use `*/2`. The following example runs a task every two minutes:

```
*/2 * * * *
```

***

## Using names

You can use names or short names for months and weekdays. \
\
The following example runs on Sundays in January and September:

```
* * * January,September Sunday
```

The following example uses short names and runs on Sundays in January and September:

```
* * * Jan,Sep Sun
```
