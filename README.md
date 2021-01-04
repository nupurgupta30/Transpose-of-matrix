# Transpose-of-matrix
#include<stdio.h>
void display(int x[][10],int xr,int xc)
{for(int i=0;i<xr;i++)
{for(int j=0;j<xc;j++)
{if(x[i][j]<10)
printf("0");
printf("%d ",x[i][j]);
}
printf("\n");
}
}
int main()
{int a[10][10],b[10][10],r,c;
printf("Enter No of Rows    :");
scanf("%d",&r);
printf("Enter No of Columns :");
scanf("%d",&c);
printf("Enter Matrix :\n");
for(int i=0;i<r;i++)
{for(int j=0;j<c;j++)
{printf(" A%d%d :",i+1,j+1);
scanf("%d",&a[i][j]);
}
}
printf("Before Transpose :\n");
display(a,r,c);
for(int i=0;i<r;i++)
{for(int j=0;j<c;j++)
b[j][i]=a[i][j];
}
printf("After Transpose :\n");
display(b,c,r);
return 0;
}
