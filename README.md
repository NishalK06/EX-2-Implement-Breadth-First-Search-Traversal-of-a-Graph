# EX-2: Implement-Breadth-First-Search-Traversal-of-a-Graph

**Name: K NISHAL**

**Register Number: 2305001021**

### Aim:
To Implement Breadth First Search Traversal of a Graph using Python 3.

### Theory:
Breadth-First Traversal (or Search) for a graph is like the Breadth-First Traversal of a tree. The only catch here is that, unlike trees, graphs may contain cycles so that we may come to the same node again. To avoid processing a node more than once, we divide the vertices into two categories:

Visited

Not Visited

A Boolean visited array is used to mark the visited vertices. For simplicity, it is assumed that all vertices are reachable from the starting vertex. BFS uses a queue data structure for traversal.

**How does BFS work?**
Starting from the root, all the nodes at a particular level are visited first, and then the next level nodes are traversed until all the nodes are visited. To do this, a queue is used. All the adjacent unvisited nodes of the current level are pushed into the queue, and the current-level nodes are marked visited and popped from the queue. Illustration: Let us understand the working of the algorithm with the help of the following example. 

### Algorithm:

step 1: Construct a Graph with Nodes and Edges

Step 2: Breadth First Uses Queue and iterates through the Queue for Traversal.

Step 3: Insert a Start Node into the Queue.

Step 4: Find its Successors Or neighbors and Check whether the node is visited or not.

Step 5: If Not Visited, add it to the Queue. Else Continue.

Step 6: Iterate steps 4 and 5 until all nodes get visited, and there are no more unvisited nodes.

### Program:
```
def bfs(graph, start):
    visited = []  
    queue = [start]  

    while queue:
        node = queue.pop(0)  
        if node not in visited:
            visited.append(node)  
            queue.extend(graph.get(node, []))  

    return visited

graph = {}
n = int(input("Enter number of nodes: "))  

for _ in range(n):
    node = input("Enter node: ")
    neighbors = input(f"Enter neighbors of {node} (comma separated): ").split(",")
    graph[node] = [neighbor.strip() for neighbor in neighbors]  

start_node = input("Enter the starting node for BFS: ")


print("BFS Traversal Order:", bfs(graph, start_node))
```
### Sample Input:

Enter number of nodes: 3

Enter node: A

Enter neighbors of A (comma separated): B

Enter node: B

Enter neighbors of B (comma separated): C

Enter node: C

Enter neighbors of C (comma separated): 

Enter the starting node for BFS: A

### Sample Output:

BFS Traversal Order: ['A', 'B', 'C']
### Input:

![WhatsApp Image 2025-09-08 at 14 27 54_ed2c8a21](https://github.com/user-attachments/assets/71fce49d-814c-4ec0-8596-9813beb49ca9)


### Output:
![WhatsApp Image 2025-09-08 at 14 28 40_0f5b7bbd](https://github.com/user-attachments/assets/a26d9194-c8b7-47f2-9599-f3a42ce34a2a)




### Result:
Thus the program to implement bredth first search of a traversal graph has been executed successfully.
