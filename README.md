# 문자 타입
문자 타은 문자에 해당하는 정수를 나타냅니다.   

`'` `문자` `'` 형태로 씁니다. `문자`는 작은 따옴표 `'`, 역슬래시 `\`, 엔터를 제외하고 쓸 수 있고, 특수문자 문법을 쓸 수도 있습니다. 

문자 타입의 크기는 1 바이트입니다. 

1 바이트의 크기는 최소 8비트로 정해져있는데, 대부분 8비트입니다. 

각 문자에 해당하는 정수는 컴파일러에서 정합니다. 

문자가 여러개 있을 경우, 한국어 사용 등의 경우에 해당하는 정수도 컴파일러에서 정합니다.  

#### 코드 예시:
```c
char c = 'a'; /* 변수 c는 1 바이트의 메모리 공간을 할당받습니다 */
```

#### 관련 C89 표준
[3.1.2.5 Types](https://port70.net/~nsz/c/c89/c89-draft.html#3.1.2.5)
> The meaning of a value stored in an object or returned by a function is determined by the type of the expression used to access it.
> (An identifier declared to be an object is the simplest such expression; the type is specified in the declaration of the identifier.)
> Type are partitioned into object types (types that describe objects), function types (types that describe functions), and incomplete types
> (types that describe objects but lack information needed to determine their sizes).
>
> An object declared type char is large enough to store any member of the basic execution character set.
> If a member of the required source character set enumerated in 2.2.1 is stored in a char object, its value is guranteed to be positive. ...
>
> The type char, ... are collectively called integral types. The representations of integral types shall define values by use of
> a pure binary numeration system. ...

[3.3.3.4 The sizeof operator](https://port70.net/~nsz/c/c89/c89-draft.html#3.3.3.4)
> ... the size (in bytes) of
>
> ... type char ... is 1. ...

[1.6 DEFINITIONS OF TERMS](https://port70.net/~nsz/c/c89/c89-draft.html#1.6)
> \* Byte --- the unit of data storage in the execution environment large enough
> to hold any member of the basic character set of the execution environment.
> It shall be possible to express the address of each individual byte of an object uniquely.
> A byte is composed of a contiguous sequence of bits,
> the number of which is implementation-defined.
> The least significant bit is called the low-order bit,
> the most significant bit is called the high-order bit.

[2.2.4.2 Numerical limits](https://port70.net/~nsz/c/c89/c89-draft.html#2.2.4.2)
> ... Their implementation-defined values shall be equal or greater in magnitude (absolute value) to those shown, with the same sign.
> \* maximum number of bits for smallest object that is not a bit-field (byte) CHAR_BIT 8
