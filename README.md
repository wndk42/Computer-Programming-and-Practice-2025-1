# 문자 타입
문자 타입은 소스 파일의 문자들을 저장할 수 있는 크기인 1바이트를 가지며, 이진수로 표현됩니다.  

문자 타입은 정수 타입의 일종입니다. 

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
