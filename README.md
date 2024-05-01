## EXPERIMENT-9-SIMPLE IF STATEMENT

## AIM:
   - To print the word "APPLE" `n` times.

## ALGORITHM:
   1. Begin the program.
   2. Declare a variable `n` of type int.
   3. Input the value of `n`.
   4. Use a for loop to iterate `n` times:
      - Print "APPLE" followed by a newline.
   5. End the program.
## PROGRAM :
```
#include <stdio.h>
int main()
{
    int n;
    scanf("%d", &n);
    for (int i = 0; i < n; i++)
    {
        printf("APPLE\n");
    }

    return 0;
}
```
## SAMPLE OUTPUT:
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/dfebca03-6a7c-4f61-ba76-e324196cd39c)
## OUTPUT :
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/5a807714-40ff-499b-82f9-7dac30276aeb)


## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-10-NUMBER SEQUENCE PRINTER

### AIM:
To create a program that prints a sequence of numbers from 1 to `n`, separated by colons.

### ALGORITHM:
1. Begin the program.
2. Declare a variable `n` of type int to store the upper limit of the number sequence.
3. Prompt the user to input the value of `n`.
4. Read the input value for `n` using `scanf()` function.
5. Use a for loop with loop variable `i` initialized to 1, terminating condition `i <= n`, and incrementing `i` by 1 in each iteration:
   - Inside the loop, print the value of `i`.
   - If `i` is less than `n`, print a colon followed by a space.
6. End the program.
## PROGRAM :
```
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    for (int i=1;i<=n;i++)
    {
        printf("%d",i);
        if(i<n)
        printf(" : ");
    }
    return 0;
}
```
## SAMPLE OUTPUT:
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/868d77de-e7f9-4659-9e6a-983ef1840a84)

## OUTPUT :
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/634ea6c3-8fc9-4c40-91cb-66f1226f435f)


## RESULT:
Thus the required program is written and executed successfully.

## EXPERIMENT-11-NUMBER PATTERN GENERATOR

### AIM:
To develop a program that generates a numerical pattern.

### ALGORITHM:
1. Begin the program.
2. Declare variables `i`, `j`, and `n` of type int.
3. Assign the value 10 to variable `n`.
4. Use a nested for loop structure to iterate over rows and columns:
   - Outer loop (`i` loop) iterates from 1 to `n`.
   - Inner loop (`j` loop) iterates from 1 to `i`, printing values incrementally.
   - After the inner loop, use another loop to print values in descending order, iterating from `i-1` to 1.
   - Print a newline after each row.
5. End the program.
## PROGRAM :
```
#include<stdio.h>
int main(){
    int i,j,n;
    n=10;
   
    for(i=1;i<=n;i++)
    {
        for(j=1;j<=i;j++)
        {
            printf("%d",j);
        }
for(j=i-1;j>=1;j--)
        {
            printf("%d",j);
        }
        printf("\n");
    }
        
    }

```
## SAMPLE OUTPUT:
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/918f9013-2f39-483d-bd62-bfe6acccb7b6)

## OUTPUT :
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/79a69535-50e7-4498-9917-a255477be190)


## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-12-DIAMOND PATTERN PRINTER

### AIM:
To create a program that prints a diamond pattern using the character '%' as the pattern element.

### ALGORITHM:
1. Begin the program.
2. Declare variables `n`, `i`, `j`, `s`, and `l` of type int, where `n` is assigned the value 3.
3. Declare a character variable `x` and assign it the value '%'.
4. Use a for loop with loop variable `i` initialized to `-n`, terminating condition `i <= n`, and incrementing `i` by 1 in each iteration:
   - Inside the loop:
     - Print leading spaces.
     - Determine the value of `l` based on the absolute value of `i`.
     - Print spaces to adjust the position of the pattern element.
     - Print the '%' character for each row.
     - Print a newline character.
5. End the program.
## PROGRAM :
```
#include<stdio.h>
int main(){
    int n=3,i,j,s,l;
    char x='%';
    for(i=-n;i<=n;i++){
        printf("           ");
        if(i<0) 
            l=-i;
        else
            l=i;
        for(s=0;s<n-l;s++){
            printf("  ");
        }
        for(j=0;j<n-l+1;j++){
            printf("%c ",x);
        }
        printf("\n");
    }
}

```
## SAMPLE OUTPUT:
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/9d9aff63-edc5-4249-908a-2404f181ff4d)

## OUTPUT :
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/403e21a8-52a1-4e0d-bc02-4b92cc9dbbe1)

## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-13-FIBONACCI SERIES PRINTER

### AIM:
To create a program that prints the Fibonacci series up to the `a`th term.

### ALGORITHM:
1. Begin the program.
2. Declare a function `fibo(int a)` to calculate and print the Fibonacci series up to the `a`th term.
   - Initialize variables `x` and `y` to 0 and 1 respectively.
   - Use a for loop with loop variable `i` initialized to 0, terminating condition `i < a`, and incrementing `i` by 1 in each iteration:
     - Print the value of `x`.
     - Calculate the next Fibonacci number `z` by adding `x` and `y`.
     - Update the values of `x` and `y` for the next iteration.
