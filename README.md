# Linux SHELL: input-output-error
Linux STDIN STDOUT STDERR


```
 xxxxxxxxxxxxxxxxxx
 x    TERMINAL    x
 x                x
 x  xxxxxxxxxxxx  x    #0 STDIN
 x  x KEYBOARD x  x >--------------------->-
 x  xxxxxxxxxxxx  x                        |
 x                x                        |
 x                x                    xxxxxxxxxxxx
 x                x                    x PROCESS  x
 x                x                    xxxxxxxxxxxx
 x  xxxxxxxxxxx   x   #1 STDOUT            |
 x  x         x   x<-----------<-          |
 x  x         x   x             |          |
 x  x DISPLAY x   x             ----------<-
 x  x         x   x             |
 x  x         x   x<-----------<-
 x  xxxxxxxxxxx   x   #2 STDERR
 x                x
 x                x
 x                x
 x USER INTERFACE x       INTERPRETER       APPLICATION
 x xxxxxxxxxxxxxx x
 x x            x x     xxxxxxxxxxxxxxx    xxxxxxxxxxxxx
 x x $ COMMAND  x x --> x PARSE-INPUT x -> x EXECUTION x ->-
 x x            x x     xxxxxxxxxxxxxxx    xxxxxxxxxxxxx   |
 x x            x x                                        |
 x x  RESULT    x x <------------------------------------<--
 x x            x x
 x x $          x x
 x xxxxxxxxxxxxxx x
 xxxxxxxxxxxxxxxxxx

```

# Linux SHELL: how commands are being executed
As the shell input is being read, the command is devided into words and operators:
```
    xxxxxxxxxxxxxxxxxxxxxx     xxxxxxxxxxxxxxxxxx
    x                    x     x Ignore coments x
    x      TERMINAL      x     xxxxxxxxxxxxxxxxxx
    x                    x             |
    x                    x             v
    x   xxxxxxxxxxxxxx   x      xxxxxxxxxxxxxxxx          xxxxxxxxxxxxxxxxx
    x   x Read input x   x ---> x Divide input x -------> x Apply quoting x
    x   xxxxxxxxxxxxxx   x      xxxxxxxxxxxxxxxx          xxxxxxxxxxxxxxxxx
    x                    x                                        |
    x                    x                                        v
    x                    x                                xxxxxxxxxxxxxxxxxxxxxxx
    x                    x                                x Parse into commands x
    x                    x                                xxxxxxxxxxxxxxxxxxxxxxx
    x                    x                                        |
    x                    x                                        v
    x xxxxxxxxxxxxxxxxxx x      xxxxxxxxxxxxxxxxxxxxx     xxxxxxxxxxxxxxxxxxxxx
    x x Display output x x <--- x Wait exist status x <-- x Apply redirection x
    x xxxxxxxxxxxxxxxxxx x      xxxxxxxxxxxxxxxxxxxxx     xxxxxxxxxxxxxxxxxxxxx
    x                    x
    xxxxxxxxxxxxxxxxxxxxxx
```



