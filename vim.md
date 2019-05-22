 - Replace all the occurences of " 0x" or "0x" by "\x" (bash format for hex numbers) inside of visual area (%V)
 
    :s/\%V\ 0x\|0x/\\x/g
 
 - Count number of occurences of a regex: 
 
    :s/pattern//ng
