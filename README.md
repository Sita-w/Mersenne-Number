#include<stdio.h>
#include<math.h>
double a(int n);
int main()
{
	int count=0,i,j,n,s,flag;
	scanf("%d",&n);
	if(n==1)printf("None");	
	else
	{
		for(i=2;i<=n;i++)
		{
			s=a(i)-1;
			flag=1;
			for(j=2;j<=sqrt(s);j++)
			{
				if(s%j==0)
				{
					flag=0;
					break;
				}
			}
			if(flag)
			{
				printf("%d\n",s);
				count++;
			}
		}
		if(count==0)printf("None");	
		return 0;
    }
}
double a(int n)
{
	int i;
	double s=1;
	for(i=1;i<=n;i++)
	{
		s*=2;
	}
	return s;
}
