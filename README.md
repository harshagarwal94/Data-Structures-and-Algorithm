# Data-Structures-and-Algorithm
Provides Information regarding DSA (Data Structures and Algorithm) at VIT (Vellore Institute of Technology)

#### Course Instructor - Dr. Praveen Lalwani 

# Overview



(1)


Introduction to Algorithm and Data Structures

Algorithm: Introduction - Algorithm Design – Complexity- Asymptotic notations. Data Structures: Introduction-
Classification of Data structure -Abstract Data Type (ADT).



(2)


Sorting and Searching

Brute force approach: General method -Sorting ( bubble, selection, insertion) – Searching (Sequential/Linear)
Divide and Conquer approach: General method - Sorting ( merge, quick) – Searching (Binary Search).



(3)


List, Statck and Queue ADT

Linked List: Array Vs Linked List - Singly Linked List, Doubly Linked Lists – Circular Linked Lists-implementation -
application.
Stack and Queue: Introduction – implementation (static and dynamic) – application – Circular queues-application.



(4) 


Tree ADT and Hashing

Search Tree – AVL Tree – Red block Tree – Splay Tree – B Tree. - Hashing: Introduction – Hash Function-Methods-
Collision Resolution.



(5)


Graph ADT

Graph: Introduction – Representations – Traversals - Topological Sorting – Connected and Bi-Connected Components –
Articulation Point - Shortest-path algorithms (Dijkstra’s and Floyd’s algorithms) - Minimum spanning tree (Prim’s and
Kruskal’s algorithms).


## How to calculate the time complexity

```
Step1: Initially u have to calculate the number of executable steps.
Step2: Represents in the form notations(Big O, Omega, Theta).

................................................................
Q.1 for(i=0;i<n;i++)
{
 printf("Today i am in bad mood");//executalbe statement
}
.................................................
Ans
step1. printf("Today i am in bad mood");//executable statement
Step 2. 0 to n-1= n // no. of times
Step 3. O(n)// Big O(n)
..................................................
Q.2 for(i=0;i<n/2;i++)
{
 printf("Today i am in good mood");
}
......................................................
Ans step1. printf("Today i am in good mood");// executable statement
Step 2. 0 to n/2-1= n/2 // no. of times
Step 3. O(n/2)= O(n) //neglecting the constant terms
.....................................................
Q.3 for(i=0;i<n;i++)// n
     for(j=0;j<n;j++)// n
       {
      printf("Today i am in bad mood"); //executable statement
       }
...................................................
Ans 
 Step1: printf("Today i am in bad mood");
 Step2: i=0, j=n;
        i=1, j=n;
        i=2, j=n;


       i=n-1, j=n;
summation of all j's= (n+n+n+n.........+n)=n * (1+1+1+1.....)= n*n=n^2= O(n^2);
.................................................................................
Q.4 for(i=n;i>=1;n=n/2)
      {
       statement;
     }
ans: step1: statement;
     step2: i=n;
            i=n/2;
            i=n/4;
	    i=n/8;
   .........i=n/n=1
     generalized way: n/(2^k)=1
                    n=(2^k)
      Apply log both the side
             then log(n)=====complexity=O(log n)
...........................................................................
Q.5 for(i=n;i>=1;n=n/3)
      {
       statement;
     }
ans: step1: statement;
     step2: i=n;
            i=n/3;
            i=n/9;
	    i=n/27;
   .........i=n/n=1
     generalized way: n/(3^k)=1
                    n=(3^k)
      Apply log both the side
             then log(n)=====complexity=O(log n)
    log base is 3
........................................................................
Q.5 for(i=n;i>=1;n=n/5)
      {
       statement;
     }
ans: step1: statement;
     step2: i=n;
            i=n/5;
            i=n/25;
	    i=n/125;
   .........i=n/n=1
     generalized way: n/(5^k)=1
                    n=(5^k)
      Apply log both the side
             then log(n)=====complexity=O(log n)
    log base is 5
    
@.6 for(i=0;i<n;i++)//n
for(j=0;j<n;j++)//n
 {
   statement;

 }
solution n*n;

@.7 for(i=0;i<n;i++)//n 
    for(j=n;j>=1;j=j/2)// logn
    {
     statement;

    }
 ans : n*logn
@.8 for(i=0;i<n;i++)n
    for(j=0;j<n;j++)n
    for(k=0;k<n;k++)n
      {
       statement;
     }
ans;n^3

@.9 for(i=0;i<n;i++)//n
    for(j=0;j<n;j++)//n
    for(k=n;k>=1;k=k/2) logn
     {
      statement;
     }

ans : (n^2)(log n)

Big O
.................................
Suppose if the complexity is n:
 1. O(n), O(n^2), O(n^3)//// Big O
...................................
2. Theta(n), Theta(n), Theta(n)
...................................
3. Omega(n), Omega(log n), Omega(log log n)









```
### Sorting and Searching

```
Unit-2: Sorting and Searching
Sorting: Arrange of data in order (Asc or Desc).
Searching: Finding element in a available data.
..........................................
Sorting: 
Part 1:
1. Bubble Sort
2. Insertion Sort
3. Selection Sort
Part 2:
1. Quick Sort
2. Merge Sort
................................................
Bubble Sort:
Objective: Arrangment of numbers
first iteration 
suppose array size is n: 0 to n-1;
place largest number at the end (n-1);
second iteration
array size is n: 0 to n-2;
place secon largest number at the (n-2);
third iteration
arrayt size is n: 0 to n-3;
third largest element searched and placed at (n-3)index
............................................................
#include<stdio.h>
void main()
{
int a[]={24, 16, 96, 1,14};
int n=sizeof(a)/sizeof(a[0]);
BubbleSort(a, n);
}
void BubbleSort(int a[], int n)
{
int i,j;
for(i=0;i<n-1;i++)// number of iteration
for(j=0;j<n-1-i, j++)
    {
       if(a[j]>a[j+1]){swap(&a[j], &a[j+1]);}
  }

}
void swap(int *a, int *b)
{
temp=*a; *a=*b; *b=temp;
}

```




















#Disclaimer 

* For Educational Purpose only 
* Open Source Licensed
