git-ripped
==========

`git-ripped` is a `git` [post-commit] script that encourages you to take an
exercise break after every commit. Think of it as a Python compatibility layer
between your unused exercise equipment and your soft, shitty programmer body.

```
      XXXX                                                           XXXX     
      XXXX                                                           XXXX     
    XXXXXX                                                           XXXXXX   
 [||XXXXXX||==========xxxxx========================xxxxx===========||XXXXXX||]
 /\ XXXXXX                                                           XXXXXX /\
      XXXX                                                           XXXX     
      XXXX                                                           XXXX     
```

`git-ripped` can be configured to choose exercises from a list of your specification, and can
operate in one of three ways. It can be made to:

1. Prescribe a fixed number of repititions at each break
2. Randomly choose between a specified minimum and maximum number of 
   repititions for each exercise
3. Intelligently prescribe a suggested exercise and effort based on how long it
   has been since your last commit (and thereby, how rested you are in turn)

                                                                              

Advantages
----------
- Exercise occurs after commits, which is a natural best point
- Encourages you to step away from your computer periodically

Installing
----------
- Just copy the two files

Configuration
-------------
- Config file
- params:

`adaptive`
`color`
`logfile`
`max_rest_time`
`random`
`exercises`

Usage
-----
- Configure as git post-commit hook
- CSV output

_Successful_ Usage
------------------
Make sure to tune it properly that you don't just start ignoring it. If you're
too ambitious in the configs, you'll just ignore the robot, rendering it
pointless.

License
-------
`git-ripped` is released under the [GPL3 license][]. It comes with no warranty,
expressed or implied.


[post-commit]: http://git-scm.com/book/ch7-3.html
[GPL3 license]: http://www.gnu.org/licenses/gpl-3.0.txt
