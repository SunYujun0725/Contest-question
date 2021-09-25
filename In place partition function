//
//  main.c
//  4.
//
//  Created by 孫渝鈞 on 2020/12/2.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//
/* probID:MT2B-4-InPlacePartition */
int In_Place_Partition(int A[],int left,int right,int key){
    int k=A[key];
    int temp=A[left];
    A[left]=A[key];
    A[key]=temp;
    int ptrl=left+1,ptrr=right;
    while(ptrl<=ptrr){
        int l=0,r=0;
        if(A[ptrl]<k){
            ptrl++;
        }
        else{
            l=1;
        }
        if(A[ptrr]>=k){
            ptrr--;
        }
        else{
            r=1;
        }
        if(l==1&&r==1){
            int t=A[ptrl];
            A[ptrl]=A[ptrr];
            A[ptrr]=t;
            l++;
            r--;
        }
    }
    
    int t=A[ptrl-1];
    A[ptrl-1]=A[left];
    A[left]=t;
    
    return ptrl-1;
    
}
/*#include<stdio.h>
int In_Place_Partition(int [],int,int,int);
int A[10000000],n;
int left,right,key;
int main(){
    scanf("%d",&n);
    for(int i=0;i<n;i++){
        scanf("%d",&A[i]);
    }
    scanf("%d %d %d",&left,&right,&key);
    key=In_Place_Partition(A,left,right,key);
    for(int i=0;i<n;i++){
        printf("%d",A[i]);
    }
    printf("\n%d\n",key);
    return 0;
}*/
