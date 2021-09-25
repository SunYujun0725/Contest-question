//
//  main.c
//  5.
//
//  Created by 孫渝鈞 on 2020/12/2.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//

#include<stdio.h>

int n,k;
int map[110][110];
int sub_map[110][110];
int keep[110][110];
int dirs[8][2]={{1,0},{-1,0},{0,1},{0,-1},{1,1},{1,-1},{-1,1},{-1,-1}};

void game(){
    int live=0;
    for(int i=1;i<=n;i++){
        live=0;
        for(int j=1;j<=n;j++){
            live=0;
            if(map[i][j]==1){
                for(int k=0;k<8;k++){
                    if(map[i+dirs[k][0]][j+dirs[k][1]]==1){
                        live++;
                    }
                }
                if(live<2) sub_map[i][j]=0;
                if(live==2||live==3) sub_map[i][j]=1;
                if(live>3) sub_map[i][j]=0;
            }
            else if(map[i][j]==0){
                for(int k=0;k<8;k++){
                    if(map[i+dirs[k][0]][j+dirs[k][1]]==1){
                        live++;
                    }
                }
                if(live==3) sub_map[i][j]=1;
            }
            live=0;
        }
    }
    for(int i=1;i<=n;i++){
        for(int j=1;j<=n;j++){
            map[i][j]=sub_map[i][j];
            if(map[i][j]==1){
                keep[i][j]++;
            }
        }
    }
}
int main(){
    scanf("%d%d",&n,&k);
    for(int i=0;i<=n+1;i++){
        for(int j=0;j<=n+1;j++){
            if(i==0||i==n+1||j==0||j==n+1){
                map[i][j]=5;
                sub_map[i][j]=9;
            }
            else{
                scanf("%d",&map[i][j]);
            }
        }
    }
    if(k>0){
        for(int i=1;i<=n;i++){
            for(int j=1;j<=n;j++){
                if(map[i][j]==1){
                    keep[i][j]++;
                }
            }
        }
        while(k--){
            game();
        }
    }
    else{
        for(int i=1;i<=n;i++){
            for(int j=1;j<=n;j++){
                if(map[i][j]==1){
                    keep[i][j]++;
                }
            }
        }
    }
    int max=0;
    int x=0,y=0;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=n;j++){
            if(keep[i][j]>=max){
                max=keep[i][j];
                x=i;
                y=j;
            }
            printf("%d ",map[i][j]);
        }
        printf("\n");
    }
    printf("%d %d\n",x,y);
    return 0;
}
