//
//  main.c
//  5.
//
//  Created by 孫渝鈞 on 2020/10/15.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//

#include <stdio.h>

  int Switch(int n){
    if (n >= 10) {
        int dev = n / 10;
        int mod = n % 10;
        return Switch(dev) * 2 + mod;
    }
    else {
        return n;
    }
}
int main()
{
    int n;
    scanf("%d",&n);
    printf("%d\n",Switch(n));


    return 0;
}
