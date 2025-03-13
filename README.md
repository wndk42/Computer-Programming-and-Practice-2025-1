# 함수정의 (매개변수리스트가 있을 때)

함수 정의는 함수의 이름, 반환타입, 매개변수의 타입과 이름, 실행할 문장리스트를 정합니다.  
함수 실행하는 동안 매개변수에 저장된 값을 읽거나 새로운 값을 매개변수에 저장할 수 있습니다. 
매개변수는 함수를 호출할 때마다 메모리를 새로 할당받고, 호출시 전달된 값으로 초기값이 저장됩니다.
매개변수가 없는 함수를 정의할 때는 괄호 안에 void만 적거나, 괄호 안을 비워놓습니다. 

`타입` `이름` `(` `매개변수리스트` `)` `{` `문장리스트` `}` 형태로 함수정의를 합니다.

`매개변수리스트`는 `매개변수선언` 또는 `매개변수리스트` `,` `매개변수선언` 입니다. 

`매개변수선언`은 `타입` `이름` 입니다. 

#### 코드 예시:
```c
int f(int a, int b) { return a; } /* 첫번째 매개변수를 반환하는 함수 */
int g(int a, int b) { return b; } /* 두번째 매개변수를 반환하는 함수 */
int h(void) { return 1; } /* 1을 반환하는 함수 */
```

### 관련 C 표준
3.7.1 Function definitions
> Constraints
>
> If the declarator includes a parameter type list,
> the declaration of each parameter shall include an identifier
> (except for the specifal case of a parameter list consisting of a single parameter of type void,
> in which there shall not be an identifier).
>
> Semantics
>
> ... parameter type list ... specifies the types of all the parameters;
> ... also servers as a function prototype for later calls to the same function in the same translation unit.
> ...
> 
> On entry to the function the value of each argument expression shall be converted to the
> type of its corresponding parameter, as if by assignment to the parameter. ...
