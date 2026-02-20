# 2. DSA PROBLEMS (PYTHON) - 

--------------------------------------------------------------------------------------------------------
## Probelm 1. Designer PDF Viewer
--------------------------------------------------------------------------------------------------------

🎯 Purpose 

To calculate the area occupied by a highlighted word in a PDF viewer based on the heights of its letters.

🔑 Key Insight

The height of the highlighted word is determined by the tallest letter in the word, not by all letters.
The width of the highlighted area depends on the number of letters in the word.

🧠 Concept

- Each lowercase alphabet letter (a to z) has a predefined height stored in an array.
- To find the highlighted area:
- Each character in the word is mapped to its corresponding height.
- The maximum height among these characters is selected.
- The final area is calculated using the product of:
  Maximum letter height
  Total number of characters in the word

🧩 Core Concepts

- Character-to-Index Mapping: Letters are mapped to array indices (a → 0, b → 1, … z → 25).
- Maximum Selection: Only the tallest letter determines the height.
- Length Calculation: Word length represents the width.
- Area Formula: Area = max height × word length.
- Efficiency: Single pass through the word is sufficient.

------------------------------------------------------------------------------------------------------------------
## Problem 2. Utopian Tree
--------------------------------------------------------------------------------------------------------------------

🎯 Purpose

To calculate the height of the Utopian Tree after a given number of growth cycles.

🔑 Key Insight

- The tree grows in two alternating phases:
 Spring: the height doubles
 Summer: the height increases by 1
- The final height depends on applying these phases in order for each cycle.

🧠 Concept

- The tree starts with an initial height of 1.
Growth happens cyclically:

- First cycle is Spring
- Second cycle is Summer
- This pattern repeats for all cycles
- The height is updated step-by-step based on the type of cycle.

🧩 Core Concepts

- Initial State: Tree height starts at 1
- Alternating Growth: Spring (×2), Summer (+1)
- Cycle-Based Logic: Growth depends on cycle number
- Iteration: Each cycle updates the height
- Deterministic Process: Same input always produces the same height

---------------------------------------------------------------------------------------------------------------------------
## Probelm 3. Angry Professor
---------------------------------------------------------------------------------------------------------------------------
🎯 Purpose

To decide whether a class is cancelled or not based on the number of students who arrive on time.

🔑 Key Insight

- Only students who arrive on time or early (arrival time ≤ 0) are counted.
- If the number of such students is less than the required threshold, the class is cancelled.

🧠 Concept

- Each test case represents one class.
For that class:
- Student arrival times are checked.
- Students with arrival time ≤ 0 are considered present on time.
- The class is cancelled if the count of on-time students is strictly less than the threshold value.

🧩 Core Concepts

- On-Time Condition: Arrival time ≤ 0
- Threshold Logic: Minimum number of students required to conduct the class
- Comparison Rule: Cancel class when on-time count < threshold
- Multiple Test Cases: Each test case is evaluated independently
- Binary Decision: Output is either cancellation or continuation

-----------------------------------------------------------------------------------------------------------
## 4. Problem - Beautiful days at the movies 
-----------------------------------------------------------------------------------------------------------

🎯 Purpose

To count how many numbers within a given range are beautiful days, based on a divisibility condition involving the number and its reverse.

🔑 Key Insight

A day is considered beautiful if the absolute difference between the number and its reversed form is exactly divisible by a given value k.

🧠 Concept

For each number in the range:

- The number is reversed digit by digit (works for any number of digits).
- The absolute difference between the original number and its reverse is calculated.
- If this difference is divisible by k, the day is counted as beautiful.
- This process is repeated for all numbers in the given range.

🧩 Core Concepts

-  Digit Reversal: Reversing a number using repeated modulo and division
-  Absolute Difference: Ensures comparison is always non-negative
-  Divisibility Check: Uses modulo operation to test exact division
-  Range Iteration: Each number in the interval is evaluated
-  Generality: Logic works for numbers with any number of digits

---------------------------------------------------------------------------------------------------------------------
## 5. Problem - Viral Advertising
---------------------------------------------------------------------------------------------------------------------

🎯 Purpose

To calculate the total number of likes an advertisement receives over a given number of days based on a fixed sharing pattern.

🔑 Key Insight

Each day:

- Only half of the people who see the advertisement like it.
- Every person who likes the ad shares it with 3 new people the next day.
- Likes are cumulative and added day by day.

🧠 Concept

