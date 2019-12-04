#include <iostream>
using namespace std;
int f(int n)
{
    if((n&(n-1))==0)
    return 1;
    else
    return 0;
}
void f1(int n)
{
    int i;
    for( i=n-1;i>0;i--)
    {
      if(i%2!=0)
       continue;
       int x=f(i);
       if(x==1)
       break;
    }
    cout<<i<<" ";
}
void f2(int n)
{
    int i;
    for(i=n+1;;i++)
    {
        if(i%2!=0)
        continue;
        int x=f(i);
        if(x==1)
        break;
    }
    cout<<i<<endl;
}
int main() 
{
	int t;
	cin>>t;
	while(t-->0)
	{
	       int n;
	      cin>>n;
	        f1(n);
	        f2(n);
	}
}
