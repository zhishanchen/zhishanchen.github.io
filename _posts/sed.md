---
title: 'sed'
date: 2020-06-19
permalink: /posts/2020/06/blog-post-4/
tags:
  - sed
---

sed commands that frequently be used


Return only the portion of a line after a matching pattern
======
```
sed -n -e 's/^.*stalled: //p'

sed -n -e 's/^.*\(stalled: \)/\1/p'

sed -n -e 's/^\(.*\)\(stalled: \)\(.*\)$/\3\2\1/p'

```
-n means not to print anything by default  
-e is followed by a sed command    
s is the pattern replacement command 