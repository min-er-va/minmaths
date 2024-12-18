#Overview
This is a small program to read in a string of natural language maths and execute it.
Division is treated with the same precedence as multiplication.

Supported symbols:
+   -   *   /   (   )

#Algorithm
 - Read the expression from left to right
 - if X is a number, place X in the number stack
 - if X is an operator, evaluate operators until any of:
   - The operator stack is empty
   - the top of the operator cellar is an open paren
   - the precedence of the operator at the top of the operator stack is lower than the precedence of X
   - Then: place X in the operator stack
 - If X is an open paren, push X onto the operator stack
 - If X is a close paren:
   - Evaluate operators until an open paren is at the top of the operator stack
   - Remove the open paren from the operator stack
 - If there are no more tokens to read, evaluate the remaining operators.
