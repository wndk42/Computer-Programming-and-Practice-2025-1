# 지역변수선언
지역변수는 함수 안에서 쓴다고 선언된 변수입니다. 
지역변수를 선언하는 문법과 전역변수를 선언하는 문법은 똑같습니다.

초기값이 없는 변수선언은 `타입` `이름` `;` 형태로 합니다.

초기값이 없는 변수선언은 `타입` `이름` `=` `식` `;` 형태로 합니다. 

#### 코드 예시:
```c
void f() {
   int x = 1; /* f 함수를 실행할 때마다 새로 할당되고 없어지는 변수 x */
}

void g() {
   int x = 1; /* g 함수를 실행할 때마다 새로 할당되고 없어지는 변수 x */
}
```

# 관련 C89 표준
3.1.2.1 Scopes of identifiers
>
> An identifier is visible (i.e., can be used) only within a region of program text called its scope.
> There are ... kinds of scopes: ... , file, block, and function prototype.
> (A function prototype is a declaration of a function that declares the types of its parameters).
>
> ... identifier has scope determined by the placement of its declaration ...
> If the declarator ... that declares the identifier appears outside of any block or list of parameters,
> the identifier has file scope, which terminates at the end of the translation unit.
> If the declarator ... that declares the identifier appears inside a block or
> within the list of parameter declarations in a function definition,
> the identifier has block scope, which terminates at the } that closes the associated block.
> If the declarator ... that declares the identifier appears within the list of parameter declarations
> in a function prototype (not part of a function definition), the identifier has function prototype scope,
> which terminates at the end of the function declarator.
> If an outer declaration of a lexically identical identifier exists in the same name space,
> it is hidden until the current scope terminates, after which it again becomes visible.

3.1.2.2 Linkage of identifiers
>
> An identifier declared in different scopes or in the same scope more than once can be made to refer
> to the same object or function by a process called linkage. There are three kinds of linkage:
> external, internal, and none.
>
> In the set of translation units and libraries that constitutes an entire program,
> each instance of a particular identifier with external linkage denotes the same object or function.
> Within one translation unit, each instance of an identifier with internal linkage denotes the
> same obejct or function.
> Identifiers with no linkage denote unique entities.
>
> The following identifiers have no linkage: ... an identifier declared to be a function parameter;
> an identifier declared to be an object inside a block witout the storage-class specifier extern.

3.1.2.4 Storage durations of objects
>
> an object has a storage duration that determines its lifetime.
> There are two storage durations: static and automatic.
> An object declared with no linkage and without the storage-class specifier static has
> automatic storage duration. Storage is guaranteed to be reserved for a new instance of such an object
> on each normal entry into the block in which it is declared ...
> If an initialization is specified for the value stored in the object, it is performed on each normal entry
> ... Storage for the object is no longer guaranteed to be reserved when execution of the block ends in
> any way. (Entering an enclosed block suspends but does not end execution of the enclosing block.
> Calling a function that returns suspends but does not end execution of the block containing the call.)
> The value of a pointer that referred to an object with automatic storage duration that is no longer
>guranteed to be reserved is indeterminate. 

1.6 DEFINITIONS OF TERMS
> Object ---  region of data storage in the execution environment, the contents of which can represent
> values. Except for bit-fields, objects are compsoed of contiguous sequences of one or more bytes,
> the number, order, and encoding of which are either explicitly specified or implementation-defined.
