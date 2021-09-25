//
//  main.c
//  Bonus 1
//
//  Created by 孫渝鈞 on 2020/10/23.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//

#include <stdio.h>
int getDays(int,int);
int main()
{
    int Y,M,W;
    scanf("%d %d %d",&Y,&M,&W);//2020 10 4
    //
    if(Y<1000 || Y>3000 || M<1 || M>12 || W<1 || W>7){
        printf("invalid\n");
      
    }

    else{
    printf(" Su Mo Tu We Th Fr Sa\n");
    printf("=====================\n");
    int days= getDays(Y,M);
    for(int n=1-W;n<=days;n++){
        if(n>0) printf("%3d",n);
        else printf("   ");
        if((n+W)%7==0) printf("\n");
    }
    printf("\n");
    printf("=====================\n");
    return 0;
    
    
    
    
    
}
}
int getDays(int Y,int M){
    //檢查是否為潤年
    int days=0;
    switch(M){
        case 1:
        case 3:
        case 5:
        case 7:
        case 8:
        case 10:
        case 12:
            days=31;
            break;
        case 4:
        case 6:
        case 9:
        case 11:
            days=30;
            break;
        case 2:
            //檢查是否為潤年
               if(Y%4==0){
                   days=29;
             }
               else{days=28;}
            break;
    }
    return days;
}

