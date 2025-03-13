# 여러 소스파일

프로그램의 코드가 여러 소스파일에 나눠져 있을 수 있습니다. 
기계어로 번역되어있는 파일에 있는 함수를 쓸 수도 있습니다. 
다른 파일에 있는 함수를 쓸 때도 함수 선언을 하고 쓰면 됩니다.

#### 코드 예시:
```c
/* main.c */

int value(int); /* 반환타입이 int고, 매개변수타입도 int인 함수 value를 선언 */

int main() {
   return value(5);
}
```

```c
/* value.c */

int value(int); /* value 함수 선언 */

/* value 함수 정의 */
int value(int x) {
   return x;
}
```

#### 관련 C 표준
2.1.1.1 Program structure
> A C program need not all be translated at the same time.
> The text of the program is kept in units called source files in this Standard.
> A source file ... is called a translation unit.
> ... The seperate translation units of a program communicate by (for example) calls to functions
> whose identifiers have external linkage,
> by manipulation of objects whose identifiers have external linkage,
> and by manipulation of data files.
> Translation units may be separately translated and then later linked to produce an executable program.
