# 식문
식 문장은 식을 계산하고, 계산 결과는 버립니다.  

주로 메모리에 값을 저장하거나, 함수 호출을 합니다. 

`식` `;` 형태로 씁니다.


#### 코드 예시:
```c
int x() {
   x(); /* 자기 자신을 호출합니다. 무한히 반복됩니다. */
   return 1; /* 무한 재귀 호출로 인해 여기까지 도달할 수 없습니다. */
}
```

#### 관련 C89 표준
[3.6.3 Expression and null statement](https://port70.net/~nsz/c/c89/c89-draft.html#3.6.3)
> Semantics
>
> The expression in an expression statement is evaluated as a void expression for its side effects.
