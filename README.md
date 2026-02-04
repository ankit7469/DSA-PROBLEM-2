# 2. DSA-PROBLEM --

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
 maximum letter height
 total number of characters in the word

🧩 Core Concepts

• Character-to-Index Mapping: Letters are mapped to array indices (a → 0, b → 1, … z → 25).
• Maximum Selection: Only the tallest letter determines the height.
• Length Calculation: Word length represents the width.
• Area Formula: Area = max height × word length.
• Efficiency: Single pass through the word is sufficient.

------------------------------------------------------------------------------------------------------------------
## Problem 2. Utopian Tree
--------------------------------------------------------------------------------------------------------------------

🎯 Purpose

To calculate the height of the Utopian Tree after a given number of growth cycles.

🔑 Key Insight

The tree grows in two alternating phases:
Spring: the height doubles
Summer: the height increases by 1
The final height depends on applying these phases in order for each cycle.

🧠 Concept

The tree starts with an initial height of 1.
Growth happens cyclically:

First cycle is Spring
Second cycle is Summer
This pattern repeats for all cycles
The height is updated step-by-step based on the type of cycle.

🧩 Core Concepts

• Initial State: Tree height starts at 1
• Alternating Growth: Spring (×2), Summer (+1)
• Cycle-Based Logic: Growth depends on cycle number
• Iteration: Each cycle updates the height
• Deterministic Process: Same input always produces the same height

---------------------------------------------------------------------------------------------------------------------------
