Add your answers to the Algorithms exercises here.

## Exercise I answers
a) Runtime complexity O(n^3)
b) Runtime complexity O(n^3)
c) Runtime complexity O(n)

## Exercise II answers
You can do this in O(log n) using the algorithm and example below:

Split the initial n floors into two.

        0 1 2 3 4 5 6 7         For n=8, this is your list of floors
     0 1 2 3       4 5 6 7      Split into two, drop egg at top floor (3, 7)
                                If egg dropped at 3 survives, select list 4, 5, 6, 7 and split it.
    - -  - -      4 5    6 7    Drop egg at top floor (5, 7)
                                If egg 7 survives, f = None.
                                If egg 5 survives, select list 6 7
  - -     - -    -  -   6   7   Drop egg at 6 and 7. Return the floor that does not survive.
                                If both survive, return f = None
