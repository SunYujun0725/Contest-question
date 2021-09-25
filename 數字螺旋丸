//
//  main.cpp
//  2-3.
//
//  Created by 孫渝鈞 on 2020/12/2.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//

#include <iostream>
#include <iomanip>
using namespace std;
 
int main()
{

    int M,N;//矩陣行數
    scanf("%d %d",&M,&N);//矩陣列數

    int matrix[M][N];
    int row = 0;
    int col =   0;
    int start = 0; //起始值



    int m =M;
    int n = N;
    //可以畫N/2個圈
    for (int count = 0; count < N / 2; count++)
    {
        for (; col < n - 1; col++) //a排賦值
        {
            matrix[row][col] = start++;
        }
        for (; row < m - 1; row++) //b排賦值
        {
            matrix[row][col] = start++;
        }
        for (col = n - 1; col > count; col--) //c排賦值
        {
            matrix[row][col] = start++;
        }
        for (row = m- 1; row > count; row--) //d排賦值
        {
            matrix[row][col] = start++;
        }
        //進入下一圈
        m--;
        n--;
        row++;
        start--; //這裡是因為在換圈的時候會多加1
    }
    if (N % 2 != 0) //如果size為奇數則最後中間那一個數遍歷不到，這裡補上
    {
        int  z = M - 2 *row;
        for(int i=0  ;  i< z   ;++i)
        matrix[row++][col + 1] =++ start ;
    }

    //輸出陣列
    for (int i = 0; i < M; i++)
    {
        for (int j = 0; j < N; j++)
        {
            cout << matrix[i][j]<<" ";//設定輸出寬度為3
        }
        cout << endl;
    }


    return 0;
}
