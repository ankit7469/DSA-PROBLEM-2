# 2. DSA PROBLEMS 

---------------------------------------------------------------------------------------------------------
## Probelm 1. Designer PDF Viewer
---------------------------------------------------------------------------------------------------------

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

------------------------------------------------------------------------------------------------------------
## 4. Problem - Beautiful days at the movies 
------------------------------------------------------------------------------------------------------------

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
---------------------------------------------------------------------------------------------------------------

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
