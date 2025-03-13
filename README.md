# 전역변수선언
변수는 값을 저장할 수 있는 메모리 공간입니다. 
전역변수는 소스 파일에 있는 모든 코드에서 쓸 수 있습니다. 
같은 전역변수를 여러번 선언할 경우 한번만 메모리 공간을 할당받습니다.
전역변수 선언에서 초기화를 하면 처음 메모리 공간을 할당받을 때 초기값을 저장합니다.
한 전역변수에 대해서 초기화는 한번만 할 수 있습니다. 
전역변수의 초기값으로는 상수만 쓸 수 있습니다. 

초기값이 없는 변수선언은 `타입` `이름` `;` 형태로 합니다.

초기값이 없는 변수선언은 `타입` `이름` `=` `식` `;` 형태로 합니다. 

#### 코드 예시:
```c
int x = 1; /* 초기값이 1인 int 타입의 전역변수 x를 선언하고, 메모리 공간을 할당받음 */
int x; /* int 타입의 전역변수 x를 선언. 메모리 공간은 앞에서 할당받았으므로 할당받지 않음 */

int get_x() {
   return x; /* 함수 정의의 문장리스트에서 x의 값에 접근 가능 */
}
```

# 관련 C89 표준
3.7 EXTERNAL DEFINITIONS
>
>Semantics
>... An external definition is an external declaration that is also a definition of a function or an object
>If an identifier declared with external linkage is used in an expressioin (...),
>somewhere in the entire program there shall exactly one external definition for the identifier.

3.7.2 External object definitions
>
>Semantics
>If the declaration of an identifier has file scope and an initializer,
>the declaration is an external definition for the identifier.
>
>A declaration of an identifier for an object that has file scope without an initializer, ..., constitutes a tentative definition.
>If a translation unit contains one or more tentative definitions for an identifier,
>and the translation unit contains no external definition for that identifier,
>then the behavior is exactly as if the translation unit contains a file scope declaration of that identifier,
>with an initializer equal to 0. ...




>A
