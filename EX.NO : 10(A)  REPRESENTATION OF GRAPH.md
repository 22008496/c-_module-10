
# EX.NO : 10(A)  REPRESENTATION OF GRAPH 
 
# PROGRAM STATEMENT: 
 
To write A C++ Program to represent the Adjacency Matrix. 

 ![image](https://github.com/user-attachments/assets/0400eb48-50b5-4024-8329-4c389731172b)

 
# ALGORITHM:   
 
1. Start the program. 
2. Define a graph matrix: Create a 2D array vertArr to represent the graph, initialized to 0. 
3. Add edges: The add_edge function sets the corresponding matrix entries to 1 for both directions (undirected graph). 
4. Input edges: Use a loop to take 6 pairs of inputs representing edges. 
5. Display adjacency matrix: The displayMatrix function prints the adjacency matrix, showing connections between vertices. 
6. End the program. 
 
# PROGRAM:  
```
#include<iostream>
using namespace std;
int vertArr[20][20];
int count = 0;
void displayMatrix(int v)
{
   int i, j;
   for(i = 0; i < v; i++) 
   {
      for(j = 0; j < v; j++) 
      {
         cout << vertArr[i][j] << " ";
      }
      cout << endl;
   }
}
void add_edge(int u, int v) 
{
   vertArr[u][v] = 1;
   vertArr[v][u] = 1;
}
int main() 
{
   int v = 6,a,b;    //there are 6 vertices in the graph
   for(int i=0;i<6;i++)
   {
       cin>>a>>b;
       add_edge(a, b);
   }
   displayMatrix(v);
   return 0;
}
```
# output:

![image](https://github.com/user-attachments/assets/25a1e31c-5b03-4583-b0fb-7ea15958af63)

# RESULT: 
 
Thus, the C++ program to represent the Adjacency Matrix is created successfully. 

