//
//  main.c
//  9.
//
//  Created by 孫渝鈞 on 2020/10/15.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//

#include <stdio.h>

int gcd(int a,int b) {return(b == 0)? a:gcd(b, a % b);}
int lcm(int a, int b) {return a * b / gcd(a, b);}

int main(void) {
    int n,i1=0,j1=0;
    scanf("%d",&n);
    int min=n*2;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=n;j++){
            if(lcm(i,j)==n){
                if(i+j<min){
                    min=i+j;
                    i1= i;
                    j1= j;
                }
                
            }
        }
    }
    printf("%d",i1);
    printf(" ");
    printf("%d",j1);

    return 0;
}

