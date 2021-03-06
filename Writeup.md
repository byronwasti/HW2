Decoder:

```
En A0 A1| O0 O1 O2 O3 | Expected Output
0  0  0 |  0  0  0  0 | All false
0  1  0 |  0  0  0  0 | All false
0  0  1 |  0  0  0  0 | All false
0  1  1 |  0  0  0  0 | All false
1  0  0 |  1  0  0  0 | O0 Only
1  1  0 |  0  1  0  0 | O1 Only
1  0  1 |  0  0  1  0 | O2 Only
1  1  1 |  0  0  0  1 | O3 Only
```

![Decoder](decoder.png)

Multiplexer:

```
A0 A1 | in0 in1 in2 in3 | out | Expected
0  0  | 1   x   x   x   | 1   | 1
0  0  | 0   x   x   x   | 0   | 0
1  0  | x   1   x   x   | 1   | 1
1  0  | x   0   x   x   | 0   | 0
0  1  | x   x   1   x   | 1   | 1
0  1  | x   x   0   x   | 0   | 0
1  1  | x   x   x   1   | 1   | 1
1  1  | x   x   x   0   | 0   | 0
```

![Multiplexer](multiplexer.png)

Adder:

```
a b cin | sum cout | Expected 
0 0 0   | 0   0    | 0  0
1 0 0   | 1   0    | 1  0
0 1 0   | 1   0    | 1  0
1 1 0   | 0   1    | 0  1
0 0 1   | 1   0    | 1  0
1 0 1   | 0   1    | 0  1
0 1 1   | 0   1    | 0  1
1 1 1   | 1   1    | 1  1
```
![Adder](adder.png)
