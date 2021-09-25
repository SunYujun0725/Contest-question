//
//  main.c
//  7.
//
//  Created by 孫渝鈞 on 2020/10/14.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//

#include <stdio.h>
#include <math.h>
int f(int f,int e){  //算最大公因數
    while(f%e!=0){
        int t=f%e;
        f=e;
        e=t;
    }
    return e;
    
}

int main()
{   int n;
    scanf("%d",&n);
    int a[n];
    int b[n];
    int c[n];
    int d[n];
    for(int i=0;i<n;i++){
        scanf("%d %d %d %d",&a[i],&b[i],&c[i],&d[i]); //輸入
    }
    int m;
    int e;
    int g;
    int h;
    int l;
    int count;
    for(int i=0;i<n;i++){
        if(a[i]==c[i]){
            count=0;
            if(b[i]<=d[i]){
                b[i]+=1;
                count++;
                
            }
            printf("%d\n",count);
        }
        
        
      else if(a[i]<=c[i]&&b[i]<=d[i]) {
            count=0;
        m=b[i]-d[i];
        e=a[i]-c[i];
        g=f(m,e);
          
        h=m/g; //分數最簡化
        l=e/g; //分數最簡化
          
       
         while(a[i]<=c[i]&&b[i]<=d[i]){
            a[i]+=l;
            b[i]+=h;
            count++;
            
        }
         printf("%d\n",count);
       
      }
     else if(a[i]<=c[i]&&b[i]>=d[i]){
          count=0;
                 m=b[i]-d[i];
                 e=c[i]-a[i];
                 g=f(m,e);
                   
                 h=m/g; //分數最簡化
                 l=e/g; //分數最簡化
                   
                
                  while(a[i]<=c[i]&&b[i]>=d[i]){
                     a[i]-=l;
                     b[i]+=h;
                     count++;
                     
                 }
                printf("%d\n",count-1);
            }
     else if(a[i]>=c[i]&&b[i]<=d[i]){
                        count=0;
                         m=d[i]-b[i];
                         e=a[i]-c[i];
                         g=f(m,e);
                           
                         h=m/g; //分數最簡化
                         l=e/g; //分數最簡化
                           
                        
                          while(a[i]<=c[i]&&b[i]>=d[i]){
                             a[i]-=l;
                             b[i]+=h;
                             count++;
                             
                         }
                        printf("%d\n",count-1);
         
    }
        
     else{
           count=0;
           m=b[i]-d[i];
           e=a[i]-c[i];
            g=f(m,e);
                                  
            h=m/g; //分數最簡化
            l=e/g; //分數最簡化
                                  
                               
            while(a[i]<=c[i]&&b[i]>=d[i]){
                    a[i]+=l;
                    b[i]+=h;
                     count++;
                                
          }
        printf("%d\n",count-1);
                
         
     }
        
        
    }
    return 0;
}
