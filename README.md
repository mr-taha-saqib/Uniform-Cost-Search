# Uniform Cost Search (UCS) Algorithm

This repository contains an implementation of the **Uniform Cost Search (UCS)** algorithm in Python. UCS is used to find the shortest path in a weighted graph, ensuring the total traversal cost is minimized. This implementation supports graphs with varying edge weights and is scalable for handling large graphs efficiently.

---

## **Features**
- Handles weighted graphs with arbitrary edge weights.
- Ensures correctness and optimality of the shortest path.
- Efficiently manages memory using a priority queue.
- Capable of processing large graphs.

---

## **Algorithm Overview**
Uniform Cost Search (UCS) is a graph traversal algorithm that expands the least-cost node first. It is a variant of Dijkstra's algorithm and ensures that the first time a goal node is expanded, it is reached via the optimal path.

### **Steps of UCS:**
1. Start at the initial node.
2. Use a priority queue to always expand the node with the least cost.
3. Mark nodes as visited to avoid revisiting them.
4. Stop when the goal node is reached, returning the optimal path and its cost.

---

## **Implementation Details**

### **Graph Class**
The graph is represented as an adjacency list, where each node points to its neighbors along with the associated edge weights.

### **Methods**
- `add_edge(start, end, weight)`: Adds a directed edge with a specified weight.
- `uniform_cost_search(start, goal)`: Executes the UCS algorithm to find the shortest path from `start` to `goal`.

---

## **Usage**

### **1. Install Dependencies**
Ensure you have Python installed. No additional libraries are required beyond the standard library.

### **2. Example Code**
```python
# Create a graph
g = Graph()
g.add_edge('A', 'B', 1)
g.add_edge('A', 'C', 4)
g.add_edge('B', 'C', 2)
g.add_edge('B', 'D', 6)
g.add_edge('C', 'D', 3)
g.add_edge('C', 'E', 5)
g.add_edge('D', 'E', 1)

# Perform UCS
start_node = 'A'
goal_node = 'E'
path, cost = g.uniform_cost_search(start_node, goal_node)

print(f"Optimal Path: {path}")
print(f"Total Cost: {cost}")
