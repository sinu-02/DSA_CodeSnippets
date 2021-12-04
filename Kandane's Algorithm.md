[Question Link](https://practice.geeksforgeeks.org/problems/kadanes-algorithm-1587115620/1)

#include<bits/stdc++.h>

using namespace std;

int main()
{

    int n;
    
    cin>>n;
    
    int a[n];
    
    for(int i=0;i<n;i++)
    {
    
    	cin>>a[i];
      
	  }
	int sum=0,maxs=a[i];
  
	for(int i=0;i<n;i++)
	{
		int x=a[i];
    
		sum=max(x,sum+x);
    
		maxs=max(maxs,sum);
    
	}
	cout<<maxs;
  
	return 0;
  
}
