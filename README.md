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

About
-----
`git-ripped` is intended to be configured with exercises of your choosing, and
can operate in one of three modes. It can:

1. prescribe a fixed number of repetitions with each commit
2. prescribe a random number of reptitions with each commit (within a specified
   min/max)
3. intelligently prescribe a number of repititions with each commit, based on
   how much time has passed between commits


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
