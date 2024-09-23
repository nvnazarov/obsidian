4GL

- Comments, docstrings

```python
# comment

def fun():
	"""..."""
	pass
```

- Constants

```go
package math

const Pi = 3.14

const (
	A = 1,
	B = 2,
)
```

- Control Flow

```python
if cond:
	...
elif cond:
	...
else:
	...

for i in iterable:
	... # break, continue, pass
else:
	...

while cond:
	...
else:
	...

match expr:
	case val:
		...
	case _:
		...
```

- OOP

Classes:

```python
class A:
	...
```

Encapsulation:

```c++
class A {
private:
public:
protected:
}
```

Inheritance (Single, Multiple):

...

Abstraction:

...

- String interpolation

```python
s = f"{a}bo{b}a"
```

- Try-Catch/Except-Finally

```python
try:
	...
except Exception as e:
	...
finally:
	...
```

- Coroutines

```python
def fun():
	for i in range(10):
		yield i
```

- Cooperative concurrency (async / await)

```python
import asyncio

async def coro():
	await asyncio.sleep(10)
	print("done")

asyncio.run(coro)
```

- native

```java
public class NativeLib {
	static {
    	System.loadLibrary("piValueLib");
	}

	public native String getPiValue(); // native method
}
```

- Threads (Shared memory concurrency)

```python
import threading
```

- Processes

```python
import multiprocessing
```

- Pointers & references

```c++
int* a = malloc(sizeof(int));
int& b = *a;

delete a;
```

- Macros

- Anonymous / lambda functions

- Functions as first class objects

- Everything is an object

- Typedef

-  Generators

### Built-in Data Types

```python
a = dict() # dict
b = {1, 2} # set
```

```go
var a map[int]string
```

Routines that act like iterators. Instead of returning an array of values, returns values one by one.
### Modules system

Include hubs.

Built-in modules:
- math
- os
- io
- net
- time
- path
- crypto
- db/sql
- encoding, csv
- json
- fmt
- random

### Reflection

# Tools
## Package manager
## Virtual environments
## Debugger
## Sanitizer
## Formatter
## Language server
