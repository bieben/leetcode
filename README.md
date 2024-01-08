# leetcode
## Day 1 - Array part 1
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
- Good start for the Carl's bootcamp!  
- Today's problem is easy and time costs about 2 hours.  
- Keep hustling!

## Day 2 - Array part 2
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
- 2 hours work.  
- Cannot solve by myself.  
- Try to review them after submission to strengthen the memory.  
- And remember to read the problem carefully. Be sure to understand it.

## Day 3 - Linked List part 1
### [203. Remove Linked List Elements](https://leetcode.com/problems/remove-linked-list-elements/description/)
1. Use a dummy head node for two reasons:
   - Store the original linked list to return after ajustment.
   - Make sure that target node could be removed when current node is the head node. (node.next = node.next.next)
2. Pay attention to the move of pointers. 
3. Complexity:
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
   - Same internal logic as Two pointers. 
   - Exit when cur == None. Update cur and pre in the return value. 
3. Complexity:
   - Time: O(n)
   - Space: O(1) with TP, O(n) with Recursion.

Notes:
- Can figure ou the logic in the loop, but wrongly set up a dummy node which is not necessary. 
- Just strenthen the logic, and pay more attention to the other parts.

### Summary:  
- Expire to the next day.  
- Be more efficient and more focus on the problem solving.
## Day 4
miss
## Day 5
Rest

## Day 6 - Hash Map part 1
### [242. Valid Anagram](https://leetcode.com/problems/valid-anagram/description/)
1. Iterate given String and target String, use an array to record chr's appearance and check in the target String.
2. Use ord() to store every char in a hash map of 26 letters. Then check them in the target string.
3. Complexity:
   - Time: O(n)
   - Space: O(1)

### [349. Intersection of Two Arrays](https://leetcode.com/problems/intersection-of-two-arrays/description/)
1. Use hash map to store the elements of first array, then check the second array if element in the map. Delete element in the hash map after add the intersection in the result list.
2. Complexity:
   - Time: O(n+m), create the hash map from nums1(n length of nums1) and iterate over nums2 and check in the hash map(m: length of nums2; plus 1:lookup the hash map).
   - Space: O(n), hash map(n) and result array(min(n,m) min length of nums1 and nums2)

### [202. Happy Number](https://leetcode.com/problems/happy-number/description/)
1. Use set to store the calculated sum while iterating, since if a repeat sum is appear it means that the iteration will never end.
2. Use sum with for loop to calculate sum of square of every digit.
3. Complexity:
   - Time: O(logn), the number of digits in a number n is prportional to the logarithm of n, which is approximately log10(n) digits. e.g. 1000 has 4 digits(log10(1000) = 3).
   - Space: O(logn), it's related to the number of digits in n and the unique numbers generated from those digits.

Notes:
- Not so familar with calculating the square of every digits in n.
- Set can store unique elements.

### [1. Two Sum](https://leetcode.com/problems/two-sum/description/)
1. Use hash map to store difference with target and the index. When encounter the target complement value, return two index at the same time.
2. Hash Map:
   - Store value and index at the same time.
   - Quickly track the Complement value in O(1) average time.
   - Avoid nested loop.
3. Complexity:
   - Time: O(n)
   - Space: O(n)  

### Summary:
- Miss a day practice and complete it today.
- Easy problems but strengthen the memory and solutions.

## Day 7 - Hash map part 2
### [454. 4Sum II](https://leetcode.com/problems/4sum-ii/description/)
1. Divide it into 2 parts with two nums. Thus there are only two for loop with O(n2).
2. Use hash map to store complement value.
3. Complexity:
   - Time: O(n2)
   - Space: O(n2), which worst case is that A and B are totally different.

Note:
- If 4 for loop are too slow, try to split it into 2 part to calculate sum.

### [383. Ransom Note](https://leetcode.com/problems/ransom-note/description/)
1. Use hash map to check two string.
2. Use array to build a hash map for 26 letter. Iterate two strings then compare the count of every letter with all() function.
3. Complexity:
   - Time: O(n)
   - Space: O(1) for array-based O(u) for dictionary-based.

Notes:
- Use array-based for space efficiency.

### [3. 3Sum](https://leetcode.com/problems/3sum/description/)
1. Use 2 pointers to iterate array and to find target pair. 
2. Skip duplicate inside the *while* loop for two pointers(left and right) and also in the *for* loop for first pointer.
3. Complexity:
   - Time: O(n2), O(nlogn) for sorting and O(n2) for finding triplets.
   - Space: O(1)

### [18. 4Sum](https://leetcode.com/problems/4sum/description/)
1. Same logic as 3Sum, but one more for loop.
2. Adjust skipping duplicate with second for loop. Avoid wrongly skipping valid value by skip as j > i+1.
3. Complexity:
   - Time: O(n3)
   - Space: O(1)

### Summary:
- Strengthen the logic of the **Sum** Problems.
- Dictionary takes more space than array, but less time than array. Decision of using which depends on the type of given data.

## Day 13 - Stack and Queue part 3
### [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/description/)
1. Use deque to get the max num of current sliding window.
   - **Adding Elements to Deque**: While the current element *x* is greater than the last element of deque, remove from the back of deque. This ensure the deque always has the largest element at the front.
   - **Appending to Deque**: Append the index of the current element to the deque.
   - **Maintain Window Size**: If the first element of deque is outside the current window(the difference between the current index i and the index at the front of the deque is at least k, i - q[0]), remove it from the front.
   - **Adding to Result**: Once the window size reaches 'k', add the element corresponding to the front of the deque to the result list 'res', as it's the maximum in the current window.
2. Complexity:
   - Time: O(n)
   - Space: O(k)

### [347. Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/description/)
1. Use hash map to record the frequency and value.
2. Use a Min-Heap(Priority Queue) to sort and get the result in k size.
   - Insert *freq* and *key* into a min-heap.
   - If the size exceeds *k*, pop the smallest frequency(at the top of the heap). It ensures that only the 'k' most frequent elements remain in the heap.
   - Build and return the result list by populated in reverse order(poping elements from the heap, to ensure that higher frequency elements are placed at the end of the list).
3. Complexity:
   - Time: O(nlogk), counting freqency with O(n), insert n elements into heap(O(logk) for each) takes O(nlogk), and building result by heappop(logk for each) with additional O(klogk). Overall is O(nlogk + klogk).
   - Space: O(n)