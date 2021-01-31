
_按需查询Python文档并实践_

---

<font size = 5px>**Contents**</font>
- [Built-in Functions](https://docs.python.org/3/library/functions.html)
- [string](https://docs.python.org/3/library/string.html)
- [os](https://docs.python.org/3/library/os.html)
- [datetime](https://docs.python.org/3/library/datetime.html)

### string

[Examples](https://docs.python.org/3/library/string.html#format-examples)
```python
'rounded to 2 decimal places: {:.2f}'.format(0.555)
```

### os

[Documentation](https://docs.python.org/3/library/os.html)

```python
import os
from os.path import join, getsize

for folder in os.listdir('.'):
    n=0
    sizesum=0
    for (root, dirnames, filenames) in os.walk(folder,topdown=False):
        sizesum += sum(getsize(join(root,name)) for name in filenames)
        n += len(filenames)
    if sizesum>1e4:
        print('{!r:15}: {:6,} files, {:8,.1f} M.'.format(root,n,sizesum/1e6))
```

### datetime
___


___


___

___


___


___


___

___

___

___


###### References:

<div id="refer-1"></div>

[1] [Python documentation](https://docs.python.org/3/)
