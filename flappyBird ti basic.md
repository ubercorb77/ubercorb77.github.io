This was my first calculator game that used collisions. 68 lines

```
ClrHome
ClrDraw
FnOff
AxesOff
¯16→Xmin
16→Xmax
¯8→Ymin
8→Ymax
0→S
16→E
15→R
Pxl-Change(15,21)
0→D
Repeat D=1
Repeat getkey
For(J,1,2)
Pxl-Change(R,21)
R+1→R
If pxl-Test(R,21)
Then
1→D
Else
Pxl-Change(R,21)
End
End
If E=¯10
Then
If D=0
Then S+1→S
End
End
If E<¯14
Then
16→E
randInt(¯6,8)→Q
End
If E>¯16
Then
Line(E,16,E,¯16,0)
If E=¯9
Pxl-On(R,21)
E-1→E
Line(E,8,E,Q)
Line(E,Q-2,E,¯8)
End
End
Pxl-Change(R,21)
R-4→R
If pxl-Test(R,21)
Then
1→D
Else
Pxl-Change(R,21)
End
End
Disp "SCORE:"
Disp S
0→S
FnOn
AxesOn
¯10→Xmin
10→Xmax
¯10→Ymin
10→Ymax
Disp "ENTER 123 TO"
Disp "PLAY AGAIN: ",A
If A=123
prgmFLPYBIRD
```
