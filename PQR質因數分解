//
//  main.c
//  4.
//
//  Created by 孫渝鈞 on 2020/10/15.
//  Copyright © 2020 孫渝鈞. All rights reserved.
//


#include <stdio.h>
#include<math.h>
//submitted
int main()
{
    long a[3],n;
    int ct=0;
    int record[1000]= {0};
    int counter=0;
    int z=0;


    scanf("%ld%ld%ld",&a[0],&a[1],&a[2]);

    for(int j=0; j<3; j++)
    {
        n=a[j];
        ct=0;

        while (n%2 == 0)
        {
            //printf("%d ", 2);
            n = n/2;
            ct++;
        }
        if(ct>0)
        {
            if(z>0)
                {
                    z=z+1;
                    record[z]=2;
                    z+=1;
                    record[z]=ct;
                    counter+=1;
                }
                else
                {
                    record[z]=2;
                    z+=1;
                    record[z]=ct;
                    counter+=1;
                }
        }

        for (int i = 3; i <= sqrt(n); i = i+1)
        {
            ct=0;

            while (n%i == 0)
            {

                n = n/i;
                ++ct;

            }
            if(ct>0)
            {

                if(z>0)
                {
                    z=z+1;
                    record[z]=i;
                    z+=1;
                    record[z]=ct;
                    counter+=1;
                }
                else
                {
                    record[z]=i;
                    z+=1;
                    record[z]=ct;
                    counter+=1;
                }

            }

        }


        if (n > 2)
        {
            if(z>0)
            {
                z=z+1;
                record[z]=n;
                z+=1;
                record[z]=1;
                counter+=1;
            }
            else
            {
                record[z]=n;
                z+=1;
                record[z]=1;
                counter+=1;
            }
        }
    }



    int ra[100]={0};
    int rb[100]={0};


    for(int i=0; i<counter; i++)
    {
        ra[i]=record[i*2];
        rb[i]=record[i*2+1];
    }

    int count;
    int f[100]={0};
    int freq[100]={-1};
    for(int i=0; i<counter; i++)
    {
        count = rb[i];
        for(int j=i+1; j<counter; j++)
        {

            if(ra[i]==ra[j])  //
            {
                count=count+rb[j];


                rb[j] = 0;
            }
        }


        if(count>0)
        {
            f[i]=ra[i];
            freq[i] = count;
        }
    }

    for(int i=0; i<counter; i++)
    {
      if(freq[i]!=0)
        printf("%d %d\n",f[i],freq[i]);

    }
    return 0;
}
