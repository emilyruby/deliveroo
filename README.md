# Deliveroo Technical Task

This is my code for the 'Cron Parser' question!

## Running the Code

After cloning the project, just run the following command to get your cron
string parsed. This is assuming you have python installed:

`python parser.py "CRON_STRING"`

For example:

`python parser.py "*/15 0 1,15 * 1-5 /usr/bin/find"`

For this input, you should then get the following output:

```
Minutes: 0 15 30 45
Hours: 0
Day of month: 1 15
Month: 1 2 3 4 5 6 7 8 9 10 11 12
Day of Week: 1 2 3 4 5
Command: /usr/bin/find
```

### Future Development / Current Shortcomings

The following features are not yet complete in this version of the code:
- The code does not change the number of days in each month. For example, February has 31 instead of 28 days.
- The string format for days of the week and months of the year are case-sensitive. The actual cron spec states that this input is not case-sensitive so this needs to be altered. e.g. `MON` would succeed, whilst `mon` would not be recognised.
- There are no tests for this code, although there is error handling.
- Code structure could be definitely be improved, and further comments could be added to improve readability.
- The `#` special character is not supported.