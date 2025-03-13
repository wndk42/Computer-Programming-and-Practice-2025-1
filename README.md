# <stdio.h> 라이브러리의 printf 함수
<stdio.h> 헤더 파일에는 입력과 출력에 관련된 함수들의 선언이 있습니다. 
printf함수는 콘솔창에 문자열을 표시할 수 있고, 표시할 문자열 안에 값들을 넣을 수 있습니다. 
printf함수의 반환값은 출력한 문자의 개수이며, 에러가 발생했을 때는 음수가 반환됩니다.
printf함수는 가변 개수 매개변수라는 문법으로 선언 및 정의되어 있어서 매개변수의 개수는 한개 이상이면 모두 가능합니다.

printf 함수를 호출할 때 첫번째 매개변수에는 문자열을 씁니다. 

문자열은 `"` `문자들` `"` 형태로 씁니다. 

#### 예제 코드:
```c
int main() {
   return printf("C"); /* 화면에 C가 출력된 후 출력된 글자 개수가 반환됩니다. */
}
```

#### 관련 C89 표준
4.9.6.3 The printf function
> Description
>
> The printf function is equivalent to fprintf with the argument stdout interposed before the arguments to printf.
>
> Returns
> The printf function returns the number of characters transmitted, or a negative value if an output error occurred.

4.9.6.1 The fprintf function
> Description
>
> The fprintf function writes output to the stream pointed to by stream,
> under control of the string pointed to by format that specifies how subsequent arguments are converted
> for output. ...
>
> Returns
> The fprintf function returns the number of characters transmitted, or a negative value if an output error occrured.

4.9.1 Introduction
> stdout ... point to the ... standard ... output streams.
