# Refactoring
- good code is between clear comprehension and speed
- you do not want a function to return undefined, instead throw an error so the coder/user knows clearly what happened.
- if a function may loop over many iterations, use a hash function, which Map and set have under the surface
- make sure each function does one thing.
- (D)on't (R)epeat (Y)ourself
- return as soon as possible in functions
- cache variables to increase readability, such as multidimensional arrays

- “Complexity is anything that makes software hard to understand or to modify." — John Outerhout
- Functional programming is a programming paradigm ... that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — Wikipedia 
- "pure" functions: returns the same result if given the same arguments (it is also referred as deterministic) and It does not cause any observable side effects
  - a pure function does not rely on a global variable not passed into the function as parameter, as a global variable may changed.
  - pure functions do not rely on random numbers
  - does not change a global variable or parameter
  - no mutability!
- Benefits
  - easier to test, given parameter always has the same result
- Immutability: instead of changing a value, create new object with new value
- pure functions + immutable data = referential transparency
- higher-order functions: takes one or more functions as arguments, or
returns a function as its result
- such as filter, map, etc