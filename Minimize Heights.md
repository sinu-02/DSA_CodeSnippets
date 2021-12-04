[Question Link](https://practice.geeksforgeeks.org/problems/minimize-the-heights3351/1)

int main()

{

    int n,k;
    
    cin>>n>>k;
    
    int a[n];
    
    for(int i=0;i<n;i++)
    
    {
    
    	cin>>a[i];
      
   	}
  
	 sort(a, a+n);
   int ans = a[n-1] - a[0];
   
   int smallest = a[0]+k;
  
   int largest = a[n-1]-k;
  
   int minimum, maximum;
        
   for(int i = 0; i < n; i++){
  
     minimum = min(smallest, a[i+1]-k);
     
     maximum = max(largest, a[i]+k);
     
     if(minimum < 0)
        continue;
        
     ans = min(ans, maximum - minimum);
     
     }
     
   cout<<ans;
  
	 return 0;
}
