# 정수 값
10진수, 16진수, 8진수로 정수값을 표현할 수 있습니다.   

10진수는 `1-9숫자` `0-9숫자` 형태로 씁니다. `0-9`숫자는 없어도 되고 여러개 있어도 됩니다. 

16진수는 `0x` `0-f숫자` 형태로 씁니다. `0-f`숫자는 1개 이상 있어야 합니다. 대문자로 써도 됩니다. 

8진수는 `0` `0-7` 형태로 씁니다. `0-7`숫자는 없어도 되고 여러개 있어도 됩니다. 


#### 코드 예시:
```c
int x() {
   return 0x01; /* 1을 반환합니다. */
}
```

#### 관련 C89 표준
[3.1.3.2 Integer constants](https://port70.net/~nsz/c/c89/c89-draft.html#3.1.3.2)
> **Description**
>
> An integer constant begins with a digit, but has no period or exponent part.
> It may have a prefix that specifies its base and a suffix that specifies its type.
>
> A decimal constant begins with a nonzero digits and consists of a sequence of decimal digits.
> An octal constant consists of the prefix 0 optionally followed by a sequence of the digits 0 through 7 only.
> A hexadecimal constant consists of the prefix 0x or 0X followed by a sequence of the decimal digits
> and the letters a (or A) through f (or F) with values 1o through 15 respectively.
>
> **Semantics**
>
> The value of a decimal constant is computed base 10; that of an octal constant, base 8;
> that of a hexadecimal constant, base 16. The lexically first digit is the most significant.
>
> The type of an integer constant is the first of the corresponding list in which its value can be represented.
> Unsuffixed decimal: int, long int, unsigned long int;
> unsuffixed octal or hexadecimal: int, unsigned int, long int, unsigned long int;
> suffixed by the letter u or U: unsigned int, unsigned long int;
> suffixed by the letter l or L: long int, unsigned long int;
> suffixed by both the letters u or U and l or L: unsigned long int.
