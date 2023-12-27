# leetcode
## Day 1
### [704.Binary Search](https://leetcode.com/problems/binary-search/description/)
1. Using while left < right
- This condition avoids mid element being equal to right element, thus reducing the risk of infinite loop.
- Update the right element as 'right = mid'.
- This approach often requires post-processing after the loop, as the exact target might not be determined inside the loop.
2. Using while left <= right
- This condition allows loop to continue until 'left' and 'right' pointer meet (left = right), which can help find the exact match to the problem.
- Update the right element as 'right = mid - 1'.  

3. Complexity
- Time: O(logn)
- Space: O(1), No need extra array space, just use the given array.

### [27.Remove Element](https://leetcode.com/problems/remove-element/description/) - first time
1. Use fast and slow pointer
- Use fast pointer to iterate orignal array.
- Use slow pointer to skip target value. Update the array follwing the fast pointer. When pointing no-target value, update it with the fast pointer.  When pointing the target value, keep the pointer.