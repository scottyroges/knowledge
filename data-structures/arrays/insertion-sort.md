# Insertion Sort

Description: Starting at second element, check if previous element is greater than current index. If it is then move previous elements to the right until the current element is larger. Then insert current element at that position

Worst Case: O(n^2) - reversed\
Best Case: O(n) - already sorted\
Space Complexity: O(1)

Not the most efficient in most cases, but useful for mostly sorted arrays. Also used only one additional int for extra space to hold the temp variable and does the sorting in place. Does a lot of writes.

### Language Specifics:
[Java Usage](/languages/java/java-insertion-sort.md)