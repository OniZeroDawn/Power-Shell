<# 1 #>
function q1($var1,$var2,$var3,$var4) {
    <# Return the product of the arguments #>
    return $var1*$var2*$var3*$var4
}





function q2($arr,$rows,$cols,$key) {
    <# Search the 2 dimensional array for the first occurance of key at column index 0
       and return the value at column index 9 of the same row.
       Return -1 if the key is not found.
    #>
    foreach ($i in $arr) {
        if ($i[0] -eq $key) {
            return $i[9]
        }
    }
    return -1
}










function q3 {
    <# In a loop, prompt the user to enter positive integers one at time.
       Stop when the user enters a -1. Return the maximum positive
       value that was entered."
	#>
    $arr=@()
    while (($num = Read-Host -Prompt "Enter a positive integer") -gt -1) {
        $arr = ($arr += @($num))
        }
        return $arr[0] | sort -Descending
    
}
or
$vals = @()
do { 
  $val = read-host
  if($val -ne -1) {
    $vals += $val
  }
}until($val -eq  -1









function q4($filename,$whichline) {
    <# Return the line of text from the file given by the \`$filename
	   argument that corresponds to the line number given by `$whichline.
	   The first line in the file corresponds to line number 0."
	#>
    $Content = Get-Content $filename
    return $Content[$whichline]
    
}








function q5($path) {
    <# Return the child items from the given path sorted
       ascending by their Name
	#>
    return Get-ChildItem -Path "$path" | Sort-Object 
}











function q6 {
    <# Return the sum of all elements provided on the pipeline
	#>
    $sum = 0
    foreach ($a in $input) {
    $sum += $a
    }
    return $sum
}















function q7 {
	<# Return only those commands whose noun is process #>
    return Get-Command -Noun process
}
















function q8($adjective) {
    <# Return the string 'PowerShell is ' followed by the adjective given
	   by the `$adjective argument
	#>
    return "PowerShell is $adjective"    
}














function q9($addr) {
	<# Return `$true when the given argument is a valid IPv4 address,
	   otherwise return `$false. For the purpose of this function, regard
	   addresses where all octets are in the range 0-255 inclusive to
	   be valid.
	#>
    foreach($octet in $addr.split(".")) {
        if([int]$octet -lt 0 -or [int]$octet -gt 255) {
            return $false
        }
    }
    return $true
}













function q10 ($filepath,$lasthash) {
    <# Return `$true if the contents of the file given in the
       `$filepath argument have changed since `$lasthash was
       computed. `$lasthash is the previously computed SHA256
       hash (as a string) of the contents of the file. #>
        $hash = Get-FileHash -Algorithm SHA256 $filepath
        return $hash.hash -ne $lasthash    
}
