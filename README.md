# 주소 연산식
주소 연산은 변수나 함수의 주소를 계산합니다.

`&` `식`

`식`은 변수나 함수를 가리켜야 합니다. 

주소 연산 결과의 타입을 포인터라고 합니다. 

#### 코드 예시:
```c
int i = 0; /* int 타입의 전역변수 i, 초기값은 0 */
int *pi = &i; /* int 포인터 타입의 전역변수 pi, 초기값은 i의 주소 */
```

#### 관련 C89 표준
[3.3.3.2 Address and indirection operators](https://port70.net/~nsz/c/c89/c89-draft.html#3.3.3.2)
> **Constraints**
> The operand of the unary & operator shall be either a function designator or an lvalue that designates an object ...
>
> **Semantics**
>
> The result of the unary & (address-of) operator is a pointer to the object or function designated by
> its operand. If the operand has type " type ", the result has type "pointer to type ".
