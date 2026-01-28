# WordNet Graph Algorithms

A Java-based implementation of **WordNet semantic analysis** using **directed graphs** and **shortest ancestral path (SAP)** algorithms.

This project models linguistic relationships using graph traversal techniques and identifies semantic distances and outliers among nouns.

---

## 🛠 Tech Stack

- **Java**
- **Princeton Algorithms (algs4) Library**
- **Directed Graphs**
- **Breadth-First Search (BFS)**
- **Topological Sorting**
- **Red-Black BST**

---

## 📂 Project Components

### 1️⃣ WordNet.java
Builds a semantic network of English nouns using synsets and hypernym relationships.

**Responsibilities:**
- Parses synsets and hypernyms files
- Constructs a directed acyclic graph (DAG)
- Validates single-rooted structure
- Computes semantic distance between nouns
- Finds shortest ancestral paths

---

### 2️⃣ SAP.java (Shortest Ancestral Path)
Computes the shortest path between two vertices (or vertex sets) that share a common ancestor.

**Key Features:**
- Uses **BFS** from multiple sources
- Efficient ancestor distance computation
- Supports single vertex and iterable inputs
- Time complexity: **O(V + E)** per query

---

### 3️⃣ Outcast.java
Identifies the noun that is least semantically related to others in a given list.

**Approach:**
- Computes total semantic distance of each noun to all others
- Selects the noun with the maximum cumulative distance

---

## 📁 File Structure

