# 함수선언 (매개변수가 없을 때)

함수 선언은 함수 정의, 전역변수 선언과 더불어 전처리 후의 C 프로그램을 구성합니다. 
함수 선언은 이름이 특정 반환타입의 함수를 가리킨다고 정합니다. 

`타입` `이름` `(` `)` `;` 형태로 씁니다.

#### 코드 예시:
```c
/* 반환 타입이 void고, 이름이 x인 함수의 선언 */
void x();
```

#### 관련 C89 표준
3.5.4.3 Function declarators (including prototypes)
> Semantics
>
> If, in the declaration "T D1", D1 has the form
>
> D( ... )
>
> ... then the type specified for ident is " ... function returning T." 
