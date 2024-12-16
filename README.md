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

PROGRAM to check prime number or not:

#include<stdio.h>

int main()
{
    int n, i;
    printf("enter number : \n");
    scanf("%d", &n);
     
    if (n <= 1)
    {
        printf("not prime number");
        return 0;
    }
    for(i=2; i*i <= n; i++)
    {
       if(n%i == 0)
       {
        printf("prime number\n");
        return 0;
       }
    }   
       
        printf("not prime number\n");
     
   return 0;
}

PROGRAM to print factorial of number using recursions:

#include <stdio.h>

int Ft (int n);

int Ft (int n)
{
  
  if (n<0)
  {
      printf ("enter positive number \n");
      return -1;
  }
  
  if (n==0)
  {
    return 1;  
  }
  
  int f = Ft (n-1);
  int ft = f*n;
  return ft;
}


int main()
{
    int n;
    printf("enter number \n");
    scanf("%d", &n);
    
    printf ("factorial is %d", Ft(n));
    
    return 0;
}

PROGRAM to print bigger number using pointers:

#include <stdio.h>

int main()
{
    int a, b;
    int *ptr1, *ptr2;

    // Prompt and input first number
    printf("Enter the first number: ");
    scanf("%d", &a);

    // Prompt and input second number
    printf("Enter the second number: ");
    scanf("%d", &b);

    // Assign addresses to pointers
    ptr1 = &a;
    ptr2 = &b;

    // Compare and print the bigger number using pointers
    if (*ptr2 > *ptr1) {
        printf("The bigger number is: %d\n", *ptr2);
    } else {
        printf("The bigger number is: %d\n", *ptr1);
    }

    return 0;
}

PROGRAM of a function to count the number of odd numbers in an array:

#include <stdio.h>

int countOdd (int odd[], int n);

int main()
{
    int n, i;
    
    printf ("enter no. of elements \n");
    scanf ("%d", &n);
    
    int odd[n];
    
    printf ("enter %d numbers : \n", n);
    for (i=0; i<n; i++) 
    {
    scanf("%d", &odd[i]);
    }
    
    int count = countOdd(odd, n);
    
    printf ("count of odd numbers = %d", count);
    
    return 0;
}

int countOdd (int odd[], int n) 
{
    int count = 0;
  for (int i = 0; i < n; i++)
  {
  if (odd[i]%2 != 0) 
   {
     count++; 
   } 
 
  } return count;
}

PROGRAM of function to reverse the given array:

#include <stdio.h>

void reverseArr(int arr[], int n);

int main()
{   
    int i, n, swap;
    
    printf("enter no. of digits \n");
    scanf("%d", &n);
    
    int arr[n];
    
    printf("enter %d digits \n", n);
    for(i=0; i<n; i++){
        scanf("%d", &arr[i]);
    }
   
   reverseArr(arr, n);
   
   printf("digits in reverse order: \n");
   for(i=0; i<n; i++){
       printf ("%d \n", arr[i]);
   }
    return 0;
}

void reverseArr(int arr[], int n) 
{
    int temp;
    
    for (int i=0; i<=n/2; i++){
        int temp = arr[i];
        arr[i] = arr[n-1-i];
        arr[n-1-i] =temp;
        
    }
    
}
