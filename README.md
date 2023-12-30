# leetcode
## Day 1
### [704. Binary Search](https://leetcode.com/problems/binary-search/description/)
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

Notes:  
- Very basic problem for Binary Search.   
- Strengthen the understanding of edge condition about left and right pointers.

### [27. Remove Element](https://leetcode.com/problems/remove-element/description/) - first time
1. Use fast and slow pointer
   - Use fast pointer to iterate orignal array.
   - Use slow pointer to skip target value. Update the array follwing the fast pointer. When pointing no-target value, update it with the fast pointer.  When pointing the target value, keep the pointer.
2. Complexity
   - Time: O(n)
   - Space: O(1), No need extra array space, just use the given array.  

Notes:
- When using force brute, it would be out of the index within just one for loop since the loop cannot update its size with the popping, so use two loops is better.  

### Summary:
Good start for the Carl's bootcamp!  
Today's problem is easy and time costs about 2 hours.  
Keep hustling!

## Day 2
### [977. Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/description/)
1. Use Two pointers to iterate array from head and tail. Since the number is non-decreasing, the biggest square of numbers should be placed on the two sides.
2. Complexity:
   - Time: O(n)
   - Space: O(n), New array is built.

Notes:
- Easy to use force brute, but cannot find out using two pointers immediately. Based on the spacial feature of sorted array, the best way to calculate square of the number and sort them is to iterate from two side.

### [209. Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/description/)
1. Use Sliding window to expand by adding number from the end and shrink by removing number from the start.
2. Complexity:
   - Time: O(n)
   - Space: O(1)

Notes:
- Not so familar with sliding window, also with the edge conditions of the iteration. Like the start and end pointer, initialize it to 0 or 1. Just be careful of it because it is important to solve problem with edge case thinking in the code interview or any other problems.

### Summary:
2 hours work.  
Cannot solve by myself.  
Try to review them after submission to strengthen the memory.  
And remember to read the problem carefully. Be sure to understand it.

## Day 3
### [203. Remove Linked List Elements](https://leetcode.com/problems/remove-linked-list-elements/description/)
1. Use a dummy head node for two reasons:
- Store the original linked list to return after ajustment.
- Make sure that target node could be removed when current node is the head node. (node.next = node.next.next)

2. Complexity:
   - Time: O(n)
   - Space: O(1)

Notes:
- Cannot deal with the head node and tail node if they are target nodes. Just use a dummy head node to handle it.
- Easy to get confused with the edge conditions. Like in the while loop, current node could be None leading runtime problem when visit the next node.

### [707. Design Linked List](https://leetcode.com/problems/design-linked-list/description/)
1. Use the dummy head node to ensure returning original Linked list after processing.
2. Call functions in the class to reduce building repeatly.
3. When dealing with nodes inside/in the middle of the linked list(besides head and tail), process cur.next.
4. Maintain Size attribute to avoid some edge conditions.
5. Complexity:
   - Time: O(index) if related to index, else O(1).
   - Space: O(1)  

Notes:
- Can not figure it out completely. Due to not so familar with the concept of linked list, ingnoring a lot of details leading some bugs.    

### [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/description/)
1. Two pointers:
   - Use pre pointer to store the reversed linked list. Use cur pointer to iterate the whole linked list.
   - No need dummy node. Just use cur node pointing to head.
   - Inside the loop, use tmp to store current node temporily.

2. Recursion:
   - Same internal logic as Two pointers. Update cur and pre in the return value. 
3. Complexity:
   - Time: O(n)
   - Space: O(1) with TP, O(n) with Recursion.

Notes:
- Can figure ou the logic in the loop, but wrongly set up a dummy node which is not necessary. 
- Just strenthen the logic, and pay more attention to the other parts.

Summary:  
Expire to the next day.  
Be more efficient and more focus on the problem solving.

