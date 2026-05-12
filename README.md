# Understanding Pointers and Functions in C++

This lesson introduces some important beginner concepts in C++:

- Variables
- Functions
- References
- Pointers
- Memory addresses
- Console output

---

# Full Program

```cpp
#include <iostream>

using namespace std;

int multiplyby3(int &x)
{
    return x * 3;
}

int main()
{
    cout << "Hello World";

    int y = 14;
    int *p = &y;

    cout << "\n value of y = " << y;
    cout << "\n address of y = " << &y;
    cout << "\n pointer to y = " << p;
    cout << "\n multiplyby 3 = " << multiplyby3(y);

    return 0;
}
```

---

# 1. Including the iostream Library

```cpp
#include <iostream>
```

The `iostream` library allows us to use:

- `cout` → print output
- `cin` → receive input

---

# 2. Using the Standard Namespace

```cpp
using namespace std;
```

Instead of writing:

```cpp
std::cout
```

we can simply write:

```cpp
cout
```

---

# 3. Creating a Function

```cpp
int multiplyby3(int &x)
{
    return x * 3;
}
```

This function:

- receives a number
- multiplies it by 3
- returns the result

---

# 4. Understanding References

```cpp
int &x
```

The `&` symbol here means **reference**.

A reference acts like another name for the original variable.

Example:

```cpp
multiplyby3(y);
```

Here, `x` becomes another name for `y`.

---

# 5. Creating a Variable

```cpp
int y = 14;
```

This creates an integer variable named `y`.

---

# 6. Understanding Pointers

```cpp
int *p = &y;
```

## Breakdown

### `int *p`

Creates a pointer variable.

### `&y`

Gets the memory address of `y`.

So this line means:

> Store the address of `y` inside pointer `p`

---

# 7. Printing the Value

```cpp
cout << "\n value of y = " << y;
```

Output:

```text
value of y = 14
```

---

# 8. Printing the Address

```cpp
cout << "\n address of y = " << &y;
```

Example output:

```text
address of y = 0x61ff08
```

---

# 9. Printing the Pointer

```cpp
cout << "\n pointer to y = " << p;
```

The pointer stores the address of `y`.

---

# 10. Calling the Function

```cpp
cout << "\n multiplyby 3 = " << multiplyby3(y);
```

Since `y = 14`:

```text
14 × 3 = 42
```

---

# Expected Output

```text
Hello World
value of y = 14
address of y = 0x61ff08
pointer to y = 0x61ff08
multiplyby 3 = 42
```

---

# Important Concepts Learned

| Concept | Example |
|---|---|
| Variable | `int y = 14;` |
| Function | `multiplyby3()` |
| Reference | `int &x` |
| Pointer | `int *p` |
| Address Operator | `&y` |
| Output | `cout` |

---

# Common Beginner Confusion

The `&` symbol has two meanings in C++.

## Reference

```cpp
int &x
```

Means:

> x is a reference

## Address Operator

```cpp
&y
```

Means:

> get memory address of y

---

# Final Thoughts

This small program teaches several powerful C++ concepts:

- variables
- pointers
- references
- memory addresses
- functions
- console output

These concepts are the foundation of advanced C++ programming.
