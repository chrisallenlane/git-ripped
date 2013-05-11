git-ripped
==========

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
`git-ripped` is a `git` post-commit hook that encourages you to take an
exercise break after every commit. Think of it as a Python compatibility layer
between your soft, shitty programmer body and your unused exercise equipment.

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


[GPL3 license]: http://www.gnu.org/licenses/gpl-3.0.txt
