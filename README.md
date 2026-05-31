# AI_Preemptive_Bug_Fixing
# Objective

Use AI as a Senior C Developer to review a vulnerable linked list function, identify logical and memory safety issues, and generate a corrected implementation.

## AI Tool Used

ChatGPT

## Files

### initial_code.c
Contains the original vulnerable implementation.

### fixed_code.c
Contains the corrected implementation with proper memory checks and linked list insertion logic.

## Issues Identified

1. Logical Error
   - The traversal loop continues until the pointer becomes NULL.
   - The assignment current = new_node only modifies a local pointer.
   - The new node is never attached to the linked list.

2. Memory Safety Error
   - malloc() return value was not checked.
   - Dereferencing a NULL pointer could cause a Segmentation Fault.

## Fixes Applied

- Added NULL check after malloc().
- Properly initialized the new node.
- Correctly handled empty lists.
- Traversed to the last node.
- Linked the new node using current->next = new_node.

## Repository Structure

AI_Preemptive_Bug_Fixing/
│
├── README.md
├── initial_code.c
└── fixed_code.c
