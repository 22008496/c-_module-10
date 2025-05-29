
# EX.NO : 10(B)  BREADTH FIRST SEARCH-BFS 
 
# PROGRAM STATEMENT: 
 
To write A CPP Program to implement BFS using vectors and queue. (use double data)

![image](https://github.com/user-attachments/assets/aac309cf-24fe-419b-94b4-3bb145105553)

 
 
# ALGORITHM:   
 
1. Start the program. 
2. Define graph structure: Create a 2D vector g to store the adjacency list and a vector v to track visited nodes. 
3. Edge addition: Define the edge function to add an undirected edge between nodes by updating the adjacency list. 
4. BFS traversal: Implement BFS using a queue. Start from a node, mark it visited, and explore its neighbors in the queue. 
5. Input edges and nodes: Read the number of nodes and edges from the user, followed by pairs of nodes representing edges. Store these in the adjacency list. 
6. End the program: Traverse the graph, calling BFS on unvisited nodes, and output the BFS traversal order. 
 
# PROGRAM: 
```
// A Quick implementation of BFS using
// vectors and queue
#include <bits/stdc++.h>
#define pb push_back

using namespace std;

vector<bool> v;
vector<vector<float> > g;

void edge(int a, int b)
{
	g[a].pb(b);

	// for undirected graph add this line
	// g[b].pb(a);
}

void bfs(int u)
{
	queue<float> q;

	q.push(u);
	v[u] = true;

	while (!q.empty()) {

		int f = q.front();
		q.pop();
		cout << f << " ";

		// Enqueue all adjacent of f and mark them visited
		for (auto i = g[f].begin(); i != g[f].end(); i++) {
			if (!v[*i]) {
				q.push(*i);
				v[*i] = true;
			}
		}
	}
}

// Driver code
int main()
{
	int n, e;
	cin >> n >> e;

	v.assign(n, false);
	g.assign(n, vector<float>());

	int a, b;
	for (int i = 0; i < e; i++) {
		cin >> a >> b;
		edge(a, b);
	}

	for (int i = 0; i < n; i++) {
		if (!v[i])
			bfs(i);
	}

	return 0;
}
```
# output:

![image](https://github.com/user-attachments/assets/6c24a08c-762f-4b43-baf2-1feda4adb7d4)

# RESULT: 
 
Thus, the C++ program to implement BFS using vectors and queue is created successfully. 



