### copy assignment
### copy initialization
### direct initialization(by using parenthesis)
### brace initialization(uniform initialization)
### global namespace

### r-value reference
  
  An `lvalue` is an expression that identifies a non-temporary object.  
  An `rvalue` is an expression that identifies a temporary object or is a value (such as a literal constant) not associated with any object.
```c++
void foo(int && a)
{
    // some magical code
}

int main()
{
    int x;
    foo(x); // Error. An rValue reference cannot be pointed to a lValue.
    foo(5);
    foo( x + 5 );

    int && y = x; // Error. An rValue reference cannot be pointed to a lValue.
    int && z = 9;
    return 0;
}
```

### Big-Five

- Destructor

- Copy Constructor

  It's the `copy constructor` if the existing object is an lvalue.

- Move Constructor

  It's the `move constructor` if the existing object is an rvalue.

- Copy Assignment operator=

- Move Assignment operator=

### struct

In C++, the `struct` is a relic from the C programming language. A `struct` in C++ is essentially a `class` in which the members default to public. Recall that in a `class`, the members default to private.