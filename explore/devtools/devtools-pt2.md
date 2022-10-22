# DevTools - Debugging

1. The bug was that num1 and num2 were being passed into teh functiosn as
   strings rather than integers. This was causing a string concatenation
   operation to occur rather than addition when calculating result.

2. I would fix this by using a type conversion through `parseInt()` on num1 and
   num2. This would allow an addition operation to occur, adding num1 and num2
   to calculate the correct result.
