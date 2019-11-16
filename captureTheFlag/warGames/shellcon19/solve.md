# Shellcon 19 Capture The Flag
Had an awesome ctf weekend last week, I did not make any prominent writeups for all the solves. This is just an update from what I still remember

- I participated alone and did not win this time. Ended around the 6th place.

* Web - ByAnyOtherName

* Sudoku Solver - Programming
  - A programming challenge to solve sudoku repeatedly until you get the flag
  - As usual, used the pwntools frame from my gists at `https://gist.github.com/Srinivas11789/8376943807d42d118a1f015f20882e4b`
  - For the Sudoku Solver algorithm, I reused some of the best leetcode solution from HARD category sudoku problem ( solutions from leetcode discuss )
  - I spent all night trying different algorithms as they did not work and solved only a few of the sudoku puzzles and failed sometime in between.....:-(

```
srimbp-623:Submarine Parts sri$ python sudoku.py 
[+] Opening connection to topwing.shellcon.games on port 7071: Done
-------------------------
['-------------------------']

| 1 9 _ | 4 5 8 | 2 _ _ |
| 8 _ _ | _ _ _ | ? 4 _ |
| _ 7 _ | 9 _ 2 | 5 _ _ |
-------------------------
| _ _ 2 | 7 4 1 | 9 8 _ |
| _ 3 _ | _ _ _ | 6 7 _ |
| _ _ _ | 8 _ _ | _ _ _ |
-------------------------
| 2 _ _ | 1 _ 5 | _ _ 6 |
| 5 _ _ | _ 9 _ | _ _ 4 |
| _ _ 7 | _ 3 _ | 8 1 _ |
-------------------------

['\r', '| 1 9 _ | 4 5 8 | 2 _ _ |\r', '| 8 _ _ | _ _ _ | ? 4 _ |\r', '| _ 7 _ | 9 _ 2 | 5 _ _ |\r', '-------------------------\r', '| _ _ 2 | 7 4 1 | 9 8 _ |\r', '| _ 3 _ | _ _ _ | 6 7 _ |\r', '| _ _ _ | 8 _ _ | _ _ _ |\r', '-------------------------\r', '| 2 _ _ | 1 _ 5 | _ _ 6 |\r', '| 5 _ _ | _ 9 _ | _ _ 4 |\r', '| _ _ 7 | _ 3 _ | 8 1 _ |\r', '-------------------------\r', '']
([['1', '9', '6', '4', '5', '8', '2', '3', '7'], ['8', '2', '5', '3', '7', '6', '1', '4', '9'], ['3', '7', '4', '9', '1', '2', '5', '6', '8'], ['6', '5', '2', '7', '4', '1', '9', '8', '3'], ['4', '3', '8', '5', '2', '9', '6', '7', '1'], ['7', '1', '9', '8', '6', '3', '4', '5', '2'], ['2', '4', '3', '1', '8', '5', '7', '9', '6'], ['5', '8', '1', '6', '9', '7', '3', '2', '4'], ['9', '6', '7', '2', '3', '4', '8', '1', '5']], '1', '16')
Sending ==> 1
YAY
['YAY']

-------------------------
| 3 _ 1 | _ _ _ | 4 6 _ |
| 9 5 _ | 6 _ _ | _ _ 2 |
| _ 2 _ | _ 4 _ | _ 3 5 |
-------------------------
| 5 _ _ | 8 3 7 | _ 1 _ |
| _ 8 _ | _ 1 _ | _ _ 3 |
| _ 4 _ | _ _ 5 | 7 _ 9 |
-------------------------
| 8 9 _ | 4 7 ? | _ 2 _ |
| _ _ 6 | _ 5 2 | 8 _ 7 |
| _ _ 2 | 1 9 _ | _ 4 _ |
-------------------------

['\r', '-------------------------\r', '| 3 _ 1 | _ _ _ | 4 6 _ |\r', '| 9 5 _ | 6 _ _ | _ _ 2 |\r', '| _ 2 _ | _ 4 _ | _ 3 5 |\r', '-------------------------\r', '| 5 _ _ | 8 3 7 | _ 1 _ |\r', '| _ 8 _ | _ 1 _ | _ _ 3 |\r', '| _ 4 _ | _ _ 5 | 7 _ 9 |\r', '-------------------------\r', '| 8 9 _ | 4 7 ? | _ 2 _ |\r', '| _ _ 6 | _ 5 2 | 8 _ 7 |\r', '| _ _ 2 | 1 9 _ | _ 4 _ |\r', '-------------------------\r', '']
([['3', '7', '1', '5', '2', '9', '4', '6', '8'], ['9', '5', '4', '6', '8', '3', '1', '7', '2'], ['6', '2', '8', '7', '4', '1', '9', '3', '5'], ['5', '6', '9', '8', '3', '7', '2', '1', '4'], ['2', '8', '7', '9', '1', '4', '6', '5', '3'], ['1', '4', '3', '2', '6', '5', '7', '8', '9'], ['8', '9', '5', '4', '7', '6', '3', '2', '1'], ['4', '1', '6', '3', '5', '2', '8', '9', '7'], ['7', '3', '2', '1', '9', '8', '5', '4', '6']], '6', '65')
Sending ==> 6
YAY
['YAY']

-------------------------
| _ 8 _ | 1 2 _ | _ _ _ |
| 5 _ _ | _ _ _ | 6 ? _ |
| _ 3 9 | _ _ _ | 7 8 _ |
-------------------------
| _ 4 _ | 5 _ _ | _ 9 2 |
| 6 1 _ | _ 8 _ | _ _ _ |
| _ 9 5 | 2 7 _ | 1 3 _ |
-------------------------
| 1 _ _ | 7 _ 9 | 5 _ _ |
| _ 6 _ | _ _ 5 | 2 _ _ |
| 7 _ 3 | 6 1 _ | _ 4 8 |
-------------------------

['\r', '-------------------------\r', '| _ 8 _ | 1 2 _ | _ _ _ |\r', '| 5 _ _ | _ _ _ | 6 ? _ |\r', '| _ 3 9 | _ _ _ | 7 8 _ |\r', '-------------------------\r', '| _ 4 _ | 5 _ _ | _ 9 2 |\r', '| 6 1 _ | _ 8 _ | _ _ _ |\r', '| _ 9 5 | 2 7 _ | 1 3 _ |\r', '-------------------------\r', '| 1 _ _ | 7 _ 9 | 5 _ _ |\r', '| _ 6 _ | _ _ 5 | 2 _ _ |\r', '| 7 _ 3 | 6 1 _ | _ 4 8 |\r', '-------------------------\r', '']
([['4', '8', '6', '1', '2', '7', '3', '5', '9'], ['5', '7', '1', '3', '9', '8', '6', '2', '4'], ['2', '3', '9', '4', '5', '6', '7', '8', '1'], ['3', '4', '7', '5', '6', '1', '8', '9', '2'], ['6', '1', '2', '9', '8', '3', '4', '7', '5'], ['8', '9', '5', '2', '7', '4', '1', '3', '6'], ['1', '2', '8', '7', '4', '9', '5', '6', '3'], ['9', '6', '4', '8', '3', '5', '2', '1', '7'], ['7', '5', '3', '6', '1', '2', '9', '4', '8']], '2', '17')
Sending ==> 2
YAY
['YAY']

-------------------------
| 8 _ _ | _ 9 _ | 7 _ _ |
| 3 5 ? | 1 _ _ | _ 4 6 |
| _ _ 4 | 6 _ 3 | 2 5 _ |
-------------------------
| 7 8 _ | _ _ 5 | _ 9 _ |
| _ _ _ | _ 4 8 | 1 _ _ |
| _ _ 9 | 7 _ _ | 3 _ 2 |
-------------------------
| _ 3 5 | _ 1 9 | _ _ 7 |
| 4 7 _ | 2 _ _ | _ 1 _ |
| _ 9 2 | 4 _ _ | 8 _ 3 |
-------------------------

['\r', '-------------------------\r', '| 8 _ _ | _ 9 _ | 7 _ _ |\r', '| 3 5 ? | 1 _ _ | _ 4 6 |\r', '| _ _ 4 | 6 _ 3 | 2 5 _ |\r', '-------------------------\r', '| 7 8 _ | _ _ 5 | _ 9 _ |\r', '| _ _ _ | _ 4 8 | 1 _ _ |\r', '| _ _ 9 | 7 _ _ | 3 _ 2 |\r', '-------------------------\r', '| _ 3 5 | _ 1 9 | _ _ 7 |\r', '| 4 7 _ | 2 _ _ | _ 1 _ |\r', '| _ 9 2 | 4 _ _ | 8 _ 3 |\r', '-------------------------\r', '']
([['8', '2', '6', '5', '9', '4', '7', '3', '1'], ['3', '5', '7', '1', '8', '2', '9', '4', '6'], ['9', '1', '4', '6', '7', '3', '2', '5', '8'], ['7', '8', '1', '3', '2', '5', '6', '9', '4'], ['2', '6', '3', '9', '4', '8', '1', '7', '5'], ['5', '4', '9', '7', '6', '1', '3', '8', '2'], ['6', '3', '5', '8', '1', '9', '4', '2', '7'], ['4', '7', '8', '2', '3', '6', '5', '1', '9'], ['1', '9', '2', '4', '5', '7', '8', '6', '3']], '7', '12')
Sending ==> 7
YAY
['YAY']

-------------------------
| _ _ 2 | 7 9 _ | _ 3 4 |
| _ 3 _ | _ _ 4 | _ 8 5 |
| 6 _ _ | 3 _ 8 | 1 _ _ |
-------------------------
| _ _ _ | 1 2 5 | _ _ 6 |
| _ 2 _ | _ _ _ | 9 _ 7 |
| 4 _ _ | 8 _ _ | _ 5 ? |
-------------------------
| 3 7 _ | _ _ _ | _ _ _ |
| _ 8 5 | 9 _ 6 | 4 _ 2 |
| _ _ 4 | 5 _ 7 | _ 9 8 |
-------------------------

['\r', '-------------------------\r', '| _ _ 2 | 7 9 _ | _ 3 4 |\r', '| _ 3 _ | _ _ 4 | _ 8 5 |\r', '| 6 _ _ | 3 _ 8 | 1 _ _ |\r', '-------------------------\r', '| _ _ _ | 1 2 5 | _ _ 6 |\r', '| _ 2 _ | _ _ _ | 9 _ 7 |\r', '| 4 _ _ | 8 _ _ | _ 5 ? |\r', '-------------------------\r', '| 3 7 _ | _ _ _ | _ _ _ |\r', '| _ 8 5 | 9 _ 6 | 4 _ 2 |\r', '| _ _ 4 | 5 _ 7 | _ 9 8 |\r', '-------------------------\r', '']
([['8', '5', '2', '7', '9', '1', '6', '3', '4'], ['9', '3', '1', '2', '6', '4', '7', '8', '5'], ['6', '4', '7', '3', '5', '8', '1', '2', '9'], ['7', '9', '3', '1', '2', '5', '8', '4', '6'], ['5', '2', '8', '6', '4', '3', '9', '1', '7'], ['4', '1', '6', '8', '7', '9', '2', '5', '3'], ['3', '7', '9', '4', '8', '2', '5', '6', '1'], ['1', '8', '5', '9', '3', '6', '4', '7', '2'], ['2', '6', '4', '5', '1', '7', '3', '9', '8']], '3', '58')
Sending ==> 3
YAY
['YAY']

-------------------------
| _ 8 _ | 1 2 _ | _ _ _ |
| 5 _ _ | _ _ _ | 6 _ _ |
| _ 3 9 | _ _ _ | 7 8 _ |
-------------------------
| _ 4 _ | 5 _ _ | _ 9 2 |
| 6 1 _ | _ 8 _ | _ _ _ |
| _ 9 5 | 2 7 _ | 1 3 _ |
-------------------------
| 1 _ _ | 7 _ 9 | 5 _ _ |
| _ 6 _ | _ _ 5 | 2 _ ? |
| 7 _ 3 | 6 1 _ | _ 4 8 |
-------------------------

['\r', '-------------------------\r', '| _ 8 _ | 1 2 _ | _ _ _ |\r', '| 5 _ _ | _ _ _ | 6 _ _ |\r', '| _ 3 9 | _ _ _ | 7 8 _ |\r', '-------------------------\r', '| _ 4 _ | 5 _ _ | _ 9 2 |\r', '| 6 1 _ | _ 8 _ | _ _ _ |\r', '| _ 9 5 | 2 7 _ | 1 3 _ |\r', '-------------------------\r', '| 1 _ _ | 7 _ 9 | 5 _ _ |\r', '| _ 6 _ | _ _ 5 | 2 _ ? |\r', '| 7 _ 3 | 6 1 _ | _ 4 8 |\r', '-------------------------\r', '']
([['4', '8', '6', '1', '2', '7', '3', '5', '9'], ['5', '7', '1', '3', '9', '8', '6', '2', '4'], ['2', '3', '9', '4', '5', '6', '7', '8', '1'], ['3', '4', '7', '5', '6', '1', '8', '9', '2'], ['6', '1', '2', '9', '8', '3', '4', '7', '5'], ['8', '9', '5', '2', '7', '4', '1', '3', '6'], ['1', '2', '8', '7', '4', '9', '5', '6', '3'], ['9', '6', '4', '8', '3', '5', '2', '1', '7'], ['7', '5', '3', '6', '1', '2', '9', '4', '8']], '7', '78')
Sending ==> 7
You failed!
['You failed!']
```

* I discussed about this with the organizers and found that sometimes there could be 2 solutions to a sudoku puzzle and the server algo was expecting only one particular answer. ....:-(

* They rectified this in the morning and the same code worked! :-)

```
([['6', '2', '7', '4', '1', '9', '5', '8', '3'], ['8', '1', '4', '3', '6', '5', '2', '7', '9'], ['5', '9', '3', '2', '7', '8', '1', '4', '6'], ['3', '6', '8', '9', '4', '1', '7', '5', '2'], ['2', '5', '1', '8', '3', '7', '6', '9', '4'], ['7', '4', '9', '6', '5', '2', '3', '1', '8'], ['1', '8', '6', '5', '9', '3', '4', '2', '7'], ['9', '3', '5', '7', '2', '4', '8', '6', '1'], ['4', '7', '2', '1', '8', '6', '9', '3', '5']], '4', '48')
Sending==> 4
['YAY']

Congrats! Flag is flag{SudokuMoreLikeSuDONEku}

['\r', 'Congrats! Flag is flag{SudokuMoreLikeSuDONEku}\r', '']
[*] Switching to interactive mode
[*] Got EOF while reading in interactive
```

* Vegan Burger - Crypto/Stegano

 - Given series of `AB` characters as a cipher --> Identified it as `Baconian cipher`

 - Next was a caesar shift (ROT13) solve to get the flag

* Horror Code - Crypto
 
  - 

* Email Steganography



* Network Steganography

* Subdomain Reconnaissance 

* Network Reconnaissance