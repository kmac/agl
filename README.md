agl
===

Helper script for the_silver_surfer (https://github.com/ggreer/the_silver_searcher).

Uses 'ag' to search given files, opens matches with 'less'

This script uses ag to 1) find a list of files matching the given pattern, and then 2) passes that list into 'less' with the search pattern applied. You can then navigate the results using less (e.g. n,N,:n,:p commands).

From the help:

```
% agl -h

Uses 'ag' to search given files, opens matches with less

Usage: agl [-h] <'ag' arguments>

Examples:
agl --java SomeClass
agl --xml '<artifact'
agl --java -i someclass
        Note: arguments are not passed into less, so in this case
        you would need to immediately use '-i' command in less.
```