The process starts with an initial number of people who see the advertisement.
For each day:
- The number of likes is calculated.
- These likes are added to a running total.
- The advertisement is shared again based on the number of likes, creating a repeating cycle.
- This cycle continues for the given number of days.

🧩 Core Concepts

- Integer Division: Likes are calculated using floor division
- Cumulative Sum: Likes are added day by day
- Iteration: Each day depends on the previous day’s result
- State Update: Next day’s audience is based on current likes
- Deterministic Pattern: Same input always gives the same output

---------------------------------------------------------------------------------------------------------------
## 6. Prroblem - Save The Prisoner
-------------------------------------------------------------------------------------------------------------

🎯 Purpose

To determine which prisoner receives the last candy when candies are distributed one-by-one in a circular arrangement starting from a given prisoner.

🔑 Key Insight

The distribution follows circular counting.
The position of the last candy can be calculated using modulo arithmetic instead of simulating each step.

🧠 Concept

- Prisoners are numbered from 1 to n (1-based numbering).
- Distribution starts at prisoner s.
- The first candy goes directly to the starting prisoner, so only the remaining candies cause movement.
- To work cleanly with modulo, the starting position is converted to 0-based indexing.
- Modulo keeps the count within the circle of prisoners.

🧩 Core Concepts

- 1-based to 0-based Conversion: s - 1 aligns seat numbering with modulo/indexing
- Movement as Steps: m - 1 represents steps because the first candy is already given
- Circular Counting: Modulo (% n) wraps positions within the prisoner circle
- Index-to-Seat Mapping: A modulo result of 0 corresponds to the last prisoner
- Efficiency: Constant-time calculation without simulation

----------------------------------------------------------------------------------------------------------------
## 7. Problem - Circular Array Rotation
----------------------------------------------------------------------------------------------------------------

🎯 Purpose

To efficiently answer queries on an array after performing a specified number of circular rotations.

🔑 Key Insight

- Instead of rotating the array for every query, the array is rotated once, and then queries are answered using index access.
- Modulo operation helps handle extra rotations and keeps the rotation within array bounds.

🧠 Concept

- The array undergoes right circular rotation k times.
- A right rotation moves the last element to the front.
- Since rotations are circular, performing k % n rotations gives the same result as k rotations.
- After rotation, each query simply asks for the element at a given index.

🧩 Core Concepts

- Circular Rotation: Elements wrap around instead of being lost
- Modulo Optimization: k % n avoids unnecessary full rotations
- Right Rotation Logic: Last element moves to index 0
- Query Handling: Each query retrieves an element by index
- Time Efficiency: Rotation done once, queries answered in O(1) time

----------------------------------------------------------------------------------------------------
## 8. Problem - Sequence Rotation
----------------------------------------------------------------------------------------------------

🎯 Purpose

To understand how and why index conversion (+1) is used when solving the Sequence Equation problem involving permutations.

🔑 Key Insight

- Python lists use 0-based indexing, while the Sequence Equation problem uses 1-based numbering.
- The +1 adjustment is required only to match the problem’s numbering system, not because of any change in data.

🧠 Concept

- The permutation p represents a mapping where positions start from 1.
- Python internally treats list positions starting from 0.
- When a position is obtained using methods like index(), it is returned in 0-based form.
- To correctly interpret this position in the context of the problem, +1 is added.
- The adjustment is applied only when converting from Python indexing to problem-defined numbering.

🧩 Core Concepts

- 0-based Indexing: Python lists start from index 0
- 1-based Numbering: Problem definitions often start counting from 1
- Index Conversion: +1 converts a Python index into a problem position
- Conditional Usage: +1 is used only when the problem explicitly requires 1-based positions
- Clarity of Context: Indexing depends on whether the output is for computation or for problem-defined results.

---------------------------------------------------------------------------------------------------------------------
## 9. Problem - Jumping on the Clouds
---------------------------------------------------------------------------------------------------------------------

🎯 Purpose

To calculate the remaining energy after performing fixed-size jumps on a circular array of clouds.

🔑 Key Insight

- Each jump reduces energy by 1 unit, and landing on a thundercloud reduces an additional 2 units.
- The movement is circular, meaning after the last cloud, the jump continues from the first cloud.

🧠 Concept

- The player starts at index 0 with an initial energy of 100.
- The player jumps exactly k steps at a time.
- The position is updated using modulo arithmetic to maintain circular movement.
  
- After every jump:
- Energy decreases by 1.
- If the landed cloud is a thundercloud (1), energy decreases by 2 more.
- The process continues until the player returns to index 0.

