
---

## 🔹 **Encoding in Genetic Algorithms**
- **Encoding** = Process of representing individuals/solutions (chromosomes) in GA.
- Representation formats: **Bits, numbers, trees, arrays, lists**.
- Choice of encoding depends on the **type of problem**.

---

### 🔹 **Binary Encoding**
- **Most common encoding method**.
- Chromosomes are **bit strings (0s and 1s)**.
- Each bit can represent:
  - A **decision variable** (e.g., include/exclude item).
  - A **numeric value** (in some cases).
  
#### ✔ Example: 0-1 Knapsack Problem
- `xi = 1`: item i is included.
- `xi = 0`: item i is not included.
- Total combinations: **2ⁿ – 1** for n items.
  
#### ✅ **Advantages**
- Fast execution due to binary operations.
- Universal applicability across optimization problems.

#### ❌ **Limitations**
- Conversion needed (real to binary).
- **Accuracy limited** by binary representation.

---

### 🔹 **Real-Value Encoding (Real-Coded GA)**
- Genes are represented using **real (floating-point) numbers**.
- Suitable for **continuous search spaces** and **precision-sensitive** problems.
- **No conversion** required (direct real values).
  
#### ✔ Example: `[5.28, -475.36, 1.74]`
- Each value is a gene; the whole array is a chromosome.

#### ✅ **Advantages**
- More natural for real-valued problems.
- Often **simpler, faster, and more accurate**.

---

### 🔹 **Permutation Encoding (Order Encoding)**
- Chromosome = **ordered sequence** of unique elements.
- Best for **ordering problems** (e.g., **Travelling Salesman Problem**).
  
#### ✔ TSP Example:
- Chromosome: P = [c0, c1, c2, ..., cn−1]
- Constraint: each city appears **only once** (except starting city).
- Cost is minimized (distance between cities).
  
#### ✅ **Key Points**
- Avoids repetition.
- Searches over **n! permutations**.

---

### 🔹 **Tree Encoding**
- Used mainly in **Genetic Programming (GP)**.
- Chromosome is a **tree**: nodes = functions/commands.
- Suitable for evolving **programs, expressions, formulas**.
  
#### ✔ Example: Floor Planning Problem
- Programs/solutions represented as **function trees**.

---

Would you like a quick quiz or flashcards based on this for practice?
