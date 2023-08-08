### COMMAND TO GET TO WINDOWS GUI
- xfreerdp /u:student /v:10.50.22.236 -dynamic-resolution +glyph-cache +clipboard
- Run windows powershell ISE in adiministrator mode

### Power Shell
- Uses a verb-noun structure
- Can run external programs
  - PS offers commands to do the same as these external programs

### Help Command
- get-help will bring up the help file
- update-help will bring up the newest help file
- get-help 'command' will pull up basic help file for the command
- get-help 'command' -full will pull up the full help page including examples
- get-help 'command' -examples will bring up only examples
- get-help \*string* will find all commands with the specified string in it

### Properties
- (Get-Process).ProcessName: Returns an array of the names
- Get-Preocess | Get-Member: Returns all properties and methods aswell as aliases
- There are built in variables within PS

### Variables
- Seen by running Get-Variable
- Get-ChildItem variable: is another way to see all the variables
- Set-Variable c 6 will set c to the value of 6
  - Can also set them as $c = 6
  - Multiple variables can be set with $c, $d, $e = 8, "cat", 6
- test-path variable:d will return whether or not a variable is in use
- write-host "this is a $d" will print "this is a cat" to the host
- write-host 'this is a $d' will print 'this is a $d' to the host
- Variables can be used in other variables
 
