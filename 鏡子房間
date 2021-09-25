//
//  main.c
//  6.
//
//  Created by 孫渝鈞 on 2020/12/2.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//
int up[100],down[100],left[100],right[100],mirror[100][100];
int n,m;
int num[400]={0};
void track(int x,int y,int r,int dir){
    if(dir==1){
        if(num[r]==0){
            x=x-1;
            if(x>=0){
                if(mirror[x][y]==0){
                    track(x,y,r,1);
                }
                else if(mirror[x][y]==1){
                    track(x,y,r,2);
                }
            }
            else if(x<0){
                num[r]=up[y];
            }

        }
    }
    else if(dir==2){
        if(num[r]==0){
            y=y+1;
            if(y<m){
                if(mirror[x][y]==0){
                    track(x,y,r,2);
                }
                else if(mirror[x][y]==1){
                    track(x,y,r,1);
                }
            }
            else if(y==m){
                num[r]=right[x];
            }

        }

    }
    else if(dir==3){
        if(num[r]==0){
            x=x+1;
            if(x<n){
                if(mirror[x][y]==0){
                    track(x,y,r,3);
                }
                else if(mirror[x][y]==1){
                    track(x,y,r,4);
                }
            }
            else if(x==n){
                num[r]=down[y];
            }

        }

    }
    else if(dir==4){
       if(num[r]==0){
            y=y-1;
            if(y>=0){
                if(mirror[x][y]==0){
                    track(x,y,r,4);
                }
                else if(mirror[x][y]==1){
                    track(x,y,r,3);
                }
            }
            else if(y<0){
                num[r]=left[x];
            }

        }

    }




}
void ex(int x,int y,int r){
    int i,v;
    if(r<m){
       if(mirror[x][y]==0){
            track(x,y,r,1);
       }
       else{
            track(x,y,r,2);
       }

    }
    else if(r>=m&&r<m+n){
        if(mirror[x][y]==0){
            track(x,y,r,4);
        }
        else{
            track(x,y,r,3);
        }
    }
    else if(r>=m+n&&r<m+n+m){
        if(mirror[x][y]==0){
            track(x,y,r,3);
        }
        else{
            track(x,y,r,4);
        }
    }
    else if(r>=m+n+m&&r<2*(m+n)){
        if(mirror[x][y]==0){
            track(x,y,r,2);
        }
        else{
            track(x,y,r,1);
        }
    }



}
#include<stdio.h>
int main(){


    scanf("%d %d",&m,&n);

    int i,count=0;
    for(i=0;i<m;i++){
        down[i]=count;
        count++;
    }
    for(i=n-1;i>=0;i--){
        right[i]=count;
        count++;
    }
    for(i=m-1;i>=0;i--){
        up[i]=count;
        count++;
    }
    for(i=0;i<n;i++){
        left[i]=count;
        count++;
    }
    int v;
    for(i=0;i<n;){
        for(v=0;v<m;v++){
            scanf("%d",&mirror[i][v]);
        }
        if(v==m){
            v=0;
            i=i+1;
        }
    }
    int r=0;

    for(i=0;i<m;i++){
        ex(n-1,i,r++);
    }
    for(i=n-1;i>=0;i--){
        ex(i,m-1,r++);
    }
    for(i=m-1;i>=0;i--){
        ex(0,i,r++);
    }
    for(i=0;i<n;i++){
        ex(i,0,r++);
    }

    for(i=0;i<2*(n+m);i++){
        printf("%d\n",num[i]);
    }


}
