# C
#include <stdio.h>
int main()
{int y=0,m=0,d=0,i=0,j=0,a=0,sum1=0,sum2=0,sum=0,b[13],k=0,c=0;
scanf("%d",&a);
if(a<1)printf("error.\n");
else{
for(c=1;c<=a;c++)
{scanf("%d %d %d",&y,&m,&d);
b[0]=0;
sum1=(y-1990)*365;
for(j=1990;j<y;j++)
{
if(j%100!=0&&j%4==0||j%400==0)
sum2=sum2+1;
}
if(y%4==0&&y%100!=0||y%400==0)
b[2]=29;
else b[2]=28;
for(i=1;i<13;i++)
 if(i==1||i==3||i==5||i==7||i==8||i==10||i==12)
    b[i]=31;
else {if(i==4||i==6||i==9||i==11)
      b[i]=30;}
for(i=1;i<m;i++) 
{sum2=sum2+b[i];
	 }   
 sum=sum1+sum2+d-2;  
switch(sum%5)
{
	case 0:printf("He was basking on %d.%d.%d\n",y,m,d);
	break;
	case 1:printf("He was fishing on %d.%d.%d\n",y,m,d);
	break;
	case 2:printf("He was fishing on %d.%d.%d\n",y,m,d);
	break;
	case 3:printf("He was fishing on %d.%d.%d\n",y,m,d);
	break;
	case 4:printf("He was basking on %d.%d.%d\n",y,m,d);
	break;
}
}
}
return 0;
}
