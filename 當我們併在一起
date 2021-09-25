//
//  main.cpp
//  7-2
//
//  Created by 孫渝鈞 on 2020/11/27.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//
/* probID:MT2A-7-Merge-Sorted-Arrays */
/*#include <iostream>
using namespace std;

int N[35];
int arrays[35][10000000];
int *ptr_arrays[35];
int merged[30000000];
void merge(int n,int N[],int *arrays[],int merged[]);
int main(){
    int i,j,n,sum=0;
    scanf("%d",&n);
    for(i=0;i<n;i++){
        scanf("%d",&N[i]);
        sum+=N[i];
    }
    for(i=0;i<n;i++){
        for(j=0;j<N[i];j++){
            scanf("%d",&arrays[i][j]);
        }
    }
    for(i=0;i<n;i++){
        ptr_arrays[i]=arrays[i];
    }
    merge(n,N,ptr_arrays,merged);
    for(i=0;i<sum;i++){
        printf("%d ",merged[i]);
    }
    printf("\n");
    return 0;
}*/


void merge(int n, int N[], int *array[], int merged[]){
 int p[n], i, j, curse=0, sum = 0;
 for(i=0;i<=n;i++) p[i] = 0; //init
 for(i=0;i<n;i++) sum += N[i];
 for(j=0;j<sum;j++){
        int smalliest = 1e9;
        for(i=0;i<n;i++){
            if(p[i]>=N[i]) continue;
            if(array[i][p[i]]<smalliest){
                smalliest = array[i][p[i]];
                curse = i;
            }
        }
        merged[j] = smalliest;
        p[curse]++;
    }

}
