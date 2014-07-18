agl / agv
=========

Helper script for the_silver_surfer (https://github.com/ggreer/the_silver_searcher).

Uses 'ag' to search given files, then opens matches with either 'less' or 'vim'.

This script uses 'ag' to 

1. Find a list of files matching the given pattern, and then 
2. Passes that list into 'less' with the search pattern applied. You can then navigate the results using less (e.g. n,N,:n,:p commands).

At it's simplest you can just use it with a search string. agl will open all the matching files in less:

```
agl somestring
```
or 
```
agl "some longer string"
```

Using vim instead of less
-----------------------------

If the script is named 'agv' it will use vim instead of less to open the file results.

The intended way to use this feature is to create a symlink from agl to agv:
```
% ln -s agl agv
```

Now use 'agv' to search and edit the results in vim.


Detailed help
--------------


From the help:

```
% agl -h

Uses 'ag' to search given files, opens matches with less

Usage: agl [-h] ['ag' arguments]

['ag' arguments] :
                A set of arguments to ag, including the search expression
                e.g. [FILE-TYPE] [OPTIONS] PATTERN [PATH]
                Note: any multi-field [OPTIONS] need to be quoted (eg "--ignore PATTERN" or "-G PATTERN")

Examples:
agl --java SomeClass
agl --xml '<artifact'
agl --java -i someclass
        Note: arguments are not passed into less, so in this case
        you would need to immediately use '-i' command in less.
agl "-G '.log'" "some string"
        Note: the -G option needs to be quoted so as to be treated as a single ag option.
agl "--ignore '*.log'" "some string"
        Note: the --ignore option needs to be quoted so as to be treated as a single ag option.
```
