### Arrays
- List of objects
- Can contain different Data types
  - ($var).GetType() = Returns the Data Type of the variable
  - ($var).count = Returns amount of items in the array
- Created by passing multiple values to a variable
  - Ex. $array1 = 1, (Get-Date), "dog", 8.33, 7
- Create an empty array with the syntax: $array = @()
- Can create an array with a range using syntax: $array = 1..10
- Declare specific values in an array using index values
  - Ex. $array[0] = Returns the first value in the array
  - Ex. $array[-1] = Returns the last value in the array
  - Ex. $array[1..3] = Returns index values 1, 2, and 3
- ## Jagarray
  - An array within the array
  - $jagarray = "joe", "jim", "jin", (1, ('apple', 'pear'), 3), "jay"
    - $jagarray[3] = 1
    - $jagarray[3][2] = 3
    - $jagarray[3][1][0] = 'apple'
- Can append values to an array using +=
  - Ex. $a += @(4, 5, 6)
- ## Multi-Dimensional Arrays
  - $mdarray = @((1, 2, 3), (4, 5, 6), (7, 8, 9))
  - $mdarray[1][0] = 5


