# python header format
This is meant to show you the best header format you should use to make your code easier to use for others. If the project is private and only for you, it's still good practice to maintain proper formatting.
<sub><sub>Extra information/examples below</sub></sub>
#####
 1. **`#!/usr/bin/env python`**
-This allows for the script to be implicitly executed by the interpreter.
 2. **`docstring description`**
 -The description for the script, if long include a brief but complete line to be first. The next line(s) can be the full longer description.
 3. **`import statements`**
 -Should go in the order of built in modules first, followed by third party modules such as pandas or requests. Finally you should put your own modules.
 4. **`authorship info`**
 -Not needed, but recommended.
&nbsp;
 # Extra info
  - docstring\
&ensp;The docstring is a multi line string without variable assignment, essentially a multiline comment.
  - authorship\
&ensp;`__author__` or `__authors__`is a must have, as is `__version__`.
&ensp;Others may include `__contact__`, `__copyright__`, `  
__license__` or`__date__`
&nbsp;
# Example
```python
#!/usr/bin/env python

"""A simple typewriter function
This script utilizes the sleep function from the time module,
as well as the flush function from the sys module.
"""

import sys
from time import sleep
import requests #This and the following import is only here to provide an example of import order.
from example import add

__author__ = "H3lix fire"
__version__ = 1.0
__date__ = "9/28/2022"

def typewrite(text:str="No text specified", time:float=0.065):
  for char in text:
    sleep(time)
    sys.stdout.write(char)
    sys.stdout.flush()

typewrite("This is an example\n", 0.12)
```
