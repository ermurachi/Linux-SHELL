# Linux-input-output-error
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




