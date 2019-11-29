**PRANVIR SINGH**
**1915059**
**CSE-A2**
```c
#include<stdio.h>
void main()
{
	puts("Budding Engineers ! Welcome to Guru Nanak Dev Engineering College");
	
}
```
```c
#include<stdio.h>
void main()
{
	puts("Guru Nanak Nagar Block-B ,VPO GILL,(Ludhiana)");
}
#include<stdio.h>
int main()
{
	int a,b,c;
	printf("Enter the values of a and b :- \n");
	scanf("%d%d",&a,&b);
	c=a+b;
	printf("The sum of two no. is :- %d\n",c);
	return 0;

}
```
```c
#include <stdio.h>
int main()
{
        int m, n, c, d, first[10][10], second[10][10], sum[10][10];
        printf("Enter the number of rows and columns of matrix\n");
        scanf("%d%d", &m, &n);
        printf("Enter the elements of first matrix\n");
        for (c = 0; c < m; c++)
        for (d = 0; d < n; d++)
             scanf("%d", &first[c][d]);

        printf("Enter the elements of second matrix\n");

        for (c = 0; c < m; c++)
                for (d = 0 ; d < n; d++)
                        scanf("%d", &second[c][d]);
        printf("Sum of entered matrices:-\n");

        for (c = 0; c < m; c++)
        {
                for (d = 0 ; d < n; d++) 
                {
                        sum[c][d] = first[c][d] + second[c][d];
                        printf("%d\t", sum[c][d]);
                }
                printf("\n");
        }
       return 0;
}
```
```c
#include<stdio.h>
int main()
{
	int arr[10];
	int *p;
	int i;
	p=&arr[0];
	printf("enter array elements :- \n");
	for(i=0;i<10;i++)
	{
		printf("Enter the elements %02d :- \n");
		scanf("%d,p+i");
	}
	printf("entered array elements are :- \n");
	printf("\naddress\tvalue\n");
	for(i=0;i<10;i++)
	{
		printf("%08x \t %03d\n",(p+i),*(p+i));
	}
	return 0;

}
```
```c
#include <stdio.h>
int main()
{
  int array[100], n, c, d, swap;
  printf("Enter number of elements\n");
  scanf("%d", &n);
  printf("Enter %d integers\n", n);
  for (c = 0; c < n; c++)
    scanf("%d", &array[c]);
  for (c = 0 ; c < n - 1; c++)
  {
    for (d = 0 ; d < n - c - 1; d++)
    {
      if (array[d] > array[d+1])
      {
        swap       = array[d];
        array[d]   = array[d+1];
        array[d+1] = swap;
      }
    }
  }
  printf("Sorted list in ascending order:\n");
  for (c = 0; c < n; c++)
     printf("%d\n", array[c]);
  return 0;
}
```
```c
#include <stdio.h>
int main()
{
    char operator;
    double firstNumber,secondNumber;
    printf("Enter an operator (+, -, *,): ");
    scanf("%c", &operator);
    printf("Enter two operands: ");
    scanf("%lf %lf",&firstNumber, &secondNumber);
    switch(operator)
    {
        case '+':
            printf("%.1lf + %.1lf = %.1lf",firstNumber, secondNumber, firstNumber + secondNumber);
            break;
        case '-':
            printf("%.1lf - %.1lf = %.1lf",firstNumber, secondNumber, firstNumber - secondNumber);
            break;
        case '*':
            printf("%.1lf * %.1lf = %.1lf",firstNumber, secondNumber, firstNumber * secondNumber);
            break;
        case '/':
            printf("%.1lf / %.1lf = %.1lf",firstNumber, secondNumber, firstNumber / secondNumber);
            break;
        default:
            printf("Error! operator is not correct");
    }
    return 0;
}
```
```c
#include <stdio.h>
void swap(int*, int*);
int main()
{
   int x, y;
   printf("Enter the value of x and y\n");
   scanf("%d%d",&x,&y);
   printf("Before Swapping\nx = %d\ny = %d\n", x, y);
   swap(&x, &y);
   printf("After Swapping\nx = %d\ny = %d\n", x, y);
   return 0;
}
void swap(int *a, int *b)
{
   int temp;
   temp = *b;
   *b = *a;
   *a = temp;
}
```
```c
#include<stdio.h>

void swap(int,int);        

void main( )
{
    int n1,n2;
    printf("Enter the two numbers to be swapped\n");
    scanf("%d%d",&n1,&n2);
    printf("\nThe values of n1 and n2 in the main function before calling the swap function are n1=%d n2=%d\n",n1,n2);
    swap(n1,n2);
    printf("\nThe values of n1 and n2 in the main function after calling the swap function are n1=%d n2=%d\n",n1,n2);}

void swap(int n1,int n2)
{ 
    int temp;
    temp=n1;
    n1=n2;
    n2=temp;
    printf("\nThe values of n1 and n2 in the swap function after swapping are n1=%d n2=%d\n",n1,n2);
}
```
```c
#include <stdio.h>
int main()
{
        int num;
        printf("Enter an integer number: ");
        scanf("%d",&num);
        if(num%2==0)
                printf("%d is an EVEN number.\n",num);
        else
                printf("%d is an ODD number.\n",num);
        return 0;
}
```
```c
#include <stdio.h>
int main()
{
    int i, n, t1 = 0, t2 = 1, nextTerm;
    printf("Enter the number of terms: ");
    scanf("%d", &n);
    printf("Fibonacci Series: ");
    for (i = 1; i <= n; ++i)
    {
        printf("%d, ", t1);
        nextTerm = t1 + t2;
        t1 = t2;
        t2 = nextTerm;
    }
    return 0;
}
```
```c
#include <stdio.h>
int main()
{
    int n, i;
    int factorial = 1;
    printf("Enter an integer: ");
    scanf("%d",&n);
    if (n < 0)
        printf("Error! Factorial of a negative number doesn't exist.");
    else
    {
        for(i=1; i<=n; ++i)
        {
            factorial *= i;
        }
        printf("Factorial of %d = %d\n", n, factorial);
    }
    return 0;
}
```
```c
#include <stdio.h>
int multiplyNumbers(int n);
int main()
{
    int n;
    printf("Enter a positive integer: ");
    scanf("%d", &n);
    printf("Factorial of %d = %d\n", n, multiplyNumbers(n));
    return 0;
}
int multiplyNumbers(int n)
{
    if (n >= 1)
        return n*multiplyNumbers(n-1);
    else
        return 1;
}
```
```c
#include <stdio.h>
int main()
{
    float celsius, fahrenheit;
    printf("Please Enter the temperature in Fahrenheit: \n");
    scanf("%f", &fahrenheit);
    celsius = (fahrenheit - 32) * 5 / 9;
    printf("\n %.2f Fahrenheit = %.2f Celsius", fahrenheit, celsius);
    return 0;
}
```
```c
#include<stdio.h>
float square ( float x );
int main()
{
    float m, n ;
    printf ( "\nEnter some number for finding square \n");
    scanf ( "%f", &m ) ;
    // function call
    n = square ( m ) ;
    printf ( "\nSquare of the given number %f is %f\n",m,n );
}

float square ( float x )
{
    float p ;
    p = x * x ;
    return ( p ) ;
}
```
```c
#include <stdio.h>
int main()
{
    int i, space, rows, k=0;
    printf("Enter number of rows: ");
    scanf("%d",&rows);
    for(i=1; i<=rows; ++i, k=0)
    {
        for(space=1; space<=rows-i; ++space)
        {
            printf("  ");
        }
        while(k != 2*i-1)
        {
            printf("* ");
            ++k;
        }
        printf("\n");
    }
    return 0;
}
```
```c
#include<stdio.h>
int main()
{
	int a[5],max,i;
	printf("Enter the values of the arrays to find the maximum :- \n");
	for(i=0;i<5;i++)
	{
		scanf("%d",&a[i]);
	}
	max=a[0];
	for(i=1;i<5;i++)
	{
		if(max<a[i])
			max=a[i];
	}
	printf("max no. = :- %d\n",max);
	return 0;
}
```
```c
#include <stdio.h>
int main()
{
  int m, n, p, q, c, d, k, sum = 0;
  int first[10][10], second[10][10], multiply[10][10];
  printf("Enter number of rows and columns of first matrix\n");
  scanf("%d%d", &m, &n);
  printf("Enter elements of first matrix\n");
  for (c = 0; c < m; c++)
    for (d = 0; d < n; d++)
      scanf("%d", &first[c][d]);
  printf("Enter number of rows and columns of second matrix\n");
  scanf("%d%d", &p, &q);
  if (n != p)
    printf("The matrices can't be multiplied with each other.\n");
  else
  {
    printf("Enter elements of second matrix\n");
    for (c = 0; c < p; c++)
      for (d = 0; d < q; d++)
        scanf("%d", &second[c][d]);
    for (c = 0; c < m; c++)
    {
      for (d = 0; d < q; d++)
      {
        for (k = 0; k < p; k++)
        {
          sum = sum + first[c][k]*second[k][d];
        }
        multiply[c][d] = sum;
        sum = 0;
      }
    }
    printf("Product of the matrices:\n");
  for (c = 0; c < m; c++)
  {
      for (d = 0; d < q; d++)
        printf("%d\t", multiply[c][d]);
      printf("\n");
    }
  }
  return 0;
}
```
```c
#include<stdio.h>  
int main()    
{    
    int n,r,sum=0,temp;    
    printf("enter the number=");    
    scanf("%d",&n);    
    temp=n;    
    while(n>0)    
    {    
    	r=n%10;    
        sum=(sum*10)+r;    
        n=n/10;    
    }    
    if(temp==sum)    
    	printf("palindrome number \n");    
    else    
        printf("not palindrome\n");   
    return 0;  
} 
```
```c
#include<stdio.h>
int main()
{
        int n;
        int *p;
        p=&n;
        n=100;
        printf("using variable :- \n");
        printf("value of n:%d\n adress of n:%d\n",n,&n);
        printf("using pointer variable :- \n");
        printf("value of n:%d \n adress of n:%d\n",*p,p);
        return 0;
}
```
```c
#include <stdio.h>
int main()
{
    int n, i, flag = 0;
    printf("Enter a positive integer: ");
    scanf("%d", &n);
    for(i = 2; i <= n/2; ++i)
    {
        if(n%i == 0)
        {
            flag = 1;
            break;
        }
    }
    if (n == 1)
    {
	    printf("1 is neither a prime nor a composite number.");
    }
    else
    {
        if (flag == 0)
       	    printf("%d is a prime number.", n);
        else
            printf("%d is not a prime number.", n);
    }
    return 0;
}
```
```c
#include<stdio.h>
int factorial(int);
int main()
{
        int i;
        printf("Enter any value :- ");
        scanf("%d",&i);
        printf("Factorial is :- %d ",factorial(i));
        return 0;
}
int factorial(int i)
{
        if(i==1)
                return 1;
        return i*factorial(i-1);
}
```
```c
#include<stdio.h>
int main()
{
        int a,n,r;
        printf("Enter a value to find its reverse :- \n");
        scanf("%d",&n);
        while(n>=1)
        {
                a=n%10;
                r=r*10+a;
                n=n/10;
        }
        printf("the reversed value is :- %d\n",r);
        return 0;
}
```
```c
#include<stdio.h>
int main()
   {
   int a[30], ele, num, i;
   printf("\nEnter no of elements :");
   scanf("%d", &num);
   printf("\nEnter the values :");
   for (i = 0; i < num; i++)
   {
      scanf("%d", &a[i]);
   }
   printf("\nEnter the elements to be searched :");
   scanf("%d", &ele);
   i = 0;
   while (i < num && ele != a[i])
   {
      i++;
   }
   if (i < num) {
      printf("Number found at the location = %d\n", i + 1);
   }
   else {
      printf("Number not found");
   }
   return (0);
}
```
```c
#include<stdio.h>
int main()
{
    struct book
    {
        char name;
        float price;
        int pages;
    };
    struct book b1, b2, b3;
    printf("\nEnter names, prices & no. of pages of 3 books\n");
    scanf("%c %f %d", &b1.name, &b1.price, &b1.pages);
    scanf("%c %f %d", &b2.name, &b2.price, &b2.pages);
    scanf("%c %f %d", &b3.name, &b3.price, &b3.pages);
    printf("\n\nAnd this is what you entered");
    printf("\n%c %f %d", b1.name, b1.price, b1.pages);
    printf("\n%c %f %d", b2.name, b2.price, b2.pages);
    printf("\n%c %f %d", b3.name, b3.price, b3.pages);
}
```
```c
#include <stdio.h>
int main()
{
   int m, n, c, d, first[10][10], second[10][10], difference[10][10];
   printf("Enter the number of rows and columns of matrix\n");
   scanf("%d%d", &m, &n);
   printf("Enter the elements of first matrix\n");
   for (c = 0; c < m; c++)
     for (d = 0 ; d < n; d++)
       scanf("%d", &first[c][d]);
   printf("Enter the elements of second matrix\n");
   for (c = 0; c < m; c++)
     for (d = 0; d < n; d++)
         scanf("%d", &second[c][d]);
   printf("Difference of entered matrices:-\n");
   for (c = 0; c < m; c++)
   {
     for (d = 0; d < n; d++)
     {
       difference[c][d] = first[c][d] - second[c][d];
       printf("%d\t",difference[c][d]);
     }
     printf("\n");
   }
   return 0;
}
```
```c
#include <stdio.h>
int main()
{
    int week;
    printf("Enter week number(1-7): ");
    scanf("%d", &week);
    switch(week)
    {
        case 1:
            printf("Monday");
            break;
        case 2:
            printf("Tuesday");
            break;
        case 3:
            printf("Wednesday");
            break;
        case 4:
            printf("Thursday");
            break;
        case 5:
            printf("Friday");
            break;
        case 6:
            printf("Saturday");
            break;
        case 7:
            printf("Sunday");
            break;
        default:
            printf("Invalid input! Please enter week number between 1-7.\n");
    }

    return 0;
}
```
```c
#include<stdio.h>
int main()
{
    int num, i, tab;
    printf("Enter the number: ");
    scanf("%d", &num);
    printf("\nTable of %d is:\n", num);
    for(i=1; i<=10; i++)
    {
        tab = num*i;
        printf("%d * %2d = %2d\n", num, i, tab);
    }
    return 0;
}
```
```c
 #include <stdio.h>
    int main()
    {
        int a[10][10], transpose[10][10], r, c, i, j;
        printf("Enter rows and columns of matrix: ");
        scanf("%d %d", &r, &c);
        // Storing elements of the matrix
        printf("\nEnter elements of matrix:\n");
        for(i=0; i<r; ++i)
            for(j=0; j<c; ++j)
            {   
                printf("Enter element a%d%d: ",i+1, j+1);
                scanf("%d", &a[i][j]);
            }
        // Displaying the matrix a[][] */
        printf("\nEntered Matrix: \n");
        for(i=0; i<r; ++i)
            for(j=0; j<c; ++j)
            {   
                printf("%d  ", a[i][j]);
                if (j == c-1)
                    printf("\n\n");
            }
        // Finding the transpose of matrix a
        for(i=0; i<r; ++i)
            for(j=0; j<c; ++j)
            {
                transpose[j][i] = a[i][j];
            }
        // Displaying the transpose of matrix a
	printf("\nTranspose of Matrix:\n");
        for(i=0; i<c; ++i)
            for(j=0; j<r; ++j)
            {
                printf("%d  ",transpose[i][j]);
                if(j==r-1)
                     printf("\n\n");
            }
        return 0;
    }
```
