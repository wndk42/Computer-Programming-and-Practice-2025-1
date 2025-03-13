# return문
return 문장은 함수가 실행될 때 함수 실행을 종료합니다. 

함수 실행이 종료되고 나면 함수를 실행시킨 곳으로 이동합니다. 

return문에는 식이 있는 return문과 식이 없는 return문 두 종류가 있습니다. 

식이 있는 return문은 함수 실행 결과값을 정하고, 식이 없는 return문은 함수 실행 결과값을 정하지 않습니다. 

함수 실행 중에 문장리스트의 끝에 도달하면 식이 없는 return문을 실행한 것과 동일하게 함수 실행이 종료됩니다.

식이 없는 return문으로 함수가 종료된 후에 실행결과값을 사용하면 어떤 동작을 하는지 정해지지 않았습니다.

`return` `식` `;` 형태로 쓰거나, `return` `;` 형태로 씁니다.


#### 코드 예시:
```c
int x() {
   return 1; /* 함수 실행을 종료하고 1을 실행한 결과값으로 반환 */
}
```

#### 관련 C89 표준
3.6.6.4 The return statement
> Constraints
>
> A return statement with an expression shall not appear in a function whose return type is void.
> 
> Semantics
>
> A return statement terminates execution of the current function and returns control to its caller.
> A function may have any number of return statements, with and without expressions.
>
> If a return statement with an expression is executed,
> the value of the expression is returned to the caller as the value of the function call expression.
> If the expression has a type different from that of the function in which it appears,
> it is converted as if it were assigned to an object of that type
>
> If a return statement without an expression is executed, and the value of the function call is used by the caller, the behavior is undefined.
> Reaching the } that terminates a function is equivalent to executing a return statement without an expression.

1.6 DEFINITIONS OF TERMS
> * Undefined behavior --- behavior, upon use of a nonportable or erroneous program construct,
> of erroneous data, or of indeterminately-valued objects, for which the Standard imposes no requirements.
> Permissible undefined behavior ranges from ignoring the situation completely with
> unpredictable results, to behaving during translation or program execution in a documented
> manner characteristic of the environment (with or without the issuance of a diagnostic message),
> to terminating a translation or execution (with the issuance of a diagnostic message).
>
> If a "shall" or "shall not" requirement that appears outside of a constraint is violated,
> the behavior is undefined. Undefined behavior is otherwise indicated in this Standard by the words
> "undefined behavior" or by the omission of any explicit definition of behavior.
> There is no difference in emphasis among these three; they all describe "behavior that is undefined."
