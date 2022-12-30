# ALGORITHM-BRUTE-FORCE
#include <stdio.h>
#include<string.h>

void search(char str[],char pat[])
{
    int count=0, n=strlen(str),m=strlen(pat);
    int i,j;
    for(i=0;i<n-2;i++)
    {
        for(j=0;j<m;j++)
        {
            if(pat[j]==str[i+j])
            {
                count++;
            }
            else
            {
                break;
            }
        }
        if(count==m)
        {
            printf("%d\t",i);
        }
        count=0;
    }
}
void main()
{
    char str[] ="bcdabcbadabcda";
    char pat[] ="abc";
    search(str,pat);
}

