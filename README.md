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

<table style="width:100%; border-collapse:collapse;">
  <tr>
    <th style="width:10%;">S. No.</th>
    <th style="width:65%;">Program</th>
    <th style="width:25%;">Link</th>
  </tr>

  <tr>
    <td>1</td>
    <td>Finding Execution time</td>
    <td><a href="#program-1-Finding-Execution-Time">Program 1</a></td>
  </tr>

  <tr>
    <td>2</td>
    <td>Finding Memory Used</td>
    <td><a href="#program-2-Finding-Memory-Used">Program 2</a></td>
  </tr>

  <tr>
    <td>3</td>
    <td>Creating Graph</td>
    <td><a href="#program-3-Create-Graph">Program 3</a></td>
  </tr>

  <tr>
    <td>4</td>
    <td>Multiple Graph</td>
    <td><a href="#program-4-Mutliple-Graph">Program 4</a></td>
  </tr>

  <tr>
    <td>5</td>
    <td>Illustrate Undirected Graph</td>
    <td><a href="#program-5-Undirected-Graph">Program 5</a></td>
  </tr>

  <tr>
    <td>6</td>
    <td>Illustrate Directed Graph</td>
    <td><a href="#program-6-Directed-Graph">Program 6</a></td>
  </tr>

  <tr>
    <td>7</td>
    <td>Illustrate Undirected Weighted Graph</td>
    <td><a href="#program-7-Undirected-Weighted-Graph">Program 7</a></td>
  </tr>

  <tr>
    <td>8</td>
    <td>Illustrate Directed Weighted Graph</td>
    <td><a href="#program-8-Undirected-Weighted-Graph">Program 8</a></td>
  </tr>

  <tr>
    <td>9</td>
    <td>Implementing BFS</td>
    <td><a href="#program-9-Breadth-first Search(BFS)">Program 9</a></td>
  </tr>

  <tr>
    <td>10</td>
    <td>Implementing DFS</td>
    <td><a href="#program-10-DFS">Program 10</a></td>
  </tr>

  <tr>
    <td>11</td>
    <td>Implementing Dijkstra Function</td>
    <td><a href="#program-11-Dijkstra-Function">Program 11</a></td>
  </tr>

  <tr>
    <td>12</td>
    <td>Implementing Bell-Man Ford</td>
    <td><a href="#program-12-Bell-Man-Ford">Program 12</a></td>
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

<img width="693" height="152" alt="image" src="https://github.com/user-attachments/assets/ee849877-912c-418f-88ac-c3dff378dd4c" />


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

<img width="451" height="162" alt="image" src="https://github.com/user-attachments/assets/8f68df16-5a56-4734-b7b5-002ec768c887" />

