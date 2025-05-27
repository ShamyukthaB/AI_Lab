# Ex.No: 6   Logic Programming – Towers of Hanoi Problem   
### DATE:25-03-2025                                                                            
### REGISTER NUMBER:212222040027 
### AIM: 
To  write  a logic program  to solve Towers of Hanoi problem  using SWI-PROLOG. 
### Algorithm:
1. Start the program
2.  Write a rules for finding solution of Towers of Hanoi in SWI-PROLOG.
    a )	If only one disk  => Move disk from X to Y.
    
     b)	If Number of disk greater than 0 then
    
           i)	Move  N-1 disks from X to Z.
    
          ii)	Move  Nth disk from X to Y
    
         iii)	Move  N-1 disks from Y to X.
    
4. Run the program  to find answer of  query.

### Program:
```
% Base Case
move(1, X, Y, _) :-
    write('Move disk from '), write(X), write(' to '), write(Y), nl.

% Recursive Case
move(N, X, Y, Z) :-
    N > 1,
    N1 is N - 1,
    move(N1, X, Z, Y),
    move(1, X, Y, _),
    move(N1, Z, Y, X).
```

### Output:
![image](https://github.com/user-attachments/assets/c1303659-1363-4bfa-8c03-b9d69e907559)

### Result:
Thus the solution of Towers of Hanoi problem was found by logic programming.