🧩 Core Concepts

- Circular Movement: (current_index + k) % n ensures wrapping around
- Energy Deduction Rule: −1 per jump, −2 extra for thundercloud
- Loop Termination: Stop when index becomes 0 again
- Modulo Arithmetic: Handles circular indexing
- State Update Logic: Each jump updates position and energy

--------------------------------------------------------------------------------------------------------------
## 10. Problem - Find Digits
-------------------------------------------------------------------------------------------------------------

🎯 Purpose

To determine how many digits of a given number evenly divide the number itself.

🔑 Key Insight

- Each digit of the number is checked individually.
- A digit is counted only if:

: It is not zero, and
: The original number is exactly divisible by that digit.

🧠 Concept

- The number is broken down into its individual digits.
- Each digit is tested against the original number using the modulo operation.
- Division by zero is avoided by skipping the digit 0.
- The final result is the count of digits that divide the number evenly.

🧩 Core Concepts

- Digit Extraction: Using modulo (%) and integer division (//)
- Original Value Preservation: Store the number before modifying it
- Divisibility Check: number % digit == 0
- Zero Handling: Avoid division by zero
- Iteration: Process each digit independently.

--------------------------------------------------------------------------------------------
## 11. Problem - Extra long factorial 
--------------------------------------------------------------------------------------------
🎯 Purpose

To compute the factorial of a large number where the result exceeds the range of standard integer data types.

🔑 Key Insight

- Factorial values grow extremely fast.
- For large inputs, the result cannot be stored in normal fixed-size integer types, so we rely on languages or techniques that support arbitrary precision arithmetic.

🧠 Concept

- The factorial of a number n is the product of all positive integers from 1 to n.
- For large n, the result becomes very large (hundreds or thousands of digits).
- Instead of worrying about overflow, we use built-in big integer handling.
- The computation is typically done using iterative multiplication from 1 to n.

🧩 Core Concepts

- Factorial Definition: n! = n × (n-1) × ... × 1
- Arbitrary Precision: Handling numbers beyond fixed integer limits
- Iterative Multiplication: Loop-based factorial calculation
- Time Complexity: O(n) multiplications
- Large Number Growth: Factorials increase exponentially in size

-------------------------------------------------------------------------------------------------------------------------
## 12. Problem - Append and Delete
-------------------------------------------------------------------------------------------------------------------------

🎯 Purpose

To determine whether one string can be converted into another using exactly k operations, where each operation is either:

- Appending a character to the end, or
- Deleting the last character.

🔑 Key Insight

The transformation depends on:
1. The common prefix shared by both strings.
2. The minimum required operations to remove unmatched characters and append new ones.
3. Whether any extra operations can be safely wasted.

🧠 Concept

- First, identify the longest common prefix of both strings.
- Characters beyond the common prefix in the first string must be deleted.
- Characters beyond the common prefix in the second string must be appended.
- Calculate the minimum required operations.
- Compare it with k to determine feasibility.
- Extra operations can be canceled in pairs (delete + append), or handled using a full reset scenario.

🧩 Core Concepts

- Common Prefix Identification
- Minimum Operation Calculation
- Exact Operation Constraint (k)
- Parity Check: Extra operations must be even to cancel out
- Full Reset Condition: If k is large enough, full deletion and reconstruction is possible
- Edge Case Handling

---------------------------------------------------------------------------------------------------
## 13. Problem - Sherlock and Squares
---------------------------------------------------------------------------------------------------
📌 Description

This problem focuses on finding the number of perfect square numbers between two given integers a and b (inclusive).
A perfect square is a number that can be written as:


Examples:

1 = 1²
4 = 2²
9 = 3²
16 = 4²

🎯 Objective

Given multiple test cases:
- Input two integers a and b
- Determine how many perfect squares exist in the range [a, b]

🧠 Core Concept

- Instead of checking every number between a and b (brute force approach), we use a mathematical optimization.
Key Insight:
- If a number x² lies between a and b, then:
𝑎 ≤ 𝑥 ≤ 𝑏a ≤x≤ b
- So instead of iterating through all numbers in the range, we:
- Compute the smallest integer ≥ √a
- Compute the largest integer ≤ √b
- Count the integers between them

📐 Mathematical Formula -

- start=⌈𝑎⌉
- end=⌊𝑏⌋
- count=𝑒𝑛𝑑−𝑠𝑡𝑎𝑟𝑡+1
If start > end, then count = 0.

⚡ Time Complexity

- Brute Force Approach → O(b - a)
- Optimized Mathematical Approach → O(1)

🚀 Learning Outcome - 

By solving this problem, you understand:

- How to identify perfect squares
- How to use square root properties effectively
- How to optimize range-based problems
- Why mathematical reasoning is better than brute force in large constraints
- How to avoid Time Limit Exceeded (TLE) errors

📚 Topic Covered

- Math & Number Theory
- Square Root Concepts
- Range Optimization
- Competitive Programming Thinking

------------------------------------------------------------------------------------
## 14. Library Fine
------------------------------------------------------------------------------------

📌 Description

- This problem determines the library fine based on how late a book is returned compared to its due date.

You are given two dates:
- Return Date → The actual date when the book was returned
- Due Date → The last allowed date to return the book
- The goal is to calculate the fine using logical date comparison.

🎯 Objective

Check whether the book was returned:
- On time
- Late by days
- Late by months
- Late by year
- And apply the correct fine rule.

🧠 Core Concept

- Dates are not compared randomly.
- They must be compared in a hierarchical order:
- Year → Month → Day
This means:

- The year is checked first.
- If the year is the same, then the month is checked.
- If the month is also the same, then the day is checked.
- This structured comparison ensures accurate results.

📜 Fine Rules (Logic Based) - 

1️⃣ If the book is returned after the due year:
A fixed maximum fine is charged.

2️⃣ If the book is returned in the same year but after the due month:
A fine is charged based on how many months late it is.

3️⃣ If the book is returned in the same year and same month but after the due day:
A fine is charged based on how many days late it is.

4️⃣ If the book is returned on time or before the due date:
No fine is charged.

⚠ Important Understanding

- A later year automatically means the highest fine.
- Month comparison only matters if the year is the same.
- Day comparison only matters if both year and month are the same.
- If the return date is earlier than the due date, there is no penalty.

🚀 Learning Outcome

- From this problem, you learn:
- How to compare structured data logically
- Importance of decision hierarchy
- How real-world rules translate into condition-based logic
- How small ordering mistakes can cause incorrect outputs

📚 Topics Covered

- Conditional Thinking
- Logical Flow Control
- Date Comparison Strategy
- Problem Breakdown

-------------------------------------------------------------------------------------------
## 15. Problem - Cut the sticks 
-------------—----------—---------------—-----------------—------------—------------------—

🎯 Purpose

To determine how many sticks remain before each cutting round when repeatedly reducing all sticks by the smallest available length.

🔑 Key Insight

In every round:
- The smallest stick length is identified.
- That minimum length is subtracted from all sticks.
- Sticks that become zero are removed.
- The count of sticks before each cut is recorded.
- The process continues until no sticks remain.

🧠 Concept

- The problem simulates a repetitive cutting process.
For each round:

- Count the current number of sticks.
- Reduce all sticks by the smallest length.
- Remove sticks that reach zero.
- Repeat with the updated set.
- Each round effectively eliminates one unique stick length level.

🧩 Core Concepts

- Iterative Simulation: Process repeats until the list becomes empty
- Minimum Extraction: Smallest element determines the cut size
- State Update: Stick lengths change after every round
- Filtering: Zero-length sticks are removed
- Pattern Observation: Each new minimum creates a new round
- List Manipulation: Updating and shrinking the data structure

🚀 Learning Outcome

- Understand how iterative reduction problems work
- Learn how dynamic lists change during execution
- Strengthen logic for simulation-based problems
- Recognize when sorting or pattern observation can optimize the approach
- Improve understanding of state-driven iteration

-----------------------------------------------------------------------------------------------------------------------------
## 16. Non divisible Subset
-----------------------------------------------------------------------------------------------------------------------------

🎯 Purpose

To find the largest possible group of numbers from an array such that no two numbers in the group add up to a multiple of k.

🔑 Key Insight (Simple Understanding)

When two numbers are added:

- If their sum becomes exactly divisible by k, they cannot both stay in the subset.
- Such numbers “conflict” with each other.
- So the goal is to avoid keeping conflicting numbers together.

🧠 Concept (Easy Explanation)

- First, look at each number and see what remains when it is divided by k.
- Numbers that leave certain remainders will conflict with numbers that leave specific other remainders.
- If two remainder groups conflict, you cannot fully take both groups.
- So from each conflicting pair of groups, you choose the larger group.

 Some special cases:

- Numbers perfectly divisible by k can only contribute one element.
- In some cases, one middle remainder group can also contribute only one element.
- The idea is to choose numbers smartly so that no bad pair is formed.

🧩 Core Concepts

- Divisibility checking
- Remainder grouping
- Conflict detection
- Smart selection instead of checking every pair
- Avoiding brute force

🚀 Learning Outcome

- After solving this problem, you will:
- Understand how to avoid conflicting pairs
- Learn to think in groups instead of checking all combinations
- Improve logical reasoning in subset problems
- Recognize patterns in divisibility-based challenges
- Strengthen optimization thinking in DSA

-------------------------------------------------------------------------------------------------
## 17. Problem - Repeated String
-------------------------------------------------------------------------------------------------

🎯 Purpose

To calculate how many times the character 'a' appears in the first n characters of an infinitely repeating string.

🔑 Key Insight

- Instead of actually repeating the string many times, we observe a pattern:
- The string repeats in complete blocks.
- After full repeats, a small leftover part may remain.
- We only need to count 'a' in:
- The full repeated blocks
- The remaining partial block
- No need to build a large string.

🧠 Concept (Simple Explanation)

- Count how many 'a' are present in the original string.
- Determine how many full times the string fits into n.
- Multiply the count of 'a' by the number of full repeats.
- Check the leftover characters and count 'a' in that small part.
- Add both counts to get the final answer.
- This avoids creating a huge repeated string.

🧩 Core Concepts

- Pattern observation
- Integer division
- Remainder handling
- Character counting
- Avoiding unnecessary memory usage
- Optimization for very large inputs

🚀 Learning Outcome

- After solving this problem, you will:
- Learn how to handle very large constraints efficiently
- Understand why brute-force repetition is not practical
- Apply mathematical thinking instead of physical simulation
- Improve optimization skills in competitive programming
- Strengthen understanding of pattern-based counting problems

-------------------------------------------------------------------------------------------
## 18. Problem - Jumping on the clouds
-------------------------------------------------------------------------------------------

🎯 Purpose

To determine the minimum number of jumps required to reach the last cloud, while avoiding unsafe clouds.

🔑 Key Insight

- You can jump either 1 step or 2 steps at a time.
- You cannot land on a thunder cloud (represented by 1).
- You should always try to jump 2 steps first (if safe) to minimize total jumps.
- The goal is to reach the last cloud in the fewest possible moves.

🧠 Concept (Simple Explanation)

- Start from the first cloud (index 0).
At each step:

- Check if jumping 2 clouds ahead is possible and safe.
- If yes, take the 2-step jump.
- Otherwise, take a 1-step jump.
- Count each jump.
- Stop when you reach the last cloud.
- This works because taking the longest safe jump always reduces the total number of moves.

🧩 Core Concepts

- Index-based traversal
- Greedy approach (always choose the largest safe move)
- Boundary checking (avoid going outside the array)
- Conditional decision making
- Loop control using a pointerr

🚀 Learning Outcome

- After solving this problem, you will:
- Understand how greedy decisions reduce steps
- Learn how to control movement using indices
- Practice safe boundary checking in arrays
- Improve logic building for traversal problems
- Strengthen understanding of simulation-based DSA problems

----------------------------------------------------------------------------------------------------
## 19. Problem - Equalize the problem
----------------------------------------------------------------------------------------------------

🎯 Purpose

To determine the minimum number of deletions required so that all elements in the array become equal.

🔑 Key Insight

- To make all elements equal:
- The best strategy is to keep the element that appears the most times.
- Delete all other elements.
- Keeping the most frequent element minimizes deletions.

🧠 Concept (Simple Explanation)

- Count how many times each element appears.
- Identify the element with the highest frequency.
- Calculate how many elements are different from it.
- Delete those different elements.
- Instead of trying to convert all elements into every possible value, we simply choose the value that already appears the most.

🧩 Core Concepts

- Frequency counting
- Hash map (dictionary) usage
- Maximization strategy
- Greedy decision making
- Minimizing deletions through optimal selection

🚀 Learning Outcome

- After solving this problem, you will:
- Understand how frequency analysis simplifies array problems
- Learn how to reduce transformation problems into deletion problems
- Recognize greedy optimization strategies
- Strengthen counting and hashing techniques
- Improve logical reasoning in array manipulation challenges

---------------------------------------------------------------------------------------
## 20. Problem - Queen's attack II 
---------------------------------------------------------------------------------------
