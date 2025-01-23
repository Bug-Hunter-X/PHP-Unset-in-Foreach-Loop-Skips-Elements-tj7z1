# PHP Unset() in Foreach Loop Bug

This repository demonstrates a common but subtle bug in PHP when using `unset()` within a `foreach` loop to remove elements from an array.  The issue arises because `unset()` only removes the element at the specified key; it does not automatically re-index the array.

**Bug:**
The `unset()` function removes the element at the specified index but doesn't automatically reindex the remaining elements. This causes issues when iterating over the array and removing elements as you may skip over elements. 

**Solution:**
The solution uses `array_values()` to re-index the array after removing elements, ensuring that all remaining elements are processed correctly.