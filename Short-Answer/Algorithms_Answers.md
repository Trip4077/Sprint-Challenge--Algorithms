#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n) -> As the input, n, grows the time complexity increases at the same rate as n 


b) O(n log n) ->

    sum = 0            O(1) -> remains constant 
    for i in range(n): O(n) -> directly correlates to size of n
      j = 1            O(1) -> remains constant
      while j < n:     O(log n) -> grows at a slower rate than n due to j's value not being related to n's value and j                                      doubling every loop instead of increasing at a steady rate
        j *= 2         O(1) -> remains constant
        sum += 1       O(1) -> remains constant


    if logic is wrong about j doubling and thus not increasing at same rate as n then compleity is O(n^2)

c) O(2n) -> O(n) -> As the input, n, grows the time complexity increases at the same rate as n

## Exercise II

This problem would be a good one to use a binary search with. The building's floors are inherently sorted and we are seeking
a single break point for the eggs. We would want to 

- start at the middle floor
- drop an egg and see if it breaks
- if it doesn't then move to the middle point between the current floor and the top of the building, repeat until egg breaks
- if egg does break move to the middle point between the current floor and the bottom of the building, repeat until egg doesnt break
- if egg breaks on floor at middle point, and doesnt break on 1 floor lower then break point found

ideally binary search runs at O(log n)