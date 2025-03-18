# 정수 타입
정수 타입은 부호가 있는 정수 타입과 부호가 없는 정수 타입으로 나눠집니다. 

부호가 있는 정수 타입으로는 `signed char`, `short int`, `int`, `long int`가 있습니다. 
오른쪽으로 갈수록 같거나 더 넓은 범위의 정수를 표현할 수 있습니다. 

부호가 없는 정수 타입은 부호가 있는 정수 타입에서 `signed`를 `unsigned`로 바꾸거나, `unsigned`를 붙여서 만듭니다.
메모리 공간의 크기는 같지만 음이 아닌 정수만 나타내므로 더 큰 숫자까지 나타낼 수 있습니다.

#### 코드 예시:
```c
unsinged int i = 0; /* 변수 i에는 음이 아닌 값이 저장됩니다 */
```

#### 관련 C89 표준
[3.1.2.5 Types](https://port70.net/~nsz/c/c89/c89-draft.html#3.1.2.5)
> The type char, the signed and unsigned integer types, ... are collectively called integral types.
> The representations of integral types shall define values by use of a pure binary numeration system. ...
>
> There are four signed integer types, designated as signed char, short int, int, and long int.
> (The signed integer and other types may be designated in several additional ways, ...)
>
> An object declared as type signed char occupies the same amount of storage as a "plain" char object.
> A "plain" int object has the natural size suggested by the architecture of the execution environment. ...
> In the list of signed integer types above, the range of values of each type is a subrange of the values of the next type in the list.
>
> For each of the signed integer types, there is a corresponding (but different) unsigned integer type (designated with the keyword unsigned)
> that uses the same amount of storage (including sign information) ... The range of nonnegative values of a signed integer type is a
> subrange of the corresponding unsigned integer type, ...
>
> The type char, the signed and unsigned integer types, ... are collectively called the basic types.
> Even if the implementation defines two or more basic types to have the same representation, they are nevertheless different types.
>
> Integral and ... types are collectively called arithmetic types. ...

[3.5.2 Type specifiers](https://port70.net/~nsz/c/c89/c89-draft.html#3.5)
> **Constraints**
> Each list of type specifiers shall be one of the following sets;
> the type specifiers may occur in any order,
> possibly intermixed with the other declaration specifiers.
>
> signed char
>
> unsigned char
>
> short, signed short, short int, or signed short int
>
> unsigned short, or unsigned short int
>
> int, signed, signed int, or ...
>
> unsigned, or unsigned int
>
> long, signed long, long int, or signed long int
>
> unsigned long, or unsigned long int
>
> **Semantics**
> Each of the above comma-seperated lists designates the same type, ...
