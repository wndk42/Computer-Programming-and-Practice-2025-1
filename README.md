# 배열 타입
배열 타입은 같은 타입 여러개를 메모리에 차례로 늘어놓은 것을 뜻합니다.

`타입` `이름` `[` `식` `]` `;` 형태로 배열을 선언할 수 있습니다.

여기서 식은 상수로 계산되어야 합니다.

#### 코드 예시:
```c
char ca[10]; /* char 타입 10개를 늘어놓은 배열 ca를 전역변수로 선언합니다. */
```

#### 관련 C89 표준
[3.1.2.5 Types](https://port70.net/~nsz/c/c89/c89-draft.html#3.1.2.5)
> An array type describes a contiguously allocated set of objects with a particular member object type, called the element type.
> Array types are characterized by their element type and by the number of members of the array.
> An array type is said to be derived from its element type, and if its element tye is T,
> the array type is sometimes called "array of T".
> The construction of an array type from an element type is called "array type derivation".
>
> An array type of unknown size is an incomplete type. It is completed, for an identifier of that type,
> by specifying the size in a later declaration (with internal or external linkage).
>
> Array, function, and pointer types are collectively called derived declarator types.
> A declarator type derivation from a type T is the construction of a derived declarator type from T by the application
> of an array, a function, or a pointer type derivation to T.

[3.5.4.2 Array declarators](https://port70.net/~nsz/c/c89/c89-draft.html#3.5.4.2)
> **Semantics**
> If, in the declaration " T D1 ", D1 has the form
>
> D[ constant-expression<opt> ]
>
> and the type specified for ident in the declaration " T D " is "derived-declarator-type-list T",
> then the type specified for ident is " derived-declarator-type-list array of T".
> If the size is not present, the array type is an incomplete type.
