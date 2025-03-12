# 함수호출식 (매개변수가 없는 함수)

함수를 실행하는 것을 함수를 호출한다고 합니다. 
함수를 호출하는 것은 값을 쓰거나 더하기를 하는 것처럼 결과로 값을 얻습니다. 
실행 결과를 얻는 것을 식이라고 하고, 식은 문장의 일부로 쓰입니다. 

`식` `(` `)` 형태로 씁니다. 

`(` 왼쪽의 `식`은 함수를 가리켜야 합니다. 

#### 코드 예시:
```c
int main() {
   return main(); /* 자신을 무한히 호출해서 에러가 발생합니다 */
}
```

#### 관련 C89 표준
3.3.2.2 Function calls
> Semantics
>
> ... expression followed by parentheses () containing a possibly empty ... is a function call.
> ... expression denotes the called function. ...
> ... Recursive function calls shall be permitted, both directly and indirectly through any chain of other functions.
