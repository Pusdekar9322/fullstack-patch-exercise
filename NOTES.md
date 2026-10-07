\# Patch Notes



\## Summary



Fixed three high-value issues:



1\. Corrected SQL operator precedence so the status filter is applied correctly with title/description search.

2\. Reset pagination to page 1 when the search text or status filter changes.

3\. Removed the unnecessary Thread.sleep delay from the task search API.



\## Not Changed



I did not change the existing pagination calculation or task ordering because they worked correctly during testing. I also avoided unrelated dependency changes to keep the patch focused.



\## Biggest Remaining Risk



The backend currently loads all matching tasks and performs pagination in memory. This is acceptable for the exercise dataset, but database-level pagination would be better for a large production dataset.



\## AI / Tools



I used AI assistance to understand the existing code, identify potential issues, explain the changes, and review my fixes. I tested and understood the changes before applying them.

