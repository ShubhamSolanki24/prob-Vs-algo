### 1. Square Root Explanation

```python
def binary_search_sqrt(left_pointer, right_pointer, target):
    mid_pointer = (left_pointer + right_pointer) // 2
    if mid_pointer ** 2 <= target < (mid_pointer + 1) ** 2:
        return mid_pointer
    elif mid_pointer ** 2 > target:
        return binary_search_sqrt(left_pointer, mid_pointer - 1, target)
    return binary_search_sqrt(mid_pointer + 1, right_pointer, target)
```

Time complexity --> A binary search takes O(logn) throwing a half in each iteration
Space complexity --> O(logn), the binary search recursive stack 
