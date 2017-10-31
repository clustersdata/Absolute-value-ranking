# Absolute-value-ranking

Absolute value ranking

Problem Description

输入n(n<=100)个整数，按照绝对值从大到小排序后输出。题目保证对于每一个测试实例，所有的数的绝对值都不相等。

 
Input

输入数据有多组，每组占一行，每行的第一个数字为n,接着是n个整数，n=0表示输入数据的结束，不做处理。  


Output

对于每个测试实例，输出排序后的结果，两个数之间用一个空格隔开。每个测试实例占一行。

 
Sample Input

3 3 -4 2

4 0 1 2 -3

0

 
Sample Output

-4 3 2

-3 2 1 0



解答：

#include<stdio.h>

main()

{

    int n,m,a[100],b[100],c,d,e,f,i,j,k;
    
    while(scanf("%d",&n)!=EOF&&n!=0)
    
    {
    
        for(i=0;i<n;i++)
        
        scanf("%d",&a[i]);
        
         f=0;
         
        for(j=0;j<n;j++)
        
        {
        
            c=0;
            
            for(i=0;i<n;i++)
            
            {
            
                if(a[i]<0)
                
                 m=-a[i];
                 
                 else m=a[i];
                 
                 if(c<=m)
                 
                 {
                 
                 c=m;
                 
                 b[j]=a[i];
                 
                 k=i;
                 
                 }
                 

            }
            
            a[k]=0;
            
            if(f)
            
            printf(" ");
            
            printf("%d",b[j]);
            
            f=f+1;
            
        }
        
        printf("\n");
        
    }
    
}

