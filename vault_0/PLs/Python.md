#prog-lang 
## Packaging

[Packaging Python Projects - Python Packaging User Guide](https://packaging.python.org/en/latest/tutorials/packaging-projects/)
## Concurrency

[Concurrency Concepts in Python - YouTube](https://www.youtube.com/watch?v=S05-MZAJqNM&list=PL9_iFHfnv8hBzIvrgk5qsE4VD7oUiAQ4E&index=8)

In single Python process, threads can run only in a time-sliced manner, because of GIL (CPython implementation).
### Multiprocessing

```python
from multiprocessing import Pool

def long_running_func(...):
	...

with Pool(processes=4) as pool:
	result = pool.starmap(long_running_func, array_of_args_for_each_instance)

# or (if we want to pass named arguments)

pool = Pool(processes=4)
async_results = [
	pool.apply_async(long_running_func, args=args, kwds=kwargs)
	for args, kwargs in ...
]
pool.close()  # no more funcs to pool
pool.join()
results = [result.get() for result in async_results]
```


In Python, ... is good for I/O bound operations, but will likely fail for CPU bound operations (because of GIL)
## Asynchrony

[Полное руководство по модулю asyncio в Python. Часть 1 / Хабр (habr.com)](https://habr.com/ru/companies/wunderfund/articles/700474/)
[Python Asyncio: The Complete Guide - Super Fast Python](https://superfastpython.com/python-asyncio/)

```python
asyncio
.run(coro)
.create_task(coro)

.gather(*[coro1, ...])

# or

async with asyncio.TaskGroup() as group:
	task = group.create_task(coro)

.wait([task1, ...], return_when=asyncio.ALL_COMPLETED, timeout=10)

try:
	await asyncio.wait_for(coro, timeout=10)
except asyncio.TimeoutError:
	...

asyncio.shield(task)

asyncio.to_thread()
```
## GC

[Всё, что нужно знать о сборщике мусора в Python / Хабр (habr.com)](https://habr.com/ru/articles/417215/)

`sys.getrefcount(object)` - количество ссылок на объект

```python
import gc

gc.get_threshold()
gc.set_threshold()

gc.disable()  # disable auto gc

gc.collect()  # garbage collect cyclic links
```

## Datamodel

https://docs.python.org/3/reference/datamodel.html
## Super()

Method resolution order:

```python
__mro__
```
## Metaclass

[oop - What are metaclasses in Python? - Stack Overflow](https://stackoverflow.com/questions/100003/what-are-metaclasses-in-python)
## Descriptors

Descriptor - object defining any of `__get__`, `__set__`, `__delete__`

## CPython

[python/cpython: The Python programming language (github.com)](https://github.com/python/cpython)
## PyPy
