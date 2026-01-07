# Array
---

- Implementation
```c++
#include<bits/stdc++.h>
using namespace std;

void Input(int arr[] , int size)
{
    cout << "Enter Array Elements" << endl;
    for(int i=0 ; i<size ; i++)
    {
        cin >> arr[i];
    }
}

void Print(int arr[] , int size)
{
    cout << "Array Elements" << endl;
    for(int i=0 ; i<size ; i++)
    {
        cout << arr[i] << " ";
    }
}

int LinearSearch(int arr[] , int size , int key)
{
    for(int i=0 ; i<size ; i++)
    {
        if(arr[i] == key)
        {
            return i;
        }
    }
    return -1;
}

void Reverse(int arr[] , int size)
{
    int start = 0;
    int end = size - 1;
    while(start <= end)
    {
        swap(arr[start++] , arr[end--]);
    }
}

int Sum(int arr[] , int size)
{
    int sum = 0;
    for(int i=0 ; i<size ; i++)
    {
        sum = sum + arr[i];
    }
    return sum;
}

int Min(int arr[] , int size)
{
    int mini = INT_MAX;
    for(int i=0 ; i<size ; i++)
    {
        mini = min(arr[i] , mini);
    }
    return mini;
}

int Max(int arr[] , int size)
{
    int maxi = INT_MIN;
    for(int i=0 ; i<size ; i++)
    {
        maxi = max(arr[i] , maxi);
    }
    return maxi;
}

int main()
{
    int size;
    cout << "Enter size : ";
    cin >> size;
    int arr[size];
    Input(arr , size); // 1 2 3 4 5
    Print(arr , size);
    cout << "Key Index : " << LinearSearch(arr , size , 4) << endl; // Key Index : 3
    cout << "Sum : " << Sum(arr , size) << endl; // Sum : 15
    cout << "Minimum : " << Min(arr , size) << endl; // Minimum : 1
    cout << "Maximum : " << Max(arr , size) << endl; // Maximum : 5
    Reverse(arr , size); // 5 4 3 2 1
    Print(arr , size);
    return 0;
}
```

---
