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

`logfile` - Specify an absolute path to which exercise logs may optionally be written, or boolean `false` to disable logging. If a file path ending with the `.csv` file extension is specified, the application will output CSV data. Otherwise, plain-text will be logged. Make note not to use double-quotes within your exercise names (within the `.git-ripped.json` file), because I am not CSV-escaping these values before writing them to disk.

`max_rest_time` - Specify the time duration (in minutes) wherein the application should consider you to be 100% rested. This value is used for a modifier calculation when the `adaptive` value is set to `true`.

`random` - If set to boolean `true`, random repetition values will be prescribed for each exercise. This may be used in conjunction with `adaptive`. Specifiy boolean `true` to enable randomization or `false` to disable.

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
