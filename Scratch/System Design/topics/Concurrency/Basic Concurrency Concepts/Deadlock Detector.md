https://www.geeksforgeeks.org/deadlock-detection-algorithm-in-operating-system/
https://www.geeksforgeeks.org/deadlock-detection-recovery/

You lock can have a name.
What the deadlock detector would do is to keep track of these names and look for the conflicts

Deadlock detector will only find deadlock from your codes, so, you need to have a very good tests coverage and do not use unknown function (like 3rd party library) from inside lock