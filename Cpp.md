# C++

## [auto_ptr<>](https://en.cppreference.com/w/cpp/memory/auto_ptr)

- depracted in C++11 and removed in C++17 -> use [`unique_ptr`](https://en.cppreference.com/w/cpp/memory/unique_ptr)
- `Because of these unusual copy semantics, auto_ptr may not be placed in standard containers`

Test struct `printer`:
```cpp
#include <iostream>
#include <memory>

struct printer {
    void print() {
        printf("test");
    }
};
```

1) variable
```cpp
int main() {
    printer p;

    p.print();
    return 0;
}
```

2) pointer
```cpp
int main() {
    printer* p;
    p = new printer();

    p->print();
    return 0;
}
```

3) auto_prt<>
```cpp
int main() {
    std::auto_ptr<printer> p(new printer());

    p->print();
    return 0;
}
```

4) auto_ptr<> -> pass to function
```cpp
void test(printer & p) {
    p.print();
}

int main() {
    std::auto_ptr<printer> p(new printer());

    //p->print();
    test(*p);
    return 0;
}
```

5) unique_ptr<> -> pass to function
```cpp
int main() {
    std::unique_ptr<printer> p(new printer());

    //p->print();
    test(*p);
    return 0;
}
```

Stack Overflow discusion: [Can i pass auto_ptr by reference to functions?](https://stackoverflow.com/questions/2486616/can-i-pass-auto-ptr-by-reference-to-functions)
