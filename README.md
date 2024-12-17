# Ruby Instance Variable Modification Bug

This repository demonstrates a common, yet subtle, bug in Ruby related to modifying instance variables through accessor methods.  The code showcases how direct assignment to the accessor method (`value =`) doesn't change the instance variable if a dedicated setter method (`value=`) is missing.  The solution shows how to correctly define a setter to address the issue.

## Bug Description

The issue arises when attempting to modify an instance variable indirectly through a getter method. Without an explicit setter, the assignment simply creates a new local variable within the method's scope, leaving the actual instance variable unchanged.

## Solution

The solution includes a properly defined setter method (`value=`) that correctly modifies the instance variable.