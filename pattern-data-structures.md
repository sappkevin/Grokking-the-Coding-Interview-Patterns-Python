# Data Structures for Each Pattern

## Two Pointers
Primary Structures:
- Array/List (for in-place operations)
- String (for string manipulation)

Python Implementation:
```python
# Basic array/list
nums = []
# String (immutable)
s = ""
```

## Sliding Window
Primary Structures:
- Deque (for fixed window size)
- HashMap/Counter (for frequency counting in window)
- HashSet (for unique elements in window)

Python Implementation:
```python
from collections import deque, defaultdict, Counter
# Fixed size window
window = deque(maxlen=k)
# Frequency counter
freq = Counter()
# Unique elements
unique = set()
```

## Fast & Slow Pointers
Primary Structures:
- LinkedList (for cycle detection)
- Array (for in-place manipulation)

Python Implementation:
```python
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next
```

## Merge Intervals
Primary Structures:
- Array/List of tuples/lists (for intervals)
- MinHeap (for overlapping intervals)
- Stack (for merging)

Python Implementation:
```python
import heapq
# Intervals as tuples
intervals = [(start, end)]
# Priority queue for overlapping intervals
heap = []
heapq.heapify(heap)
```

## Cyclic Sort
Primary Structures:
- Array (in-place sorting)
- HashSet (for finding duplicates/missing)

Python Implementation:
```python
# Array for in-place swapping
nums = []
# Track seen numbers
seen = set()
```

## In-place Reversal of LinkedList
Primary Structures:
- LinkedList
- Three pointers (prev, curr, next)

Python Implementation:
```python
class ListNode:
    def __init__(self, val=0):
        self.val = val
        self.next = None
```

## Tree BFS
Primary Structures:
- Queue/Deque (for level-order traversal)
- Binary Tree nodes
- List (for storing results)

Python Implementation:
```python
from collections import deque
class TreeNode:
    def __init__(self, val=0):
        self.val = val
        self.left = right = None
queue = deque([root])
```

## Tree DFS
Primary Structures:
- Stack (for iterative DFS)
- Binary Tree nodes
- Recursion stack (for recursive DFS)

Python Implementation:
```python
class TreeNode:
    def __init__(self, val=0):
        self.val = val
        self.left = right = None
stack = [root]  # For iterative DFS
```

## Two Heaps
Primary Structures:
- MinHeap and MaxHeap
- Priority Queue

Python Implementation:
```python
import heapq
min_heap = []
max_heap = []  # Store negatives for max heap
heapq.heappush(min_heap, val)
heapq.heappush(max_heap, -val)
```

## Subsets/Combinations
Primary Structures:
- List (for storing current combination)
- Set (for avoiding duplicates)
- Stack (for backtracking)

Python Implementation:
```python
results = []
current = []
def backtrack(start, current):
    results.append(current[:])
```

## Modified Binary Search
Primary Structures:
- Sorted Array
- Two pointers (left, right)

Python Implementation:
```python
left, right = 0, len(nums) - 1
while left <= right:
    mid = left + (right - left) // 2
```

## Top K Elements
Primary Structures:
- Heap (MinHeap or MaxHeap)
- QuickSelect
- Bucket Sort (for finite range)

Python Implementation:
```python
import heapq
# For k largest
heap = []
for num in nums:
    heapq.heappush(heap, num)
    if len(heap) > k:
        heapq.heappop(heap)
```

## K-way Merge
Primary Structures:
- MinHeap (for tracking smallest elements)
- Lists/Arrays (for input lists)
- LinkedLists (for linked list merge)

Python Implementation:
```python
import heapq
heap = []
for i, arr in enumerate(arrays):
    if arr:
        heapq.heappush(heap, (arr[0], i, 0))
```

## Topological Sort
Primary Structures:
- Graph (Adjacency List)
- Queue (for BFS approach)
- Stack (for DFS approach)
- HashSet (for visited nodes)

Python Implementation:
```python
from collections import defaultdict, deque
graph = defaultdict(list)
in_degree = defaultdict(int)
queue = deque()
```

## Union Find
Primary Structures:
- Array/List (for parent pointers)
- Dictionary (for element to index mapping)
- Array (for rank/size tracking)

Python Implementation:
```python
class UnionFind:
    def __init__(self, n):
        self.parent = list(range(n))
        self.rank = [0] * n
```

## Trie
Primary Structures:
- TrieNode (custom class)
- Dictionary (for children)
- Boolean flag (for word endings)

Python Implementation:
```python
class TrieNode:
    def __init__(self):
        self.children = {}
        self.is_end = False
```

## Dynamic Programming
Primary Structures:
- Array/Matrix (for tabulation)
- Dictionary (for memoization)
- Recursion stack (for top-down)

Python Implementation:
```python
# 1D DP
dp = [0] * (n + 1)
# 2D DP
dp = [[0] * m for _ in range(n)]
# Memoization
memo = {}
```

## Graph Algorithms
Primary Structures:
- Adjacency List (Dictionary of Lists)
- Adjacency Matrix (2D Array)
- Priority Queue (for Dijkstra)
- Queue (for BFS)
- Stack/Recursion (for DFS)

Python Implementation:
```python
from collections import defaultdict, deque
# Adjacency list
graph = defaultdict(list)
# BFS queue
queue = deque([start])
# DFS visited set
visited = set()
```

## Hash Table
Primary Structures:
- Dictionary
- Counter
- DefaultDict

Python Implementation:
```python
from collections import defaultdict, Counter
# Frequency counter
freq = Counter(nums)
# Default values
graph = defaultdict(list)
counts = defaultdict(int)
```