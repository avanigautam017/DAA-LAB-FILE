<div align="center">

# MODY UNIVERSITY OF SCIENCE AND TECHNOLOGY

## School of Engineering and Technology

<br>

<img width="154" height="157" alt="Mody_University_logo" src="https://github.com/user-attachments/assets/11e32514-7869-4f2d-afc9-b45171b58488" />


<br>

# PYTHON PROGRAMMING LAB

### LAB RECORD

<br><br>

**Student Name:** Avani Gautam
**Enrollment Number:** 240026

<br>

**Faculty Name:** Dr. P. K. Bishnoi

<br><br>

**Mody University of Science and Technology**
**School of Engineering and Technology**
Lakshmangarh, Rajasthan

</div>

---

<div style="page-break-after: always;"></div>

# INDEX

# INDEX

<table style="width:100%; border-collapse:collapse;">
  <tr>
    <th style="width:10%;">S. No.</th>
    <th style="width:65%;">Program</th>
    <th style="width:25%;">Link</th>
  </tr>

  <tr>
    <td>1</td>
    <td>Addition of Two Number</td>
    <td><a href="#program-1-addition-of-two-numbers">Program 1</a></td>
  </tr>

  <tr>
    <td>2</td>
    <td>Largest of Three Numbers</td>
    <td><a href="#program-2-largest-of-three-numbers">Program 2</a></td>
  </tr>

  <tr>
    <td>3</td>
    <td>Factorial of a Number</td>
    <td><a href="#program-3-factorial-of-a-number">Program 3</a></td>
  </tr>

  <tr>
    <td>4</td>
    <td>Prime Number Check</td>
    <td><a href="#program-4-prime-number-check">Program 4</a></td>
  </tr>

  <tr>
    <td>5</td>
    <td>Fibonacci Series</td>
    <td><a href="#program-5-fibonacci-series">Program 5</a></td>
  </tr>
</table>


---

<div style="page-break-after: always;"></div>

# Program 1: Finding Execution Time

## Aim

To write a Python program to find execution time.

## Program

```import time

start = time.time()

# Program
for i in range(1000000):
    pass

end = time.time()

print("Execution Time:", end - start, "seconds")
```

## Sample Output

```text
Enter first number: 10
Enter second number: 20
Sum = 30
```

[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 2: Finding Memory Used

## Aim

To write a Python program to find the memory used.

## Program

```import tracemalloc

tracemalloc.start()

# Program
a = [i for i in range(100000)]

current, peak = tracemalloc.get_traced_memory()

print("Current Memory:", current, "bytes")
print("Peak Memory:", peak, "bytes")

tracemalloc.stop()
```

## Sample Output

```text
Enter first number: 10
Enter second number: 25
Enter third number: 15
Largest number = 25
```

[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 3: Create Graph

## Aim

To write a Python program to create a Graph.

## Program

```import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 30, 25]

plt.plot(x, y)
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Simple Line Graph")
plt.show()
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 4: Multiple Graph

## Aim

To write a Python program to create multiple graph.

## Program

``import matplotlib.pyplot as plt
import math
x = [1, 2, 3, 4, 5]
y = [10, 15, 13, 17, 20]
y1=[math.log(i) for i in x]
y2=[i for i in x]
y3=[i*math.log(i) for i in x]
y4=[i*i for i in x]
plt.plot(x, y1, marker='o')
plt.plot(x, y2, marker='o')
plt.plot(x, y3, marker='o')
plt.plot(x, y4, marker='o')
plt.title("Line Graph")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.grid(True)
plt.show()
```

## Sample Output

```text
Enter number of terms: 7
0 1 1 2 3 5 8
```

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 5: Undirected Graph

## Aim

To write a Python program to create a Undirected Graph.

## Program

```import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 30, 25]

plt.plot(x, y)
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Simple Line Graph")
plt.show()
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 6: Directed Graph

## Aim

To write a Python program to create a Directed Graph.

## Program

```import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 30, 25]

plt.plot(x, y)
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Simple Line Graph")
plt.show()
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 7: Undirected Weighted Graph
## Aim

To write a Python program to create a undirected weighted Graph.

## Program

```class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2, weight):
        node1.neighbors.append((node2, weight))
        node2.neighbors.append((node1, weight))

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")

            for neighbor, weight in node.neighbors:
                print(f"{neighbor.data}({weight})", end=" ")

            print()
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 8: Directed Weighted Graph
## Aim

To write a Python program to create a Directed Weighted Graph.

## Program

```class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []

class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2, weight):
        node1.neighbors.append((node2, weight))

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")

            for neighbor, weight in node.neighbors:
                print(f"{neighbor.data}({weight})", end=" ")

            print()
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 9: BFS 

## Aim

To write a Python program to create BFS.

## Program

```# BFS
    def BFS(self, start):
        visited = set()
        queue = deque([start])
        visited.add(start)

        while queue:
            node = queue.popleft()
            print(node.data, end=" ")

            for neighbor in node.neighbors:
                if neighbor not in visited:
                    visited.add(neighbor)
                    queue.append(neighbor)
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 10: DFS

## Aim

To write a Python program to create a DFS.

## Program

```def DFS(self, start, visited=None):
        if visited is None:
            visited = set()

        visited.add(start)
        print(start.data, end=" ")

        for neighbor in start.neighbors:
            if neighbor not in visited:
                self.DFS(neighbor, visited)
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 11: Dijkstra Function

## Aim

To write a Python program to illustrate dijkstra function.

## Program

```def dijkstra(self, source):

        distance = {}

        # Step 1: Initialize distances
        for node in self.nodes:
            distance[node] = float('inf')

        distance[source] = 0

        visited = set()

        # Step 2: Repeat until all nodes are visited
        while len(visited) < len(self.nodes):

            # Find minimum-distance unvisited node
            current = None
            min_distance = float('inf')

            for node in self.nodes:
                if node not in visited and distance[node] < min_distance:
                    min_distance = distance[node]
                    current = node

            if current is None:
                break

            # Mark current node visited
            visited.add(current)

            # Relax edges
            for neighbor, weight in current.neighbors:

                new_distance = distance[current] + weight

                if new_distance < distance[neighbor]:
                    distance[neighbor] = new_distance

        return distance
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 12: Bell-Man Ford

## Aim

To write a Python program to display Bell-Man Ford.

## Program

```# Bellman-Ford Algorithm
    def bellman_ford(self, source):

        # Step 1: Initialize distances
        distance = {}

        for node in self.nodes:
            distance[node] = float('inf')

        distance[source] = 0

        # Step 2: Relax all edges V-1 times
        for i in range(len(self.nodes) - 1):

            for node in self.nodes:

                for neighbor, weight in node.neighbors:

                    if distance[node] != float('inf'):

                        new_distance = distance[node] + weight

                        if new_distance < distance[neighbor]:
                            distance[neighbor] = new_distance

        # Step 3: Check for negative weight cycle
        for node in self.nodes:

            for neighbor, weight in node.neighbors:

                if distance[node] != float('inf'):

                    if distance[node] + weight < distance[neighbor]:
                        print("Negative weight cycle detected!")
                        return None

        return distance
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

