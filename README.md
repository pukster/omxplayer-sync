Goal
==============
Forked this off of TuringMachine's site. I was modifying his code when I realized that it had many bugs (not to blame him, I would never have been able to build this from the ground up). Rather than bullet riddling his repo with issues I decided to fork it and continue my work here. The ultimated goal is to port this over to C, and then from there build it into omxplayer. Unfortunately, this program has so many bugs that it makes more sense to fix those in Python first, then move over to C.

OMXPlayer-Sync
==============

OMXPlayer-Sync facilitates synchronization of multiple OMXPlayer 
instances over the network in a master/slave fashion.

https://vimeo.com/65737409

Usage
-----

```
$ ./omxplayer-sync -h
Usage: omxplayer-sync [options] filename

Options:
  -h, --help            show this help message and exit
  -m, --master          
  -l, --slave           
  -x DESTINATION, --destination=DESTINATION
  -u, --loop            
  -v, --verbose
```

**master**

```
omxplayer -v -m -x 255.255.255.255 movie.mp4
```

**slave**

```
omxplayer -v -l movie.mp4
```


Requirements
------------
A recent version of [pyexpect](http://www.noah.org/wiki/pexpect).

Currently my [fork](https://github.com/turingmachine/omxplayer/tree/fixes) of omxplayer is required.

A build of this fork can be found at [yokto.magdesign.ch](http://yokto.magdesign.ch).
 

Settings
--------

```
OMXPLAYER = 'omxplayer'
PORT = 1666
TOLERANCE = 0.2
ADJUST_OMXPLAYER = -0.1
ADJUST_MASTER = 0.0
ADJUST_SLAVE = 0.0
SEEK_SIZE = 5
```
