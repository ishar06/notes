# GENETIC ALGORITHMS (GA)
---
## Introduction
- **Genetics**: Science of similarities and differences in species.
- **Word origin**: "Genesis" (Greek) meaning "to grow" or "to become".
- **Evolutionary Computing**:
  - Introduced by **I. Rechenberg** (1960s) through "Evolution Strategies".
- **Genetic Algorithms**:
  - Invented by **John Holland** (Father of Genetic Algorithms).
  - Developed in **1975** — Book: *"Adaptation in Natural and Artificial Systems"*.
  - Based on **Darwin’s principle**: *"Survival of the Fittest"*.
  - Useful for **search** and **optimization problems**.

## Definition
- Genetic Algorithms (GAs) are **adaptive heuristic search algorithms** based on the principles of **natural selection** and **genetics**.
- They are **robust** against input changes and noise.
- They offer advantages in:
  - Searching large state-spaces
  - Multimodal landscapes
  - High-dimensional optimization problems

## Genetic Algorithms vs Traditional Optimization

| Feature | Genetic Algorithms (GAs) | Traditional Algorithms |
|:---|:---|:---|
| Parameters | Operate on **coded versions** (e.g., binary strings) | Work directly with **actual parameters** |
| Search Method | **Population-based** (global search) | **Single point-based** (local search) |
| Derivative Requirement | **No derivatives needed** (fitness function) | **Require derivatives** (gradients) |
| Approach | **Probabilistic rules** (selection, crossover, mutation) | **Deterministic rules** (fixed steps) |
| Suitable Problems | **Discrete, non-linear, non-continuous** problems | **Continuous, smooth, convex** problems |
| Parallelism | **Naturally parallel** (evaluate many solutions) | **Sequential** (evaluate one solution at a time) |
| Robustness | **More robust** to noise and changes | **Sensitive** to initial conditions |
| Local Optima Handling | **Better at avoiding** local minima | **Can get trapped** in local minima |

## Quick MCQ Highlights
- Father of Genetic Algorithms → **John Holland**.
- GA is based on → **Natural Selection** and **Survival of the Fittest**.
- GA was invented in → **1975**.
- Evolutionary Computing introduced by → **I. Rechenberg** (1960s).
- GA works with a **population of solutions**, not a single solution.
- GA **does not require** derivatives or gradient information.
- GA is **robust** and **better at avoiding local optima** compared to traditional optimization algorithms.

---

# Basic Terminologies in Genetic Algorithm 

| Biology/GA Term | Programming Analogy | Example (Robot) |
|:---|:---|:---|
| **Allele** | Value assigned to a gene (like value of a variable) | `int speed = 5` (5 is allele) |
| **Gene** | A variable/parameter in the solution | `speed` is the gene |
| **Chromosome** | Complete set of genes (one solution); like struct/object | Struct with `speed`, `direction`, etc. |
| **Genome** | Full blueprint (chromosomes + behavior); like a class | `Robot` class with struct + methods |
| **Gene Pool** | All possible values a variable can take | Speed 1–10, Direction N/S/E/W |
| **Genotype** | Internal encoding (not directly visible); like source code | Binary string `110101` |
| **Phenotype** | Visible behavior/output from genotype | Robot moves 3 steps North based on `110101` |

## Quick Highlights
- **Allele** → Value of a gene.
- **Gene** → A single parameter.
- **Chromosome** → Set of genes (solution).
- **Genome** → Full entity blueprint (chromosomes + behavior).
- **Gene Pool** → All possible values for genes.
- **Genotype** → Hidden internal structure (binary).
- **Phenotype** → Observable behavior/output.

---
## Genetic Algorithm - Important Concepts Summary

### 1. Individuals
- **Individual** = A single solution.
- Composed of:
  - **Genotype**: Raw genetic information (chromosome).
  - **Phenotype**: Observable behavior or result from genotype.
- **Chromosome**: Divided into **genes**, each representing a factor/parameter.
- Key Point: Every possible solution must map to at least one chromosome.

### 2. Populations
- **Population** = Collection of individuals.
- Important Aspects:
  - **Initial Population Generation**:
    - Should maximize diversity (large gene pool).
    - Random or heuristic-based initialization.
  - **Population Size**:
    - Larger size = better exploration but higher computation cost.
    - Typical size ≈ 100 individuals.
- Trade-off: Diversity vs Computation resources.

### 3. Search-Space
- **Search-Space** = The complete set of all possible solutions.
- Fixed after encoding.
- Analogy:
  - Search-space: All residents of Chandigarh.
  - Population: 18–35 age group candidates.

### 4. Fitness
- **Fitness**: Value of objective function evaluated on the phenotype.
- Chromosome → Decode → Objective function → Fitness value.
- **Fitness function**:
  - Single objective: `F(x) = O(x)` (e.g., maximize profit, minimize cost).
  - Multi-objective: `F(x) = f(O1(x), O2(x), ..., On(x))`.
- **Analogy**: 
  - Runtime/memory usage can act as a fitness measure for evaluating programs.

### 5. Selection Pressure
- **Selection Mechanism**: Picks better individuals for reproduction.
- **Selection Pressure**: Degree of favoring better individuals.
  - High selection pressure → Faster convergence but risk of premature convergence.
  - Low selection pressure → Slow convergence.
- **Balance needed**: Too high = suboptimal solutions; Too low = slow GA.

### 6. Convergence
- **Convergence**: Population stabilizes; no significant improvement in generations.
- **Termination Conditions**:
  - Satisfactory solution found.
  - Fixed number of generations.
  - Time or computation budget exhausted.
  - Best fitness values stagnate across generations.
- **Premature Convergence**:
  - Loss of diversity too early → stuck in local optimum.
- **Causes**:
  - Small population size.
  - High selection pressure.
  - Similar parents during crossover.
  - Weak or absent mutation.

### 7. Generation
- A **generation** is the population at a particular step during the GA execution.
- As the GA progresses, each new generation refines the solutions further.

### 8. Elitism
- **Elitism**: Strategy to preserve best individuals into the next generation unchanged.
- **Approaches**:
  - Directly copying top individuals.
  - Letting top individuals participate more in crossover.
- **Purpose**: Maintain high-quality solutions and speed up convergence.
- **Caution**:
  - Too much elitism → Loss of diversity → Premature convergence.
  - Usually only 1–2 best individuals are preserved per generation.

### 9. Generational vs Steady-State GAs

| Parameter | Generational GAs | Steady-State GAs |
|:----------|:-----------------|:-----------------|
| **Elitism** | Typically no elitism; entire population replaced. | Can incorporate elitism. |
| **Population Size** | Constant size. | Constant or variable size. |
| **Convergence** | Faster convergence but risk of diversity loss. | Slower convergence but better diversity maintenance. |
| **Computational Cost** | Higher per generation (large-scale replacement). | Lower per generation (small-scale replacement). |
| **Use Case** | Good for early-phase exploration or multimodal problems. | Good for real-time or diversity-critical optimization. |

----
----

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
