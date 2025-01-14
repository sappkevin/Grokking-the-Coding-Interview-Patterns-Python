# Python Code Reference for Patterns

## Array/List Operations
```python
# Remove duplicates
nums = [1, 2, 2, 3, 4, 4]
nums = list(set(nums))  # Using set
nums = list(dict.fromkeys(nums))  # Preserve order

# Remove specific element
nums.remove(element)  # Removes first occurrence
nums.pop(index)  # Removes by index
del nums[index]  # Removes by index

# Insert element
nums.insert(index, element)
nums.append(element)  # Add to end
nums.extend([1, 2, 3])  # Add multiple elements

# Sorting
nums.sort()  # In-place sort
nums.sort(reverse=True)  # Descending
sorted_nums = sorted(nums)  # Returns new list
nums.sort(key=lambda x: len(x))  # Custom sort

# Slicing
nums[::-1]  # Reverse list
nums[start:end:step]
```

## Two Pointers
```python
# Basic template
left, right = 0, len(nums) - 1
while left < right:
    # Process elements
    left += 1
    right -= 1

# Fast & slow pointer
slow = fast = head
while fast and fast.next:
    slow = slow.next
    fast = fast.next.next
```

## Sliding Window
```python
# Fixed window
from collections import deque
window = deque(maxlen=k)

# Variable window
start = curr_sum = 0
for end in range(len(nums)):
    curr_sum += nums[end]
    while curr_sum > target:
        curr_sum -= nums[start]
        start += 1
```

## Hash Maps
```python
from collections import defaultdict, Counter

# Frequency count
freq = Counter(nums)
freq = defaultdict(int)
for num in nums:
    freq[num] += 1

# Default dictionaries
graph = defaultdict(list)  # for adjacency lists
cache = defaultdict(int)   # for dynamic programming
```

## Heaps
```python
import heapq

# Min heap operations
heapq.heappush(heap, item)
smallest = heapq.heappop(heap)
heapq.heapify(list)  # Convert list to heap

# Max heap (negate values)
max_heap = []
heapq.heappush(max_heap, -num)
largest = -heapq.heappop(max_heap)

# K largest elements
k_largest = heapq.nlargest(k, nums)
k_smallest = heapq.nsmallest(k, nums)
```

## Trees
```python
# Tree node
class TreeNode:
    def __init__(self, val=0):
        self.val = val
        self.left = None
        self.right = None

# BFS template
from collections import deque
def bfs(root):
    if not root:
        return []
    queue = deque([root])
    while queue:
        node = queue.popleft()
        if node.left:
            queue.append(node.left)
        if node.right:
            queue.append(node.right)

# DFS template
def dfs(node):
    if not node:
        return
    # Process node
    dfs(node.left)
    dfs(node.right)
```

## Graphs
```python
# Adjacency list
graph = defaultdict(list)
for u, v in edges:
    graph[u].append(v)
    graph[v].append(u)  # for undirected

# BFS
def bfs(graph, start):
    visited = set([start])
    queue = deque([start])
    while queue:
        node = queue.popleft()
        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)

# DFS
def dfs(graph, node, visited):
    if node in visited:
        return
    visited.add(node)
    for neighbor in graph[node]:
        dfs(graph, neighbor, visited)
```

## Backtracking
```python
def backtrack(candidates, path, results):
    if condition:
        results.append(path[:])
        return
    
    for i in range(len(candidates)):
        path.append(candidates[i])
        backtrack(candidates[i+1:], path, results)
        path.pop()
```

## Dynamic Programming
```python
# Top-down with memoization
def dp(n, memo=None):
    if memo is None:
        memo = {}
    if n in memo:
        return memo[n]
    # Calculate result
    memo[n] = result
    return memo[n]

# Bottom-up with tabulation
def dp(n):
    dp = [0] * (n + 1)
    dp[0] = 1  # Base case
    for i in range(1, n + 1):
        # Fill dp table
        dp[i] = calculation
    return dp[n]
```

## Union Find
```python
class UnionFind:
    def __init__(self, n):
        self.parent = list(range(n))
        self.rank = [0] * n
    
    def find(self, x):
        if self.parent[x] != x:
            self.parent[x] = self.find(self.parent[x])
        return self.parent[x]
    
    def union(self, x, y):
        px, py = self.find(x), self.find(y)
        if px == py:
            return
        if self.rank[px] < self.rank[py]:
            self.parent[px] = py
        elif self.rank[px] > self.rank[py]:
            self.parent[py] = px
        else:
            self.parent[py] = px
            self.rank[px] += 1
```

## Binary Search
```python
def binary_search(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

# Bisect library
from bisect import bisect_left, bisect_right
index = bisect_left(nums, target)  # First occurrence
index = bisect_right(nums, target)  # Last occurrence + 1
```

## Sets and Set Operations
```python
# Set operations
s1 = set([1, 2, 3])
s2 = {3, 4, 5}
intersection = s1 & s2
union = s1 | s2
difference = s1 - s2
symmetric_diff = s1 ^ s2

# Set comprehension
evens = {x for x in range(10) if x % 2 == 0}
```

## Useful Built-in Functions
```python
# Numeric operations
max_val = float('-inf')
min_val = float('inf')
abs_val = abs(-5)
power = pow(2, 3)

# String operations
s = ''.join(['a', 'b', 'c'])
reversed_str = s[::-1]
is_digit = s.isdigit()
is_alpha = s.isalpha()

# Conversions
binary = bin(10)[2:]  # Remove '0b' prefix
integer = int('1010', 2)  # Binary to int
```