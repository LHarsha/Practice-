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