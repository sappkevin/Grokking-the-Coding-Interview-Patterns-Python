# Coding Pattern Explanations

## 1. Two Pointers
The two pointers pattern uses two pointers to traverse an array or sequence, usually moving towards each other or in the same direction at different speeds. This pattern is especially useful for:
- Finding pairs in a sorted array
- Comparing characters from both ends of a string
- Partitioning arrays
- Finding triplets or subarrays that meet certain conditions

Common examples: palindrome verification, merging sorted arrays, finding pair sums

## 2. Fast & Slow Pointers
Also known as Floyd's Cycle-Finding Algorithm or the "tortoise and hare" algorithm. This pattern uses two pointers moving at different speeds to:
- Detect cycles in a linked list or array
- Find middle elements
- Identify if a number is happy (sum of squares of digits)
- Find duplicate elements

The fast pointer moves twice as fast as the slow pointer, eventually meeting if there's a cycle.

## 3. Sliding Window
This pattern involves creating a "window" of elements and sliding it through an array or string to:
- Find subarrays that meet certain conditions
- Calculate running averages
- Find longest/shortest substrings with specific properties
- Monitor recent elements in a stream

The window can be fixed-size or variable depending on the problem requirements.

## 4. Merge Intervals
Used for problems involving overlapping intervals or ranges. Common applications include:
- Merging overlapping meetings
- Finding free time slots
- Scheduling tasks
- Handling resource allocation conflicts

Key operations: sorting intervals, comparing end of one interval with start of next

## 5. In-Place Linked List Reversal
This pattern modifies linked lists without using extra space by:
- Reversing entire lists or sublists
- Reordering elements
- Rotating lists
- Grouping elements

Uses three pointers (previous, current, next) to maintain links while reversing.

## 6. Two Heaps
Uses two heaps (usually one min-heap and one max-heap) to:
- Find medians in a data stream
- Manage different halves of sorted data
- Balance data around a specific point
- Schedule tasks with priorities

Particularly useful for problems requiring tracking of smallest and largest elements simultaneously.

## 7. K-way Merge
Used for combining multiple sorted arrays or lists into a single sorted output. Applications include:
- Merging k sorted lists
- Finding smallest elements across multiple sorted sequences
- External sorting
- Combining partial results

Often implemented using a min-heap to track the smallest current element from each list.

## 8. Top K Elements
Focuses on finding the k largest/smallest/most frequent elements using heaps. Used for:
- Finding k most frequent elements
- Finding k closest points
- Finding k largest numbers
- Finding k most competitive elements

Usually implemented with a heap of size k.

## 9. Modified Binary Search
Variations of binary search for:
- Searching in rotated sorted arrays
- Finding peaks or valleys
- Finding first/last occurrences
- Searching in nearly sorted arrays
- Finding ranges

Requires identifying the half that could contain the target.

## 10. Subsets
Pattern for generating combinations and permutations using:
- Backtracking
- Bit manipulation
- Iterative approaches

Common applications:
- Generating all possible subsets
- Finding all permutations
- Letter combinations of phone numbers
- Generating parentheses

## 11. Greedy
Makes locally optimal choices at each step, hoping to find a global optimum. Used for:
- Task scheduling
- Activity selection
- Resource allocation
- Optimization problems

Works when local optimal choices lead to global optimal solution.

## 12. Backtracking
Systematic way to try different possibilities until finding a solution. Used for:
- N-Queens problem
- Sudoku solver
- Path finding
- Generating combinations
- Constraint satisfaction problems

Involves making choices and undoing them if they don't lead to a solution.

## 13. Dynamic Programming
Solves complex problems by breaking them into simpler subproblems. Two approaches:
- Top-down (memoization)
- Bottom-up (tabulation)

Common applications:
- Optimal substructure problems
- Overlapping subproblems
- Path finding
- Resource allocation optimization

## 14. Cyclic Sort
Used when dealing with arrays containing numbers in a given range. Efficient for:
- Finding missing numbers
- Finding duplicates
- Array rearrangement
- In-place sorting of numbers from 1 to n

Works by putting each number in its correct position.

## 15. Topological Sort
For ordering vertices in a directed graph where some vertices must come before others. Used in:
- Course scheduling
- Build dependencies
- Task scheduling
- Package management

Requires directed acyclic graph (DAG).

## 16. Matrices
Techniques for 2D array manipulation including:
- Matrix traversal
- Spiral traversal
- Rotation
- State propagation
- Island problems
- Boundary traversal

Often involves careful index management and direction arrays.

## 17. Stacks
LIFO (Last In, First Out) data structure useful for:
- Expression evaluation
- Parentheses matching
- Function call tracking
- Undo operations
- Next/Previous greater/smaller element

Often used with recursive problems and depth-first traversal.

## 18. Graphs
Techniques for working with connected data structures. Common approaches:
- DFS (Depth-First Search)
- BFS (Breadth-First Search)
- Shortest path algorithms
- Cycle detection
- Connected components

Used for networks, relationships, and path-finding problems.

## 19. Tree DFS (Depth-First Search)
Tree traversal pattern using recursion or stack. Used for:
- Path sum problems
- Tree validation
- Tree modification
- Finding specific nodes/paths
- Tree comparison

Implementations: pre-order, in-order, post-order traversal.

## 20. Tree BFS (Breadth-First Search)
Level-by-level tree traversal using queue. Applications:
- Level order traversal
- Finding nearest nodes
- Tree modification by level
- Zigzag traversal
- Connecting nodes at same level

## 21. Trie
Tree-like data structure for storing strings, useful for:
- Prefix matching
- Autocomplete
- Spell checking
- Word validation
- Dictionary implementation

Efficient for string-based operations and searches.

## 22. Hash Maps
Data structure for key-value pair storage. Used for:
- Frequency counting
- Two-sum type problems
- Caching
- Quick lookups
- String matching

Provides O(1) average case access time.

## 23. Union Find
Also known as Disjoint Set, used for:
- Finding connected components
- Detecting cycles in graphs
- Network connectivity
- Minimum spanning trees
- Dynamic graph connectivity

Implements union and find operations efficiently.

## 24. Custom Data Structures
Designing specialized data structures for specific needs:
- LRU/LFU Cache
- Thread-safe structures
- Specialized containers
- Priority systems
- Hybrid data structures

Combines multiple data structures for optimal performance.

## 25. Bitwise Manipulation
Using bit operations for efficient solutions:
- Finding unique numbers
- Counting bits
- Power of two checks
- Flag manipulation
- Space optimization

Requires understanding of binary operations and bit properties.