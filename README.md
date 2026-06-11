README
Fraudulent Activity Notifications

Given daily expenditures and a trailing window size d, determine how many fraud notifications are sent. A notification is triggered when today's expenditure is greater than or equal to twice the median of the previous d days.

Approach
Use a frequency array (0–200) to store expenditure counts.
Compute the median directly from frequencies.
Slide the window by removing the oldest value and adding the newest.
Count notifications whenever:
expenditure[i] >= 2 × median
Algorithm
Initialize frequency counts for the first d days.
For each day from d to n-1:
Find twice the median from the frequency array.
Check notification condition.
Update the frequency array for the sliding window.
Return the total notifications.
Complexity
Time: O(n)
Space: O(201)
Example

Input:

9 5
2 3 4 2 3 6 8 4 5

Output:

2

Notifications are triggered on days 6 and 7.
