# 2-pointer-approach


#include<bits/stdc++.h>
using namespace std;

bool three_sum(int arr[],int n,int k)
{
    sort(arr,arr+n);
    for(int i=0;i<n;i++)
    {
        int low =i+1;
        int high= n-1;
        while(low<high)
        {
            int sum = arr[i] + low + high;
            if( k == sum)
            {
                return true;
            }
            else if( k > sum)
            {
                low = low +1;
            }
            else{
                high = high-1;
            }
        }
    }
    return false;
}


int main()
{
    int n;
    int count=0;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
    }
    int k;
    cin>>k;
    
    cout<<three_sum(arr,n,k);
    
    
}
