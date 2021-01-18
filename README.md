#include<iostream>
//#include<stdio.h>
using namespace std;
void printLeaders(int arr[], int size) 
{ 

    for (int i = 0; i < size; i++) 

    { 

        int j; 

        for (j = i+1; j < size; j++) 

        { 

            if (arr[i] < arr[j]) 

                break; 

        }     

        if (j == size) // the loop didn't break 
            cout<<arr[i] <<" "; 

  } 
} 


int main() 
{ 

    int arr[10];
    int i,p;
    cout<<"Enter the number of elements in the array(<10)";
	cin>>p;
	cout<<"Enter the array";
	for(i=0;i<p;i++)
	{
		cin>>arr[i];
	}
    //int n = sizeof(arr)/sizeof(arr[0]); 

    printLeaders(arr, p); 

    return 0; 
}


------------------------------------------------------------------------------------------------



#include <iostream>
using namespace std; 
int main()
{
    int i, j, n;
    cout<<"enter the mumer of rows:";
    cin >> n;
    // upper half of the pattern
    for(i = 0; i < n; i++)
    {
        for(j = 0; j < (2 * n); j++)
        {
            if(i >= j) // upper left triangle
                cout << "*";
            else
                cout << " ";
            if(i >= (2 * n - 1) - j)  // upper right triangle
                cout << "*";
            else
                cout << " ";
        }
        cout << "\n";
    }
    // bottom half of the pattern
    for(i = 0; i < n; i++)
    {
        for(j = 0; j < (2 * n); j++)
        {
            if(i + j <= n - 1)  // bottom left triangle
                cout << "*";
            else
                cout << " ";
            if((i + n) <= j)  // bottom right triangle
                cout << "*";
            else
                cout << " ";
        }
        cout << "\n";
    }
    return 0;
}