3. In the `main()` function:
   - Declare a variable `a` of type int to store the term up to which Fibonacci series is to be printed.
   - Prompt the user to input the value of `a`.
   - Read the input value for `a` using `scanf()` function.
   - Call the `fibo()` function with argument `a`.
4. End the program.
## PROGRAM :
```
#include <stdio.h>
void fibo(int a)
{
    int x=0,y=1,z;
    for(int i=0;i<a;i++)
    {
        printf("%d ",x);
        z=x+y;
        x=y;
        y=z;
        
    }
    
    
}
int main()
{
    int a;
    scanf("%d",&a);
    fibo(a);
    
}
```
## SAMPLE OUTPUT:
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/4358f62f-5300-4fad-ba20-8fabe716fe2b)
## OUTPUT :
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/3f70f77a-7646-4533-9f94-51523fdfcece)


## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-14-ADDITION SERIES GENERATOR

### AIM:
To create a program that generates an addition series starting from 100 up to 500, with each term incremented by the input value `a`.

### ALGORITHM:
1. Begin the program.
2. Declare a function `sub()` to generate the addition series.
   - Declare variables `a` and `c` of type int.
   - Prompt the user to input the value of `a`.
   - Read the input value for `a` using `scanf()` function.
   - Use a for loop with loop variable `i` initialized to 100, terminating condition `i <= 500`, and incrementing `i` by 100 in each iteration:
     - Calculate the value of `c` as the sum of `i` and `a`.
     - Print the value of `c`.
3. In the `main()` function:
   - Call the `sub()` function to generate the addition series.
4. End the program.
## PROGRAM :
```
#include<stdio.h>
void sub()
{
    int a,c;
    scanf("%d",&a);
    for(int i=100;i<=500;i+=100)
    {
      c=i+a;
      printf("%d  ",c);
    }
    
    
}
int main()
{
    sub();
}


```
## SAMPLE OUTPUT:
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/f721e3e2-683d-48d0-aa20-0b50fa67775e)

## OUTPUT :
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/3605613a-bf1b-4dcc-9a24-6d606f43ec00)


## RESULT:
Thus the required program is written and executed successfully.

## EXPERIMENT-15-PALINDROME NUMBER CHECKER

### AIM:
To create a program that checks whether the given number is a palindrome or not.

### ALGORITHM:
1. Begin the program.
2. Declare variables `n` and `a` of type int to store the input number and its copy.
3. Prompt the user to input a number.
4. Read the input value for `n` using `scanf()` function.
5. Assign the value of `n` to `a`.
6. Declare variables `r` and `digit` of type int to store the reversed number and individual digits.
7. Use a do-while loop to reverse the number `n`:
   - Inside the loop:
     - Extract the last digit of `n` using the modulo operator and store it in `digit`.
     - Update the value of `r` by multiplying it by 10 and adding the extracted digit.
     - Update the value of `n` by removing the last digit.
   - Continue the loop until `n` becomes 0.
8. Check if the original number `a` is equal to the reversed number `r`:
   - If true, print "Palindrome Number".
   - If false, print "Not a Palindrome Number".
9. End the program.
## PROGRAM :
```
#include<stdio.h>
int main(){
    int n,a;
    scanf("%d",&n);
    a=n;
    int r=0,digit;
    do{
        digit=n%10;
    r=r*10+digit;
    n/=10;
    }
    while(n>0);
    if(a==r){
        printf("Palindrome Number");
    }
    else{
        printf("Not a Palindrome Number");
    }
    
}
```
## SAMPLE OUTPUT:
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/6feb0507-d320-4892-a048-65a058285898)

## OUTPUT :
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/b56334c1-e681-43d1-9bf7-d454c7313034)



## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-16-PATTERN PRINTER

### AIM:
To create a program that prints a pattern.

### ALGORITHM:
1. Begin the program.
2. Use nested for loops to generate the desired pattern:
   - Outer loop (`i` loop) iterates from 1 to 5.
   - Inner loop (`j` loop) prints numbers from 1 to the current value of `i`.
   - Second inner loop (`k` loop) prints the character 'A' in a decreasing manner from 4 to `j-1`.
   - Third inner loop (`l` loop) prints numbers from `i` to 1 in a decreasing manner.
   - Print a newline character after each iteration of the outer loop.
3. End the program.
## PROGRAM :
```
#include<stdio.h>
int main()
{
    int i,j,k,l;
    for(i=1;i<=5;i++)
    {
        for(j=1;j<=i;j++)
        {
            printf("%d",j);
    
        }
        for(k=4;k>=j-1;k--)
        {
            printf("A");
        }
        for(l=i;l>=1;l--)
        {
            printf("%d",l);
    
    
        }
    printf("\n");
    }
}
```
## SAMPLE OUTPUT:
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/f6269ad3-192b-419d-8d97-43f2c6b8fc86)

## OUTPUT :
![image](https://github.com/EzhilsreeJ/module-2/assets/144870412/f80d36b0-2e9f-47fd-bf33-c0ddf7c2655c)

## RESULT:
Thus the required program is written and executed successfully.


