//
//  main.c
//  3.
//
//  Created by 孫渝鈞 on 2020/12/2.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//

#include <stdio.h>
#define MAX_N 100
#define MAX_M 100
int n,m;
char A[MAX_N][MAX_M];
int B[MAX_N][MAX_M];
int visited[MAX_N][MAX_M];
void Explore(int x,int y);
int dirs[4][2]={{1,0},{-1,0},{0,1},{0,-1}};
int dirs1[4][2]={{0,0},{0,0},{1,0},{-1,0}}; //'|'
int dirs2[4][2]={{0,0},{0,0},{0,1},{0,-1}}; //'-'
void Explore(int x,int y)
{
    visited[x][y]=1;
    
    if(A[x][y]=='+'){
       for(int i=0;i<=3;i++){
            if(A[x+dirs[i][0]][y+dirs[i][1]]=='+'&&visited[x+dirs[i][0]][y+dirs[i][1]]==0){
                if(x+dirs[i][0]>=0&&x+dirs[i][0]<n&&y+dirs[i][1]>=0&&y+dirs[i][1]<m){
                    if(B[x][y]>=B[x+1][y]){
                        Explore(x+1,y);
                    }
                    if(B[x][y]>=B[x-1][y]){
                        Explore(x-1,y);
                    }
                    if(B[x][y]>=B[x][y+1]){
                        Explore(x,y+1);
                    }
                    if(B[x][y]>=B[x][y-1]){
                        Explore(x,y-1);
                    }
                }
            }
            else if(A[x+dirs1[i][0]][y+dirs1[i][1]]=='|'&&visited[x+dirs1[i][0]][y+dirs1[i][1]]==0){
                if(x+dirs1[i][0]>=0&&x+dirs1[i][0]<n&&y+dirs1[i][1]>=0&&y+dirs1[i][1]<m){
                    if(B[x][y]>=B[x+1][y]){
                        Explore(x+1,y);
                    }
                    if(B[x][y]>=B[x-1][y]){
                        Explore(x-1,y);
                    }
                }
            }
            else if(A[x+dirs2[i][0]][y+dirs2[i][1]]=='-'&&visited[x+dirs2[i][0]][y+dirs2[i][1]]==0){
                if(x+dirs2[i][0]>=0&&x+dirs2[i][0]<n&&y+dirs2[i][1]>=0&&y+dirs2[i][1]<m){
                     if(B[x][y]>=B[x][y+1]){
                        Explore(x,y+1);
                    }
                    if(B[x][y]>=B[x][y-1]){
                        Explore(x,y-1);
                    }
                }
            }
            
        }
        
    }
    else if(A[x][y]=='|'){
        for(int i=0;i<=3;i++){
            if(A[x+dirs1[i][0]][y+dirs1[i][1]]=='+'&&visited[x+dirs1[i][0]][y+dirs1[i][1]]==0){
                if(x+dirs1[i][0]>=0&&x+dirs1[i][0]<n&&y+dirs1[i][1]>=0&&y+dirs1[i][1]<m){
                    if(B[x][y]>=B[x+1][y]){
                        Explore(x+1,y);
                    }
                    if(B[x][y]>=B[x-1][y]){
                        Explore(x-1,y);
                    }
                }
            }
            else if(A[x+dirs1[i][0]][y+dirs1[i][1]]=='|'&&visited[x+dirs1[i][0]][y+dirs1[i][1]]==0){
                if(x+dirs1[i][0]>=0&&x+dirs1[i][0]<n&&y+dirs1[i][1]>=0&&y+dirs1[i][1]<m){
                    if(B[x][y]>=B[x+1][y]){
                        Explore(x+1,y);
                    }
                    if(B[x][y]>=B[x-1][y]){
                        Explore(x-1,y);
                    }
                }
            }
        }
    }
    else if(A[x][y]=='-'){
        
    for(int i=0;i<=3;i++){
        if(A[x+dirs2[i][0]][y+dirs2[i][1]]=='+'&&visited[x+dirs2[i][0]][y+dirs2[i][1]]==0){
            if(x+dirs2[i][0]>=0&&x+dirs2[i][0]<n&&y+dirs2[i][1]>=0&&y+dirs2[i][1]<m){
                if(B[x][y]>=B[x][y+1]){
                    Explore(x,y+1);
                }
                if(B[x][y]>=B[x][y-1]){
                    Explore(x,y-1);
                }
            }
        }
       else if(A[x+dirs2[i][0]][y+dirs2[i][1]]=='-'&&visited[x+dirs2[i][0]][y+dirs2[i][1]]==0){
            if(x+dirs2[i][0]>=0&&x+dirs2[i][0]<n&&y+dirs2[i][1]>=0&&y+dirs2[i][1]<m){
                 if(B[x][y]>=B[x][y+1]){
                    Explore(x,y+1);
                }
                if(B[x][y]>=B[x][y-1]){
                    Explore(x,y-1);
                }
            }
        }
        
    }
    }
    
    
    
    
    
}
int main()
{
    scanf("%d %d",&n,&m);
    for(int i=0;i<n;i++){
        char tmp[1000000];
        scanf("%s",tmp);
        for(int j=0;j<m;j++){
            A[i][j]=tmp[j];
            visited[i][j]=0;
        }
    }
    for(int i=0;i<n;i++){
        for(int j=0;j<m;j++){
            scanf("%d",&B[i][j]);
        }
    }
    
    int x,y;
    scanf("%d %d",&x,&y);
    int endx,endy;
    scanf("%d %d",&endx,&endy);
    Explore(x,y);
    if(visited[endx][endy]==1){
        printf("Yes\n");
    }
    else{
        printf("No\n");
    }
    return 0;
}
