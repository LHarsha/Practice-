# Practice-
C language 

program to print average of three numbers:

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

program to print fail or pass (below 30 marks = fail) using if and else:

#include <stdio.h>

int main()
{

    int a;
    printf("enter marks \n");
    scanf("%d", &a);
   
   if (a >= 30) 
    {
      printf("pass");
    } 
   
   else 
    {
      printf("fail"); 
    }
    
    return 0;
}