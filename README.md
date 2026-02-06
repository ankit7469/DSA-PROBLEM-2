
# 2. DSA-PROBLEM 

-----------------------------------------------------
## Probelm 1. Designer PDF Viewer
-----------------------------------------------------

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

• Digit Reversal: Reversing a number using repeated modulo and division
• Absolute Difference: Ensures comparison is always non-negative
• Divisibility Check: Uses modulo operation to test exact division
• Range Iteration: Each number in the interval is evaluated
• Generality: Logic works for numbers with any number of digits
