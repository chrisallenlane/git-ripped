git-ripped
==========

`git-ripped` is a `git` [post-commit] script that encourages you to take an
exercise break after every commit. Think of it as a Python compatibility layer
between your enfeebled programmer body and your unused exercise equipment.

![Imgur](http://i.imgur.com/rPOUZOD.png)


About
-----
`git-ripped` is intended to be configured with exercises of your choosing, and
can operate in one of three modes. It can:

1. prescribe a fixed number of repetitions with each commit
2. prescribe a random number of repetitions with each commit (within a
   specified min/max)
3. intelligently prescribe a number of repetitions with each commit, based on
   how much time has passed between commits


Installing
----------
Installation is simple:

1. Download `git-ripped` and `.git-ripped.json`
2. Optionally place `git-ripped` somewhere on your system `$PATH`
3. Optionally place `.git-ripped.json` in your `$HOME` directory
4. Modify `.git-ripped.json` per your preferences
5. Specify `git-ripped` to run as a `git` post-commit hook


Configuration
-------------
```
      XXXX                                                           XXXX     
      XXXX                                                           XXXX     
    XXXXXX                                                           XXXXXX   
 [||XXXXXX||==========xxxxx========================xxxxx===========||XXXXXX||]
 /\ XXXXXX                                                           XXXXXX /\
      XXXX                                                           XXXX     
      XXXX                                                           XXXX     
```

The configuration file contains several switches which can be used to alter
`git-ripped`'s behavior:

- `adaptive`  
If boolean `true`, the application will adjust its prescribed exercises based
on how much time has passed between commits. Set to boolean `true` or `false`.
- `color`  
Output to the terminal in the specified color. Requires `termcolor`
to be installed on your system. (`sudo pip install termcolor`, etc.) Set to a
valid terminal color or the string `"default"`.
- `logfile`  
Specify an absolute path to which exercise logs may optionally be
written, or boolean `false` to disable logging. If a file path ending with the
`.csv` file extension is specified, the application will output CSV data.
Otherwise, plain-text will be logged. Make note not to use double-quotes within
your exercise names (within the `.git-ripped.json` file), because I am not
CSV-escaping these values before writing them to disk.
- `max_rest_time`  
Specify the time duration (in minutes) wherein the
application should consider you to be 100% rested. This value is used for a
modifier calculation when the `adaptive` value is set to `true`.
- `min_rest_time`  
Specify (in minutes) the minimum amount of time that should pass between
exercises. By setting this parameter, you can prevent `git-ripped` from 
prescribing exercises if you're making many rapid-fire commits in quick
succession.
- `random`  
If set to boolean `true`, random repetition values will be
prescribed for each exercise. This may be used in conjunction with `adaptive`.
Specify boolean `true` to enable randomization or `false` to disable.


Usage
-----
Regardless of whether you chose to install `git-ripped` to your system path,
you simply need to invoke it in a post-commit hook to run it. Note that the
script optionally accepts a single command-line parameter, which is the path to
the configuration file to use, as in:

```bash
git-ripped /path/to/my/git-ripped.json
```


_Successful_ Usage
------------------
It's important to specify sensible repetition maximums in your configuration
file so you don't acquire the habit of ignoring the script's suggestions. Start
very conservatively and work up from there, being extra mindful to _obey your
robot overlord_. Don't allow yourself to get into the habbit of ignoring the
script's instructions, or you will find it wholly ineffective.


License
-------
`git-ripped` is released under the [GPL3 license][]. It comes with no warranty,
expressed or implied.


[post-commit]: http://git-scm.com/book/ch7-3.html
[GPL3 license]: http://www.gnu.org/licenses/gpl-3.0.txt
