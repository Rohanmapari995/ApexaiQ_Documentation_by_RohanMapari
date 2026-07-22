# Python Memory Management

## Overview
Python automatically manages memory, allowing developers to focus on writing code instead of manually allocating and freeing memory. CPython uses **Reference Counting**, **Garbage Collection**, and **PyMalloc** for efficient memory management.

---

## 1. Reference Counting
- Every Python object has a reference count.
- When the count reaches **0**, the object is immediately deleted.

```python
a = [1, 2, 3]
b = a

del a
del b
```

**Pros**
- Fast and efficient.
- Immediate memory cleanup.

**Cons**
- Cannot handle circular references.

---

## 2. Garbage Collection (GC)
- Handles objects involved in **reference cycles**.
- Uses the `gc` module.

```python
import gc
gc.collect()
```

### Generations
- **Gen 0:** New objects
- **Gen 1:** Objects surviving Gen 0
- **Gen 2:** Long-lived objects

---

## 3. PyMalloc
CPython uses **PyMalloc** to efficiently allocate memory for small objects.

Memory Structure:

```text
Arena (256 KB)
 ├── Pool (4 KB)
 │    └── Blocks
```

**Benefits**
- Faster allocation
- Reduced fragmentation
- Better performance

---

## 4. Object Interning
Python reuses certain immutable objects to save memory.

```python
a = 100
b = 100
print(a is b)   # True
```

Commonly interned:
- Small integers (`-5` to `256`)
- Some string literals

---

## 5. Stack vs Heap

| Stack | Heap |
|--------|------|
| Function calls | Python objects |
| Local references | Lists, Dictionaries, Objects |

Example:

```python
def func():
    x = [1, 2, 3]
```

- `x` → Stack (reference)
- List → Heap (object)

---

## 6. Memory Monitoring

```python
import sys
sys.getsizeof([1,2,3])
```

```python
import tracemalloc

tracemalloc.start()
current, peak = tracemalloc.get_traced_memory()
```

Useful tools:
- `tracemalloc`
- `memory_profiler`
- `psutil`

---

## 7. Best Practices
- Avoid unnecessary global variables.
- Use generators for large datasets.
- Close files using `with`.
- Remove unused references.
- Profile memory before optimizing.

---

## Summary

| Component | Purpose |
|-----------|---------|
| Reference Counting | Deletes objects when reference count becomes zero |
| Garbage Collector | Removes circular references |
| PyMalloc | Fast memory allocation for small objects |
| Stack | Stores function frames and references |
| Heap | Stores Python objects |
| Object Interning | Reuses immutable objects to save memory |

---

## Key Takeaways
- Python manages memory automatically.
- **Reference Counting** provides immediate cleanup.
- **Garbage Collection** handles cyclic references.
- **PyMalloc** improves allocation performance.
- Memory profiling tools help identify leaks and optimize applications.