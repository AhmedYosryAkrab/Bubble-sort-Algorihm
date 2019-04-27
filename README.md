
#include <iostream>
#include <stdio.h>
using namespace std;
 
  
void swap(int *xp, int *yp) 
{ 
    int temp = *xp; 
    *xp = *yp; 
    *yp = temp; 
} 
  
// A function to implement bubble sort 
void bubbleSort(int arr[], int n) 
{ 
   int i, j; 
   for (i = 0; i < n-1; i++)  {
        
  
       // Last i elements are already in place    
       for (j = 0; j < n-i-1; j++)  {
	   
           if (arr[j] > arr[j+1]) {
		   
              swap(&arr[j], &arr[j+1]);
			  } 
          }
      }
} 
  
/* Function to print an array */
void SortedArray(int arr[], int size) 
{ 
    int i; 
    for (i=0; i < size; i++){
	 
        cout<<arr[i]; 
    cout<<(" "); 
}
} 
  
// testing the program 
int main() 
{ 
int x;
cout<<"Welcome Begin your bubble sort operation:- "<<endl;
cout<<endl;
cout<<"determine size of array: "<<endl;
cin>>x;
     
    int arr[x] = {}; 
    cout<<"inserts your numbers in the determined array: "<<endl;
    for(int i=0;i<x;i++){
    	cin>>arr[i];
    }
   
    int n = sizeof(arr)/sizeof(arr[0]); 
    bubbleSort(arr, n); 
    cout<<("Sorted array: \n"); 
    SortedArray(arr, n); 
    return 0; 
} 
