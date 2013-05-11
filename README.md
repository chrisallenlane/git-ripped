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
Installation is simple.

1. Download `git-ripped` and `.git-ripped.json`
2. Optionally place `git-ripped` somewhere on your system `$PATH`
3. Optionally place `.git-ripped.json` in your `$HOME` directory
4. Modify `.git-ripped.json` per your preferences
5. Specify `git-ripped` to run as a `git` post-commit hook

Configuration
-------------
The configuration file contains several switches which can be used to alter
`git-ripped`'s behavior:

`adaptive` - If boolean `true`, the application will adjust its prescribed exercises
based on how much time has passed between commits. Set to boolean `true` or `false`.

`color` - Output to the terminal in the specified color. Requires `termcolor` to be installed on your system. (`sudo pip install termcolor`, etc.) Set to a valid terminal color or the string `"default"`.

logfile
max_rest_time
random

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
