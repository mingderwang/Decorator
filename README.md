# Python Design Pattern - Decorator
[credit](https://sourcemaking.com/design_patterns/decorator)

# UML Class Diagram
![](https://sourcemaking.com/files/v2/content/patterns/Decorator__1.png)

# decorator macro in Python
```
from functools import wraps

def debug(func):
    @wraps(func)
    def out(*args, **kwargs):
        print(func.__name__)
        return func(*args, **kwargs)
    return out

@debug
def add(x, y):
    return x + y

```