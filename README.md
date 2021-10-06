# Number_C_Program
C program to print all perfect numbers between 1 to n


**C program to print all perfect numbers between 1 to n**
#include <stdio.h>
int main()
{
    int i, j, n, sum;
    printf("Enter upper limit: ");
    scanf("%d", &n);
    printf("All Perfect numbers between 1 to %d :\n", n);
    for(i=1; i<=n; i++)
    {
        sum = 0;
        for(j=1; j<i; j++)
        {
            if(i % j == 0)
            {
                sum += j;
            }
        }
        if(sum == i)
        {
            printf("%d, ", i);
        }
    }
    return 0;
}
/*
OUTPUT :
Enter upper limit: 500
All Perfect numbers between 1 to 500 :
6, 28, 496,
*/

**2. Find total occurrence of each digits(0-9) using functions.**
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int a[10];
    int n, num, i, temp=0;
    printf("Enter the n : ");
    scanf("%d", &n);
    for(i=0; i<10; i++)
    {
        a[i] = 0;
    }
    num=n;
    while(num>0)
    {
        temp = num%10;
        num = num/10;
        a[temp]++;
    }
    for(i=0; i<10; i++)
    {
        if(a[i]>0)
            printf("%d present %d times\n",i,a[i]);
    }
    return 0;
}
/*
OUTPUT :
Enter the number : 112233980
0 present 1 times
1 present 2 times
2 present 2 times
3 present 2 times
8 present 1 times
9 present 1 times
*/

**3.Convert number to words**
