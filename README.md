## Basic-Syntax-variable-data-types-for-c


### what is programming?

-Programming is the process of creating specific instructions—or code—that tell a computer how to perform tasks, solve problems, or automate processes.

### how c language work?

-C is a compiled, procedural programming language that works by translating human-readable source code into machine code that a computer's processor can execute directly

### why c?

- Its too structured and mother of programming language
- There is no built in library or function so we can learn from 0.



### 1-1 Structure Of C Programming 

- it has two parts 
  1. **Head Part** - hold the header files (saves time and make us avoid some complicated code running behind the scene) 
  2. **Main Part** - Holds the main code

### 1-2 First C Program 
- c programming syntax 
```c
# include <stdio.h>
int main ()

{
    printf("hello world"); // we have not wrote the function of printing its coming from header file 
    return 0;
}
```
- the *stdio* means the *standard input and output* 

### Running Our First C Code

```c
# include <stdio.h>
int main () // this is the main function and its a function return type

{
    printf("hello world"); // we have not wrote the function of printing its coming from header file 
    return 0; // return 0 means the code has run successfully
}
```
- c programming starts to execute from main function 

### Printing in C 

```c
#include<stdio.h>
int main()
{
    printf("I am Sazid\n"); // for printing with brake \n is used 
    printf("demon\n");
    printf("dem\ton");
    return 0;
}
```

- for printing with brake **\n** is used
- for the *Tab Space* we can use *\t*

### Variable and Data Type

1. *int* -> -100, 0, 100
2. *float* -> -2.5, 5.46
3. *char* -> 'a', 'A', '@', 'H'
4. *boolean* -> True or False

### Variables in C 

```
data-type variable name 
```

```c
#include<stdio.h>
int main()
{
    int num; // declaring avariable will be stored in memory and we will assign data. 
    num=10;
    // or we can also write 
    int num1 = 10; 
    num1 = 20;
    float f = 3.56;
    char c = 'i am sazid';
    return 0;
}
```
- variable is stored in memory and value is assigned and the code will be executed line by line 

- *int* holds *4 byte space* in memory, *float* holds *4 byte space* in memory, *char* holds *1 byte space* in memory
- *1 byte* means *8 bit*. 010101(here is 6 bit) as compute understand 0 and 1 these are bit. 
- *1024 bit* means *1 kb*
- *1024 kb* means *1 mb*
- *1024 mb* means *1 gb*
- *1024 gb* means *1 tb*

## print a variable 

```c
#include<stdio.h>
int main()
{
    int num; // declaring avariable will be stored in memory and we will assign data. 
    num=10;
    // or we can also write 
    int num1 = 10; 
    num1 = 20;
    float f = 3.56;
    char c = 'i am sazid';
    printf("num1"); // we cant print like this 
    return 0;
}
```
- we cant print like this **We need format specifier** for printing variables 
1. *int* -> %d
2. *float* -> %f
3. *char* -> %c

```c
#include<stdio.h>
int main()
#include<stdio.h>
int main()
{
    int num; // declaring avariable will be stored in memory and we will assign data. 
    num=10;
    // or we can also write 
    int num1 = 10; 
    num1 = 20;
    float f = 3.56;
    char c = 'i am sazid';
    // printf("num1"); // we cant print like this 
    printf("%d", num1);
    printf("%f", f);
    printf("%2f", f);
    printf("%c", c);
    return 0;
}
```
## Boolean in c

- boolean datatype is hold in another header 

```c
#include<stdbool.h>
```
- print 

```c
#include<stdio.h>
#include<stdbool.h>
int main()
{
bool b;
b = false;
printf("%d", b); // boolean has no format specifier so we will be using the integer specifier as it only about 0 and 1 
return 0;
}
```
### how to take input 
- for taking input we need a function name *scanf()* same as printf. we also need a *format specifier* for this 

```c
#include <stdio.h>
int main()
{
    int a;
    scanf("%d", &a); // it will take file and keep in a . its like as int is defined and defined a garbage value (0 or other) and the scanf will replace the taken input value. & meas the address of a . its responsible for changing the value
    printf("%d", a);
    return 0;
}
```

```c
#include <stdio.h>
int main()
{
    int a;
    float f;
    char c;
    scanf("%d", &a); // it will take file and keep in a . its like as int is defined and defined a garbage value (0 or other) and the scanf will replace the taken input value. & meas the address of a . its responsible for changing the value
    scanf("%f", &f);
    scanf(" %c", &c); 

    printf("%d\n", a);
    printf("%c\n", c);
    printf("%f\n", f);

    // we can also take multiple fields as well
    scanf("%d %f %c", &a, &f, &c);
    printf("%d\n%f\n%c\n", a, f, c);
    return 0;
}
```

### data type limitations 
- data types has a fixed size. like large integer we have to use *long long int* -> size 8 byte
- for large float we have to use *double* -> 8 byte

### lets calculate the size of the data types or data 
- 1 bit mean either 0 or 1 
- 2 bit means -> 00, 01, 10, 11 we can keep 4 numbers 
- 3 bit means -> 000, 001, 010, 011, 100, 101, 110, 111

#### Lets make a pattern 
- 2 power is the base 1 bit means 2 power 1
- 32 bits means 2 power 32 .
- we can keep 10 to the power 9 value max to a integer if more we have to use *long long int* it can take 10 to the power 18 

```c
#include <stdio.h>
int main()
{
    long long int a;
    printf("%lld", a); // specifier will be lld 
    return 0;
}
```
- for float we also have limitation 
- we have to use *double*

```c
#include <stdio.h>
int main()
{
    double f;
    printf("%lf", f);
    return 0;
}
```

## naming of variable 
1. ibrahim 
2. _ibrahim 
3. @rahim -> we cant do it 
4. 123rahim -> we cant do it 
5. alu 123 ->  we cant do it 
6. epok_123
7. rahim123
8. rahim,karim -> we cant use it 
9. int -> we can do it (or any c reserved words)
