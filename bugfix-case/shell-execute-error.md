---
description: >-
  The shell write on Macbook, when open on windows and copy to linux can't run
  normally.
coverY: 0
---

# Shell Execute Error

I wrote a shell script on my macbook like below

```shell
#!/bin/sh
SERVERS=123,456

IFS=','
for SERVER in $SERVERS; do
  echo "A""$SERVER""A"
done
```

