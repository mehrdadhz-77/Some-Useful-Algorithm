# Some-Useful-Algorithm
This repository will be contained the description and the steps of some algorithms in detail with examples and codes provided.

Author: Mehrdad Hassanzadeh<br/>
Student of the Master of Data Science at Sapienza University of Rome.<br/>
Institutional Email: hassanzadeh.1961575@studenti.uniroma1.it<br/>


Input: 
    N : an integer 
    List : array of characters of length N
    
function f1(sequence, end): 
    For i=0 To end:
        OUTPUT sequence[i]
    EndFor
    Output "\n"
    
function f2(sequence, start, end): 
    If start = end: 
        f1(sequence, end)
    Else
        For i=start To end: 
            temp <-- sequence[start]
            sequence[start] <-- sequence[end]
            sequence[end] <-- temp
            f2(sequence, start+1, end)
            temp <-- sequence[start]
            sequence[start] <-- sequence[end]
            sequence[end] <-- temp
f2(List, 0, N)            
