# Practice-
C language 

PROGRAM to print average of three numbers:

#include <stdio.h>

int main()
{  
   
    int a, b, c;
    printf("enter a number \n");
    scanf("%d", &a);
    
    printf("enter 2nd number \n");
    scanf("%d", &b);
    
    printf("enter 3rd number \n");
    scanf("%d", &c);
    
    int sum = a + b + c;
    
    printf("average of 3 numbers is %d", sum/3);
    return 0;
}

PROGRAM to print fail or pass (below 30 marks = fail) using if and else:

#include <stdio.h>

int main()
{
    int a;
    printf("enter marks (1-100) \n");
    scanf("%d", &a);
   
   if (a >= 30 && a == 100) 
    {
      printf("pass");
    } 
   else if (a < 30 && a == 0)
    {
      printf("fail"); 
    }
   else 
    {
      printf("wrong marks");  
    }
    return 0;
}

PROGRAM to check whether a three digit number is Armstrong number or not (no loops used):

#include <stdio.h>

int main()
{
    int a;
    printf("enter 3 digit number \n");
    scanf("%d", &a);
    
    int b = a%10;
    int c = a/10;
    int d = c%10;
    int e = a/100;
    int f = e%10;
    
    int g = b*b*b;
    int h = d*d*d;
    int i = f*f*f;
    
    if (g+h+i == a)
     {
       printf("it is a amstrong number");
     }
    else
     {
       printf("not an amstrong number");    
     }
    return 0;
}

PROGRAM to print sum of n-natural numbers:

#include <stdio.h>

int main()
{
    int n, i;
    printf("enter number \n");
    scanf("%d", &n);
    
    int sum = 0;
    
    for(i=1; i<=n; i++)
    {
      sum += i;
    }
    
    printf("%d \n", sum);

    
    
    return 0;
}

PROGRAM to print table of n-number:

#include <stdio.h>

int main()
{
    int n, i;
    printf("enter number \n");
    scanf("%d", &n);
    
    
   for (i=1; i<=10; i++) 
   {
  
      printf("%d \n", i*n);   
   }
    
    return 0;
}

PROGRAM to print n-number of odd/even numbers:

#include <stdio.h>

int main()
{
    int n, i;
    
    printf("enter number: ");
    scanf("%d", &n);
    
    for(i=1; i<=n; i++)
    {
        if(i%2 == 0) // change it to "if(i%2 != 0)" for n-even nuumbers
        {
            continue;
        }
        printf("%d \n", i);
    }
    return 0;
}

PROGRAM to print factorial of a number:

#include <stdio.h>

int main()
{
    int n, i;
    long long factorial = 1;  // Use a larger data type to handle large results
    
    printf("Enter a number: ");
    scanf("%d", &n);
    
    if (n < 0)
        printf("Factorial of negative numbers is undefined.\n");
    else
    {
        for(i = 1; i <= n; i++)
        {
            factorial *= i;  // Multiply factorial by the current value of i
        }
    
        printf("Factorial of %d is: %lld\n", n, factorial);  // Use %lld for long long type (till 65!)
    }
    
    return 0;
}

PROGRAM to print n-rows of pyramid:

#include <stdio.h>

int main()
{   
    int i, j, n;
    
    printf("How many rows of pyramid?: \n");
    scanf("%d", &n);
    
    for (i = 1; i <= n; i++)
    {
        for (j = 1; j <= 2 * n - 1; j++)
        {
            if (j >= (n - i + 1) && j <= (n + i - 1))
            {
                printf("*");
            }    
            else 
            {    
                printf(" ");
            }
        }
        printf("\n");
    }
    return 0;
}