//
//  main.c
//  8.
//
//  Created by 孫渝鈞 on 2020/10/16.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//



#include <stdio.h>

int main()
{
    int n,m;
    scanf("%d",&n);
    int a[n+1];
    for(int i=0;i<=n;i++){
        scanf("%d",&a[i]);
    }
    scanf("%d",&m);
    int b[m+1];
    for(int i=0;i<=m;i++){
        scanf("%d",&b[i]);
        
    }
    
    int c[n+m+1];
    for(int i=0;i<=m+n+1;i++)
        c[i]=0;
    
    
    for(int i=0;i<=n;i++){
        
        for(int j=0;j<=m;j++){
            c[i+j]+=a[i]*b[j];
            
        }
    }
    
    for(int i=0;i<=n+m;i++){
        
        printf("%d",c[i]);
        printf(" ");
        
    }
    
    
    return 0;
    }
