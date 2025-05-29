
# EX.NO : 10(C)  DEPTH FIRST SEARCH-DFS 
 
# PROGRAM STATEMENT: 
 
To write A C++ Program to implementation DFS using Vector STL 
 
# ALGORITHM:   
 
1. Start the program. 
2. Define graph structure: Create a 2D vector g to store the adjacency list and a vector v to track visited nodes. 
3. Edge addition: Define the addEdge function to add an undirected edge between nodes by updating the adjacency list. 
4. DFS visit: Implement the dfsVisit function to visit nodes recursively. Mark the node as visited and explore its neighbors. 
5. DFS traversal: Implement the dfs function, iterating over all nodes and calling dfsVisit for unvisited nodes to ensure the entire graph is explored. 
6. End the program: Input the number of nodes and edges from the user, then read and store the edges. Perform DFS and output the nodes in the order they are visited. 
7. End the program. 
 
# PROGRAM:
```
#include <bits/stdc++.h>
using namespace std;
void addEdge(vector<int> adj[], int u, int v)
{
    adj[u].push_back(v);
}
void DFS(vector<int> adj[], int v, vector<bool> &vis)
{
    vis[v] = true;
    cout << v << " ";
    //for(int i=0;i<adj[v].size() ; i++)
    for (auto i : adj[v])
    {
        if (vis[i] == false)
            DFS(adj, i, vis);
    }
}
int main()
{ 
    int n,a,b;
    cin>>n;
    
    vector<int> adj[n];
    vector<bool> visited(n, false);
    
    for(int i=0;i<n;i++)
    {
        cin>>a>>b;    
        addEdge(adj, a, b);
    }
    DFS(adj, 1, visited);
}
```

# output:

![image](https://github.com/user-attachments/assets/fa18232a-996d-484e-84a7-5a33bb4e48c4)

# RESULT: 
 
Thus, the C++ program to write C++ Program to implementation DFS using Vector STL is created successfully.