[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 3: Create Graph

## Aim

To write a Python program to create a Graph.

## Program

```
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 30, 25]

plt.plot(x, y)
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Simple Line Graph")
plt.show()
```

## Sample Output

<img width="782" height="663" alt="image" src="https://github.com/user-attachments/assets/d81437bd-ecea-4a98-a952-bcfb0063e43d" />


[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 4: Multiple Graph

## Aim

To write a Python program to create multiple graph.

## Program

```
import matplotlib.pyplot as plt
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

<img width="348" height="291" alt="image" src="https://github.com/user-attachments/assets/1b568757-6115-45e8-a97a-bbc3f100eb50" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 5: Undirected Graph

## Aim

To write a Python program to create a Undirected Graph.

## Program

```
class Node:
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

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)
        node2.neighbors.append(node1)

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")

            for neighbor in node.neighbors:
                print(neighbor.data, end=" ")

            print()


# Main program
g = Graph()

a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

g.add_edge(a, b)
g.add_edge(a, c)
g.add_edge(b, d)
g.add_edge(c, d)

g.print_graph()
```

## Sample Output

<img width="461" height="167" alt="image" src="https://github.com/user-attachments/assets/47d30b6d-b256-4859-80e6-ad1932cedd69" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 6: Directed Graph

## Aim

To write a Python program to create a Directed Graph.

## Program

```
class Node:
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

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")

            for neighbor in node.neighbors:
                print(neighbor.data, end=" ")

            print()


# Main program
g = Graph()

a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

g.add_edge(a, b)
g.add_edge(a, c)
g.add_edge(b, d)
g.add_edge(c, d)

g.print_graph()
```

## Sample Output

<img width="527" height="155" alt="image" src="https://github.com/user-attachments/assets/81fa18d3-7739-4851-921c-ddbb664dd4f3" />


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


# Main program
g = Graph()

a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

g.add_edge(a, b, 5)
g.add_edge(a, c, 3)
g.add_edge(b, d, 2)
g.add_edge(c, d, 4)

g.print_graph()
```

## Sample Output

<img width="492" height="208" alt="image" src="https://github.com/user-attachments/assets/9b05d70c-abbe-4b4f-a239-1c34f61900bc" />

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 8: Directed Weighted Graph
## Aim

To write a Python program to create a Directed Weighted Graph.

## Program

```
class Node:
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


# Main program
g = Graph()

a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

g.add_edge(a, b, 5)
g.add_edge(a, c, 3)
g.add_edge(b, d, 2)
g.add_edge(c, d, 4)

g.print_graph()
```

## Sample Output
<img width="532" height="162" alt="image" src="https://github.com/user-attachments/assets/29eb1dec-4862-4da5-bfab-9ee5670a65ca" />




[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 9: Breadth-first Search(BFS) 

## Aim

To write a Python program to implement Breadth-first Search(BFS).

## Program

```
from collections import deque

class Node:
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

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)
        node2.neighbors.append(node1)

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


# Main program
g = Graph()

a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

g.add_edge(a, b)
g.add_edge(a, c)
g.add_edge(b, d)
g.add_edge(c, d)

print("BFS Traversal:")
g.BFS(a)
```

## Sample Output

<img width="516" height="115" alt="image" src="https://github.com/user-attachments/assets/08e79acb-72cb-48cd-b793-16f811723ed9" />



[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 10: DFS

## Aim

To write a Python program to implement a DFS.

## Program

```
class Node:
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

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)
        node2.neighbors.append(node1)

    def DFS(self, start, visited=None):
        if visited is None:
            visited = set()

        visited.add(start)
        print(start.data, end=" ")

        for neighbor in start.neighbors:
            if neighbor not in visited:
                self.DFS(neighbor, visited)


# Main program
g = Graph()

a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

g.add_edge(a, b)
g.add_edge(a, c)
g.add_edge(b, d)
g.add_edge(c, d)

print("DFS Traversal:")
g.DFS(a)
```

## Sample Output

<img width="503" height="152" alt="image" src="https://github.com/user-attachments/assets/c6c02fdd-b724-433b-a257-b28bbb20ade4" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 11: Dijkstra Function

## Aim

To write a Python program to illustrate dijkstra function.

## Program

```
class Node:
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

    def dijkstra(self, source):
        distance = {}

        # Step 1: Initialize distances
        for node in self.nodes:
            distance[node] = float('inf')

        distance[source] = 0
        visited = set()

        # Step 2: Find shortest distances
        while len(visited) < len(self.nodes):
            current = None
            min_distance = float('inf')

            for node in self.nodes:
                if node not in visited and distance[node] < min_distance:
                    min_distance = distance[node]
                    current = node

            if current is None:
                break

            visited.add(current)

            # Step 3: Update neighbor distances
            for neighbor, weight in current.neighbors:
                if neighbor not in visited:
                    new_distance = distance[current] + weight

                    if new_distance < distance[neighbor]:
                        distance[neighbor] = new_distance

        return distance


# Main program
g = Graph()

a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

g.add_edge(a, b, 4)
g.add_edge(a, c, 1)
g.add_edge(c, b, 2)
g.add_edge(b, d, 1)
g.add_edge(c, d, 5)

distances = g.dijkstra(a)

print("Shortest distances from A:")
for node, dist in distances.items():
    print(node.data, ":", dist)
```

## Sample Output
<img width="387" height="197" alt="image" src="https://github.com/user-attachments/assets/93465aae-17cf-4aa2-8ba1-3a74c74d2993" />

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 12: Bell-Man Ford

## Aim

To write a Python program to illustrate Bell-Man Ford.

## Program

```
class Node:
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

    def bellman_ford(self, source):
        # Step 1: Initialize distances
        distance = {}

        for node in self.nodes:
            distance[node] = float('inf')

        distance[source] = 0

        # Step 2: Relax all edges V-1 times
        for i in range(len(self.nodes) - 1):
            updated = False

            for node in self.nodes:
                for neighbor, weight in node.neighbors:
                    if distance[node] != float('inf'):
                        new_distance = distance[node] + weight

                        if new_distance < distance[neighbor]:
                            distance[neighbor] = new_distance
                            updated = True

            if not updated:
                break

        # Step 3: Check for negative-weight cycle
        for node in self.nodes:
            for neighbor, weight in node.neighbors:
                if distance[node] != float('inf'):
                    if distance[node] + weight < distance[neighbor]:
                        print("Negative weight cycle detected!")
                        return None

        return distance


# Main program
g = Graph()

a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

g.add_edge(a, b, 4)
g.add_edge(a, c, 5)
g.add_edge(b, c, -2)
g.add_edge(b, d, 6)
g.add_edge(c, d, 3)

distances = g.bellman_ford(a)

if distances is not None:
    print("Shortest distances from A:")
    for node, dist in distances.items():
        print(node.data, ":", dist)
```

## Sample Output

<img width="461" height="177" alt="image" src="https://github.com/user-attachments/assets/01244dac-7e4d-4aa9-963c-da1f452db4c1" />

[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

