# Prime-Encoder-c++-code

**Problem Statement:**

Given an integer array input[] and another integer input2, primeEncoder function returns an integer array by following these two steps:

Step 1: Find the nth prime number, where n=input2.

Step 2: To each element of the input array, add the prime number that is computed in
the above step. Assumptions:

1) All the values of input1 array is > =1 and<=1000.

2) Value of input2 is >=1 and <=100,

Note:
1) Prime number series is 2,3,5,7,11,13...etc 2).0 and 1 are neither prime nor composite.

Function Prototype: int[] primeEncoder(int input1[], int input2)

**0INPUT:**
input1[]=[1,2,3]
input2=2
**OUTPUT:**[4,5,6]




**CODE:**



```
//code
#include <bits/stdc++.h>

using namespace std;
int
main ()
{
    int n;
     cin>>n;
     int a[n];
     for(int i=0;i<n;i++)
     {
         cin>>a[i];
     }
     
  int rangenumber, c = 0, num = 2, i, letest = 0;
  //cout<<"Enter Nth Number:";
  cin>>rangenumber;
std::vector<int>v ;
  while (c != rangenumber)
    {
      int count = 0;

      for (i = 2; i <= sqrt (num); i++)
    {
   if (num % i == 0)
     {
       count++;
       break;
     }
 }
      if (count == 0)
 {
   c++;
   letest = num;
 }
      num = num + 1;
    }
 // cout<<rangenumber<<"th prime number is "<<letest;
 for(int i=0;i<n;i++)
 {
     a[i]+=letest;
     v.push_back(a[i]);
 }for(auto i:v)
 {
     cout<<i<<" ";
 }
  return 0;
}
