# TAIL

tail - output the last part of files


## Synopsis

tail [OPTION]... [FILE]...


## Options

```
-c, --bytes=[+]NUM
```

output the last NUM bytes; or use -c +NUM to output starting
with byte NUM of each file
              
```
-f, --follow[={name|descriptor}]
```

output appended data as the file grows;

an absent option argument means 'descriptor'
-F     same as --follow=name --retry


```
-n, --lines=[+]NUM
```
output the last NUM lines, instead of the last 10; or use -n
+NUM to output starting with line NUM

```
--max-unchanged-stats=N
```
with --follow=name, reopen a FILE which has not
changed size after N (default 5) iterations to see if it has
been unlinked or renamed (this is the usual case of rotated
log files); with inotify, this option is rarely useful

```
--pid=PID
```
with -f, terminate after process ID, PID dies

```
-q, --quiet, --silent
```
never output headers giving file names

```
--retry
```
keep trying to open a file if it is inaccessible

```
-s, --sleep-interval=N
```
with -f, sleep for approximately N seconds (default 1.0)
between iterations; with inotify and --pid=P, check process P
at least once every N seconds


