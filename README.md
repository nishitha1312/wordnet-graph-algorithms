# WordNet Graph Algorithms

A Java-based implementation of **WordNet semantic analysis** using **directed graphs** and **shortest ancestral path (SAP)** algorithms.

This project models linguistic relationships using graph traversal techniques and identifies semantic distances and outliers among nouns.

---

## Tech Stack

- **Java**
- **Princeton Algorithms (algs4) Library**
- **Directed Graphs**
- **Breadth-First Search (BFS)**
- **Topological Sorting**
- **Red-Black BST**

---

## Project Components

### WordNet.java
Builds a semantic network of English nouns using synsets and hypernym relationships.

**Responsibilities:**
- Parses synsets and hypernyms files
- Constructs a directed acyclic graph (DAG)
- Validates single-rooted structure
- Computes semantic distance between nouns
- Finds shortest ancestral paths

---

### SAP.java (Shortest Ancestral Path)
Computes the shortest path between two vertices (or vertex sets) that share a common ancestor.

**Key Features:**
- Uses **BFS** from multiple sources
- Efficient ancestor distance computation
- Supports single vertex and iterable inputs
- Time complexity: **O(V + E)** per query

---

### Outcast.java
Identifies the noun that is least semantically related to others in a given list.

**Approach:**
- Computes total semantic distance of each noun to all others
- Selects the noun with the maximum cumulative distance

---

## How to Run

### Compile
```bash
javac -cp .:algs4.jar *.java
Run WordNet
java -cp .:algs4.jar WordNet synsets.txt hypernyms.txt
Run Outcast
java -cp .:algs4.jar Outcast synsets.txt hypernyms.txt outcast11.txt
Algorithms Used
Breadth-First Search (BFS)

Directed Acyclic Graph (DAG) validation

Topological ordering

Shortest ancestral path computation

Red-Black Binary Search Tree for fast lookup

** Notes**
Graph validation ensures single root and no cycles

Designed for large datasets

Implements defensive argument checking

Follows modular class design

-Author
Sai Nishitha Muraharisetty

