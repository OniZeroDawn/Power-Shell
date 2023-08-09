## Arrays
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
- ### Jagarray
  - An array within the array
  - $jagarray = "joe", "jim", "jin", (1, ('apple', 'pear'), 3), "jay"
    - $jagarray[3] = 1
    - $jagarray[3][2] = 3
    - $jagarray[3][1][0] = 'apple'
- Can append values to an array using +=
  - Ex. $a += @(4, 5, 6)
- ### Multi-Dimensional Arrays
  - $mdarray = @((1, 2, 3), (4, 5, 6), (7, 8, 9))
  - $mdarray[1][0] = 5

## Hash Tables
- Create a hash table using @{}
  - $myHash = @{First = "John"; Last = "Doe"; Mid = "Bon"; Age = 35}
- Return the values by their names
  - Ex. $myHash["First"] = Returns "John"
- $myHash.keys returns all names or keys in the Hash
- $myHash.values returns all the values in the hash(

## Script Blocks
- A variable that contains commands
- Syntax for this would be: $myblock = {get-service | format-table name, status}
- To call a script block use the syntax: & $myblock

## Sorting and Grouping
- The syntax to sort items is: Sort-Object
- When wanted to sort something by a specific parameter such as size the syntax will be: Sort-Object -Property Length
  - Sort Length also works
- If the list should be in descending order use the syntax: sort -Descending

## Selecting Objects 
- Select-Object will allow you to choose the output of a command

## Where Object

## Get Unique
- Before using make sure to sort-object

## Creating Objects
- The syntax to create an object is: $myTruck = new-object object
- To add prperties use syntax: add-member -MemberType NoteProperty -name Color -value red -InputObject $myTruck

## Adding Methods
- The syntax is add-member -MemberType ScriptMethod -InputObject $mytruck -name drive -value { "going on a road trip"}

## Conditions and Comparison Operators
- Wild card statements can only be used with -like and -notlike
- The operator -match and -notmatch can use regex
- To see if a string is in an array you can use -contains and -in
- Operators for integers can be -lt -eq - mt -le -me
- Using -and you can print something that requires two arguments to be true
- You can use if statements but just using "if"
- When executing if-else statements both arguments must be enclose in {}
- Switch statements relay on the variable being constantly changing
- To use a for each loop use the command ForEach-Object {}
- While loops are formated the same way as they are in python
- Do until will iterate through the loop untile the condition is met

## Reading and Writing to Files
- Use Get-Content to read a file
- Use Set-Content -path " " -value " " to write to a file
- Add-Content -path " " -value " " to append to the file
