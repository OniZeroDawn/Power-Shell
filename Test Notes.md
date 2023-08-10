## Quesion 1 
- Return the sum of the Arguments
  - $var1,var2,var3,var4
  - return $var1 + $var2 + $var3 + $var4

## Question 2
- Return the line of text from the file given by the $file argument that begins with the text specified by $line. If no line in the file begins with the $line text, return $null
  - $content = get-content $file
    foreach ($i in $content) {
      if ($i.startswith($line)) {
        return $i
        }
      return $null
    }

## Question 3
- Combine the provided $arr argument into a string separated by a / between each element and return this string
  - Return $arr -join('/')

## Question 4
- Return the processes sorted descending by their processname
  - Return get-process | sort-object -property name -descending

## Question 5
- Search the array for the first occurance of $key at column index 0 and return the value at column index 9 of the same row. Return -1 if the $key is not found
  - foreach ($i in $arr) {
      if ($i[0] -eq $key) {
        return $i[9]
      }
    }
    return -1

## Question 6
- Get todays date in year month number and day of month in yyyymmdd format
- 
