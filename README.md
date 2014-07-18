agl
===

Helper script for the_silver_surfer. Uses 'ag' to search given files, opens matches with less


From the help:

```
% agl -h

Uses 'ag' to search given files, opens matches with less

Usage: /home/kmacleod/bin/agl [-h] <'ag' arguments>

Examples:
agl --java SomeClass
agl --xml '<artifact'
agl --java -i someclass
        Note: arguments are not passed into less, so in this case
        you would need to immediately use '-i' command in less.
```
