# 포인터 타입
포인터 타입은 함수, 변수 등의 주소를 저장할 수 있는 타입입니다.

`타입` `*` `이름` `;` 형태로 변수를 가리키는 포인터를 선언할 수 있습니다.

`타입` `(` `*` `이름` `)` `(` `)` 형태로 함수를 가리키는 포인터를 선언할 수 있습니다. 

#### 코드 예시:
```c
int *ptr_to_int; /* int 타입의 주소를 저장할 수 있는 포인터 타입의 변수 ptr_to_int를 선언합니다. */
```

#### 관련 C89 표준
[3.1.2.5 Types](https://port70.net/~nsz/c/c89/c89-draft.html#3.1.2.5)
> A pointer type may be derived from a function type, an object type, or an incomplete type, called the reference type.
> A pointer type describes an object whose value provides a reference to an entity of the referenced type.
> A pointer type derived from the referenced type T is sometimes called "pointer to T".
> The construction of a pointer type from a referenced type is called "pointer type derivation".
>
> Arithmetic types and pointer types are collectively called scalar types.
>
> Array, function, and pointer types are collectively called derived declarator types.
> A declarator type derivation from a type T is the construction of a derived declarator type from T
> by the application of an array, a function, or a pointer type derivation to T.

[3.5.4.1 Pointer declarators](https://port70.net/~nsz/c/c89/c89-draft.html#3.5.4.1)
> **Semantics**
> If, in the declaration " T D1 ", D1 has the form
>
> \* type-qualifier-list<opt> D
>
> and the type specified for ident in the declaration " T D " is "derived-declarator-type-list T",
> then the type specified for ident is "derived-declarator-type-list type-qualifier-list pointer to T".
> For each type qualifier in the list, ident is a so-qualified pointer. 
