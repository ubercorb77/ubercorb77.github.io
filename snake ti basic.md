This is quite laggy on a TI-83. I recommend using a faster calculator. Maybe it's because my program, with 77 lines, is quite inefficient (but it's not as inefficient as some specific individuals' code). Or maybe it's also because I use too many parentheses. Anyway, here's some shorter code (not mine).

```
ClrHome
Output(4,1,"MADE BY UBERCORB")
For(I,1,300)
End
ClrHome
randInt(1,8)→Y
randInt(1,16)→X
Output(Y,X,"o")
0→D
26→A
0→S
{1,1}→L6
While not(D)
 getKey→B
 If B≠A and B≥24
  B→A
 For(I,dim(L6),3,¯1)
  L6(I-2)→L6(I)
 End
 If A=24
  L6(2)-1→L6(2)
 If A=25
  L6(1)-1→L6(1)
 If A=26
  L6(2)+1→L6(2)
 If A=34
  L6(1)+1→L6(1)
 ClrHome
 Output(Y,X,"o")
 For(I,1,dim(L6),2)
  Output(L6(I),L6(I+1),".")
 End
 For(I,3,dim(L6),2)
  If L6(1)=L6(I) and L6(2)=L6(I+1)
  1→D
 End
 If L6(1)=Y and L6(2)=X
 Then
  S+1→S
  If dim(L6)>3
  Then
   {L6(dim(L6)-1),L6(dim(L6))}-{L6(dim(L6)-3),L6(dim(L6-2))}→L5
   L6(dim(L6)-1)+L5(1)→L6(dim(L6)+1)
   L6(dim(L6)-1)+L5(2)→L6(dim(L6)+1)
  Else
   If A=24
   Then
    L6(1)→L6(dim(L6)+1)
    L6(2)+1→L6(dim(L6)+1)
   End
   If A=25
   Then
    L6(1)+1→L6(dim(L6)+1)
    L6(2)→L6(dim(L6)+1)
   End
   If A=26
   Then
    L6(1)→L6(dim(L6)+1)
    L6(2)-1→L6(dim(L6)+1)
   End
   If A=34
   Then
    L6(1)-1→L6(dim(L6)+1)
    L6(2)→L6(dim(L6)+1)
   End
  End
  randInt(1,8)→Y
  randInt(1,16)→X
  Output(Y,X,"o")
 End
End
ClrHome
Disp "SCORE: ", S
Disp "123 TO PLAY:"
Input "",B
If B=123
 prgmSNAKE
```
