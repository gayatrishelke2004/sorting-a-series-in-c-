#include <bits/stdc++.h> 
using namespace std;

void selection(int arr[], int n)
{
    int i, j, min;
    for(i=0;i<n-1;i++)
    {
        min=i;
        for (j=i; j<n;j++) 
        { 
            if(arr[j]<arr[min])
            {
                min=j;
            }
        }
        if (min!=i){
            swap(arr[min],arr[i]);
        }
    }
}

void print (int arr[], int size)
{
    int i;
    for(i=0;i<size;i++){
        cout << arr[i] << " ";
        cout << endl;
    }
   
}

int main(){
    int arr[]={64,35,53,10,2};
    int n= sizeof(arr)/sizeof(arr[0]);
    selection(arr,n);
    cout << "sorted array :\n";
    print(arr,n);
    return 0;
    
    
}
    
