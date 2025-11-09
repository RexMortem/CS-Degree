
In the code:
```c
num = 3 + 3;
```

Lexing will read this as a character stream, strip whitespace, and organise the characters into **lexemes**:
```
num
=
3
+
3
;
```
Then these lexemes will be packaged as **tokens**, with a **symbol table**:
```
<identifier, 1>
<equality>
<intLiteral, 2>
<plus>
<intLiteral, 3>
<semicolon>
```

With the symbol table:

| Symbol ID | Value |
| --------- | ----- |
| 1         | num   |
| 2         | 3     |
| 3         | 3     |
