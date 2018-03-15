### static const int* a / const static int* a / static int* const a / static int const* a 之间有什么区别？

```static const int* a;```

``` const static int* b;``` 

``` static int* const c;```

``` static int const* d;```

```const int* const e```



- 对于static 和 const，优先级相同顺序不影响，故static const 和 const static 修饰含义相同,a == b;
- static的修饰含义分为全局静态文件(不可被extern)，局部静态变量(不会销毁),故四者无区别;
- 对于int* const  / const int* / int const*,const的修饰目标不同
  - int* const修饰变量，表示一个指向int型的const指针c，它必须被赋初值，且指针的值不可修改；
  - const int*修饰int,表示一个const int型指针a,b，他们指向一个const型int变量，不可通过指针修改这个变量的值；
  - int const*修饰int,表示int const型指针，实际和const int含义相同，a == d;
- 对于e，为两者结合体，即指向const int型常量的const指针，即不能修改指针指向，也不能修改指向的值；