//
//  main.c
//  8.
//
//  Created by 孫渝鈞 on 2020/10/14.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//

#include <stdio.h>

int main()
{
    for(int i=0;i<1000;i++){
    
    int a,b,c;
     if(i<10){
        a=0;
        b=0;
        c=i;
        if(i==c){
            printf("%d\n",i);
        }
     }
     else if(i<100){
         a=0;
         b=(i-i%10)/10;
         c=i%10;
         if(i==b*b+c*c){
             printf("%d\n",i);
         }
     }
     else{
         
         c=i%10;
         a=i/100;
         b=(i-100*a-c)/10;
         if(i==a*a*a+b*b*b+c*c*c){
             printf("%d\n",i);
         }
     }
        
        
    }
   
    return 0;
}
