## Why this repo:

If you install dstat using <code>apt install dstat</code> in Ubuntu 22.04LTE there are many bugs that may occur while using it in CLI. In order to alleviate some of the common bugs in CLI, this repo is created. This repo also addresses the bug of creating an output csv file of certain performance metric while running  it in a detached GNU screen. 

This repo is tested on ubuntu 22.04LTS. Build on top of debian version of [dstat](https://salsa.debian.org/debian/dstat). Which is a derivative of the original or real [dstat](http://github.com/dagwieers/dstat)

This version is tested on Python 3.7.13. Assumption: Newer versions of Python may also support (but not tested)

Unlike the previous versions of dstat on ubuntu 22.04LTS, This version supports GNU screen to log the activity of a machine into an output file as stated earlier. 

<b>How to use this repo-</b>

At first clone the repo:

```
git clone https://github.com/0rky/dstat

```
If you want to do capture some performance metrics an example will be:  
```
/path_to_repo/dstat -t -l -d --noupdate --output /path_to_output_file/output.csv 15

```
Please consult the dstat [manual](https://linux.die.net/man/1/dstat) for more details.

If you want to use GNU screen to observe some performance metrices, an example will be:

```
screen -dmS screen_name /path_to_repo/dstat -t -l -d --noupdate /path_to_output_file/output.csv 15

```

