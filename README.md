# 100A
#include<bits/stdc++.h>
using namespace std;

long long len(long long i,long long &h)
{

	if(i==1)
	{
		h++;
	return 1;
   }

	if(i%2==0)
	{
		h++;
	  len(i/2,h);
    }
	else
	{
		h++;
		len(i*3+1,h);
	 } 
	 
  return h;
}		

int main()
{
	long long i,j,u=0,l,c=0,d=0,w,t;
	
	
	while(scanf("%lld %lld",&i,&j)!=EOF)
	{
		u=-10;
	
	
    w=min(i,j);
	t=max(i,j);
	
	for(l=w;l<=t;l++)
	{
		
		
	  u=max(u,len(l,c));
	  
	   c=0;
		
		
	}
	
	
	cout<<i<<" "<<j<<" "<<u<<endl;
	
}
}
