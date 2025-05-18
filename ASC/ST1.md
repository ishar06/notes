* **Computing Model**

  * Input (Antecedent) → Function $f$ (Computing Unit) → Output (Consequent)
  * Function $f$ = formal method/algorithm/mapping that processes $x$ into $y$
  * Control actions = step-by-step instructions guiding input toward output

* **Basic Characteristics of Computing**

  * **Precise Solution**: produces exact, definitive answers
  * **Unambiguous & Accurate**: each control action has one interpretation and must be correct
  * **Mathematical Model**: relies on a well-defined algorithm representing the problem

* **Types of Computing**

  * **Hard Computing** (L.A. Zadeh, 1996)

    * Deterministic, exact, no approximation
    * Based on strict mathematical models and algorithms
    * **Features**:

      * Exact results (identical output every run)
      * Unambiguous control actions
      * Fixed, rule-based steps
    * **Examples**:

      * Numerical problem solving (equations, arithmetic)
      * Searching and sorting algorithms
      * Computational geometry (distances, areas)
  * **Soft Computing**

    * Emulates human-like reasoning under uncertainty and imprecision
    * Tolerates approximation, partial truth, and incomplete data
    * Combines methods (fuzzy logic, neural networks, genetic algorithms)
    * **Guiding Principle**: exploit tolerance for imprecision to achieve robustness and low cost

* **Requirements & Advantages of Soft Computing**

  * Handles uncertainty and partial truths (e.g., medical diagnosis with incomplete symptoms)
  * Adapts and learns from data (e.g., neural networks for stock market trends)
  * Tolerates noise/incomplete information (e.g., image recognition in self-driving cars)
  * Easier implementation for complex systems (e.g., fuzzy control without exact models)
  * Mimics human reasoning for decision-making (e.g., customer service responses)

* **Real‑World Analogies**

  * **Hard**: Manual transmission car (driver makes exact gear shifts)
  * **Soft**: Automatic transmission with fuzzy logic (adapts gear shifts to conditions)
  * **Hard**: Manual air‑conditioner (fixed temperature/fan settings)
  * **Soft**: Smart AC (adjusts cooling based on room size, occupancy, weather)

* **Key Differences: Hard vs. Soft Computing**

  | Aspect         | Hard Computing                | Soft Computing                     |
  | -------------- | ----------------------------- | ---------------------------------- |
  | Logic          | Precise binary (0/1)          | Approximate, fuzzy                 |
  | Solutions      | Exact                         | Approximate                        |
  | Flexibility    | Rigid, no uncertainty         | Flexible, handles uncertainty      |
  | Models         | Strict mathematical           | Probabilistic/heuristic            |
  | Error Handling | Errors not tolerated          | Errors/uncertainty accepted        |
  | Learning       | None                          | Adaptive, learns from experience   |
  | Computation    | Sequential                    | Parallel                           |
  | Nature         | Deterministic                 | Stochastic                         |
  | Examples       | Sorting, arithmetic, geometry | Neural networks, fuzzy systems, GA |


* **Fuzzy Computing**

  * Extends binary logic to handle qualitative, subjective, approximate situations
  * **Key Concepts:**

    * Membership function μₐ(x): assigns each element a grade \[0, 1] of belonging to fuzzy set A
    * Fuzzification: mapping crisp inputs to fuzzy membership grades
    * Rule base of “if‑then” fuzzy descriptors (e.g., “If speed is slow and target is far, then moderately increase power”)
  * **Smooth vs. Step Regulator Example:**

    * Step regulator: abrupt speed jumps at thresholds (e.g., Low/Med/High only)
    * Smooth regulator: fan speed varies continuously (e.g., 70 % Med at 25 °C, 90 % Med at 28 °C)

* **Neural Networks**

  * Composed of interconnected nodes (neurons) organized in layers, linked by weighted synapses
  * Each neuron computes $y = f\bigl(\sum_i w_i x_i + w_0\bigr)$, firing when weighted sum exceeds threshold
  * **Types:**

    * **Feedforward Networks:** signal flows one-way; trained via supervised learning (adjust weights to minimize output error)
    * **Feedback (Recurrent) Networks:** outputs fed back into hidden or input layers, providing memory and dynamic behavior

* **Genetic Algorithms (GAs)**

  * Population-based search that “evolves” solutions via selection, crossover, mutation
  * **Process:**

    1. Initialize diverse population of candidate solutions
    2. Evaluate fitness of each individual
    3. Select high‑fitness individuals to reproduce
    4. Apply crossover (recombination) and mutation to create next generation
    5. Repeat until convergence or stop criterion
  * **Characteristics:** probabilistic, exploits population diversity, escapes local minima via mutation

* **Associative Memory**

  * Content‑addressable storage: retrieves data by input pattern rather than address
  * **Auto‑associative Memory:** recalls complete stored pattern from partial/noisy input (e.g., “H\*LLO” → “HELLO”)
  * **Hetero‑associative Memory:** maps input pattern to a different output pattern (e.g., “cat” → “animal”)
  * Often implemented via neural nets or fuzzy systems to handle imprecise data

* **Adaptive Resonance Theory (ART)**

  * Addresses stability–plasticity dilemma: learn new patterns without forgetting old ones
  * **Core Concepts:**

    * Resonance: match between input and stored category triggers learning/reinforcement
    * Vigilance parameter: controls granularity of clustering (high → finer categories; low → broader categories)
    * Unsupervised clustering: dynamically creates or updates categories based on input similarity
  * **Variants:**

    * ART1: binary inputs
    * ART2: continuous‑valued inputs
    * ART3: hierarchical processing
    * Fuzzy ART: integrates fuzzy logic for handling uncertainty
  * **Applications:** image recognition clustering, anomaly detection in security, customer‑segmentation data mining, robot environment mapping

* **Definition:**

  * A fuzzy set $A$ on universe $X$ allows partial membership; each element $x\in X$ has a grade $\mu_A(x)\in[0,1]$.
  * No sharp boundary—there’s a gradual transition between membership and non‑membership.

* **Membership Function:**

  * $\mu_A(x)\!: X \to [0,1]$ assigns each $x$ its degree of belonging.

    * $\mu_A(x)=0$ ⇒ definitely not in $A$
    * $\mu_A(x)=1$ ⇒ definitely in $A$
    * $0<\mu_A(x)<1$ ⇒ boundary (partial) elements

* **Symbolic Representation:**

  * $A = \{(x,\mu_A(x))\mid x\in X\}$ or succinctly $A = \{x \mid \mu_A(x)\}$.

* **Key Subsets:**

  * **Support Set** $S_A = \{x\mid \mu_A(x)>0\}$ (crisp set of all elements with nonzero membership)
  * **Core** $C_A = \{x\mid \mu_A(x)=1\}$ (elements fully in $A$)
  * Boundary elements = $S_A\setminus C_A$

* **Universe of Discourse:**

  * The complete domain $X$ from which elements are drawn (e.g., all temperatures 0–50 °C).
  * Can be **discrete** (countable elements: letters, integers) or **continuous** (any value in a range: temperature, time).

* **Fuzzy Subset & Equality:**

  * $A\subseteq B$ iff $\mu_A(x)\le\mu_B(x)$ ∀ $x$.
  * $A = B$ iff $\mu_A(x)=\mu_B(x)$ ∀ $x$.

* **Special Fuzzy Sets:**

  * **Universal Fuzzy Set**: $\mu_A(x)=1$ ∀ $x\in X$.
  * **Empty Fuzzy Set**: $\mu_A(x)=0$ ∀ $x\in X$.

* **Fuzzy Power Set:**

  * The collection of all fuzzy subsets of $X$, denoted $P(X)$, is infinite in cardinality.

* **Cardinality of a Fuzzy Set:**

  * $\lvert A\rvert = \sum_{x\in U} \mu_A(x)$ (discrete case)

    * e.g., if $A=\{(1,0.5),(2,1.0),(3,0.2)\}$, then $\lvert A\rvert=1.7$.

* **Example (“Warm” Temperatures):**

  * Universe: 0 °C–50 °C
  * Fuzzy set $W$:

    $$
      W = \{(20,0.2),(25,0.5),(30,0.8),(35,1.0),(40,0.6)\}
    $$
  * Support $S_W=\{20,25,30,35,40\}$, Core $C_W=\{35\}$, Boundary = $\{20,25,30,40\}$.

* **Practical Notes:**

  * Fuzzy sets model vagueness (e.g., “warm,” “tall”) where crisp intervals don’t capture human perception.
  * Widely used in control systems, decision‑making, and AI to handle imprecise information.

---

* **Zadeh’s “Formal Series” Notation (Discrete Universe)**

  * Represents fuzzy set $A$ as a combination of element–grade pairs:

    $$
      A = \frac{\mu_A(x_1)}{x_1} + \frac{\mu_A(x_2)}{x_2} + \cdots + \frac{\mu_A(x_i)}{x_i} + \cdots
    $$
  * “+” is just a notational concatenation of pairs, not numeric summation.
  * **Example:** on $X=\{1,2,3,\dots\}$,

    $$
      A = 0.2/3 + 0.3/4 + 1.0/5 + 0.2/6 + 0.1/7
    $$

* **Symbolic Integration Notation (Continuous Universe)**

  * Fuzzy set $A$ written as

    $$
      A = \int_X \mu_A(x)\,/\,x
    $$
  * The integral sign is symbolic—no actual calculus is implied.
  * **Example:** $\mu_A(x)=\frac{1}{1+(x-a)^{10}}$ defines a fuzzy “relation” around $x=a$.

* **Linguistic Variables & Hedges**

  * Fuzzy descriptors (“tall,” “beautiful,” “fast”) are linguistic variables.
  * Modifiers such as “very,” “slightly,” “extremely” are **hedges** that adjust membership functions.

* **Crisp vs. Fuzzy Sets**

  | Aspect             | Crisp Set                     | Fuzzy Set                                      |
  | ------------------ | ----------------------------- | ---------------------------------------------- |
  | Representation     | $S = \{\,s\mid s\in X\}$      | $F = \{(s,\mu(s))\mid s\in X,\mu(s)\in[0,1]\}$ |
  | Membership         | Binary (0 or 1)               | Graded \[0…1]                                  |
  | Boundary           | Sharp                         | Gradual                                        |
  | Handles Vagueness? | No                            | Yes                                            |
  | Use Cases          | Binary decisions, crisp logic | AI, control systems, pattern recognition       |

* **Special Relationships**

  * **Crisp ⊆ Fuzzy:** any crisp set is a fuzzy set with $\mu\in\{0,1\}$.
  * **Fuzzy ⊆ Crisp?** No—most fuzzy sets have intermediate grades.

* **Cardinality**

  * **Crisp:** $\lvert S\rvert$ = count of elements.
  * **Fuzzy:** $\lvert A\rvert = \sum_{x\in U} \mu_A(x)$ (discrete case).

    * Finite if $U$ finite or membership defined on finitely many $x$.
    * Infinite if $U$ infinite (e.g., real line).

* **Key Takeaways for MCQs**

  * Recognize Zadeh notation formats for discrete vs. continuous fuzzy sets.
  * Understand “+” and “∫” are symbolic, not arithmetic or calculus operations.
  * Recall crisp sets as special fuzzy sets ($\mu\in\{0,1\}$).
  * Differentiate linguistic hedges from core descriptors.
  * Be able to compute fuzzy cardinality in simple discrete examples.

---

### Fuzzy Logical Operations

* **Complement (NOT)**

  * Formula: $\mu_{A'}(x)=1-\mu_A(x)$
  * Rationale: flips degree of membership
  * Example: “hot” vs. “not hot” membership curves are mirror images

* **Union (OR / Disjunction)**

  * Formula: $\mu_{A\cup B}(x)=\max\bigl(\mu_A(x),\mu_B(x)\bigr)$
  * Rationale: element belongs if it has higher grade in either set
  * Discrete Example:

    $$
      F\!=\{0.6/80,0.8/90,1.0/100\dots\},\quad  
      M\!=\{0.6/50,0.8/60,1.0/70\dots\}
    $$

    $\Rightarrow F\lor M=\{0.6/50,0.8/60,1.0/70,1.0/80,1.0/90,1.0/100,\dots\}$

* **Intersection (AND / Conjunction)**

  * Formula: $\mu_{A\cap B}(x)=\min\bigl(\mu_A(x),\mu_B(x)\bigr)$
  * Rationale: element belongs only as strongly as its weakest membership
  * Example (“Warm” ∧ “Hot”):
    $\{20:0,25:0,30:\min(0.8,0.4)=0.4,\dots\}$

* **Equality**

  * $A=B$ iff $\mu_A(x)=\mu_B(x)$ for every $x$.

* **Difference (A – B)**

  * Formula: $\mu_{A-B}(x)=\min\bigl(\mu_A(x),1-\mu_B(x)\bigr)$

* **Algebraic Operations**

  * **Algebraic Sum:** $\mu_{A+B}(x)=\mu_A+\mu_B-\mu_A\mu_B$
  * **Algebraic Product:** $\mu_{A\cdot B}(x)=\mu_A\cdot\mu_B$

* **Bounded Operations**

  * **Bounded Sum ($\oplus$)**: $\mu_{A\oplus B}(x)=\min\bigl(1,\mu_A+\mu_B\bigr)$
  * **Bounded Difference ($\ominus$)**: $\mu_{A\ominus B}(x)=\max\bigl(0,\mu_A-\mu_B\bigr)$
  * **Bounded Product ($\odot$)**: $\mu_{A\odot B}(x)=\max\bigl(0,\mu_A+\mu_B-1\bigr)$

* **Scalar Multiplication**

  * $\mu_{\alpha A}(x)=\alpha\cdot\mu_A(x)$, for $0\le\alpha\le1$

* **Basic Fuzzy‑Logic Laws**

  * **Commutativity:** $A\cup B=B\cup A,\;A\cap B=B\cap A$
  * **Associativity:** $(A\cup B)\cup C=A\cup(B\cup C)$ etc.
  * **Distributivity:** $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$ etc.
  * **De Morgan’s:** $(A\cup B)'=A'\cap B',\;(A\cap B)'=A'\cup B'$
  * **Idempotency:** $A\cup A=A,\;A\cap A=A$
  * **Absorption:** $A\cup(A\cap B)=A,\;A\cap(A\cup B)=A$
  * **Boundary Conditions:** $A\cup X=X,\;A\cap\varnothing=\varnothing$
  * **Involution:** $(A')'=A$
  * **Transitivity:** if $A\subseteq B\subseteq C$ then $A\subseteq C$

* **Law of Excluded Middle & Contradiction (Violated)**

  * In fuzzy logic, $A\cup A'\neq X$ and $A\cap A'\neq\varnothing$; partial membership allows overlap and “middle” values.

---

* **“All my statements are false” in set terms**

  * Let $X$ = universe of all my statements, $A$ = set of those that are true, $A'$ = set of those that are false.
  * **Equation:**

    $$
      A' = X
    $$

    (i.e.\ every element of $X$ lies in $A'$.)

* **Crisp‑logic contradiction**

  * In classical (bivalent) sets, $A\cup A'=X$ and $A\cap A'=\varnothing$.
  * Requiring $A'=X$ forces $A=\varnothing$.
  * But if all statements are false, there can’t be any true ones—so $A=\varnothing$.
  * Yet in crisp logic “every statement is false” contradicts “every statement is either true or false” only if one insists on truth‑value completeness.

* **Fuzzy‑logic version**

  * Complement: $\mu_{A'}(x)=1-\mu_A(x)$
  * Union (max): $\mu_{A'\cup A'}(x)=\max\bigl(\mu_{A'}(x),\mu_{A'}(x)\bigr)=\mu_{A'}(x)$
  * Statement “$A'=X$” requires $\mu_{A'}(x)=1$ ∀ $x$, i.e.\\

    $$
      1-\mu_A(x)=1 \;\Longrightarrow\;\mu_A(x)=0\quad\forall x.
    $$
  * **Conclusion:** in fuzzy logic, “all my statements are false” holds exactly when every element’s truth‑grade is zero (i.e.\ $A$ is the zero‑membership set).

---

### Fuzzy‑Set Terminology & Properties

* **Fuzzy singleton:** support = one element with $\mu=1$, all others $\mu=0$.
* **Normal fuzzy set:** $\max_x \mu_A(x)=1$ (has at least one element at full membership).
* **Subnormal fuzzy set:** $\max_x \mu_A(x)<1$ (no element reaches $\mu=1$).
* **Height:** the maximum membership value of a fuzzy set.
* **Prototypical element:** an element with $\mu=1$ (or, if none, the one at the peak in context).
* **Crossover point:** any $x$ with $\mu_A(x)=0.5$.

  * **Bandwidth:** distance between the two crossover points $\lvert x_2 - x_1\rvert$.
* **Convex fuzzy set:**

  $$
    \mu_A(x_2)\;\ge\;\min\bigl(\mu_A(x_1),\mu_A(x_3)\bigr)
    \quad\forall\,x_1\le x_2\le x_3.
  $$

  * Intersection of convex fuzzy sets remains convex.
  * **Non‑convex** = violates the above monotonicity.
* **Fuzzy number:** a convex, normal fuzzy set on $\mathbb{R}$ with a single-point core.

---

### Classical Relations

* **Relation Basics**

  * A **binary relation** between sets $X$ and $Y$ is any subset $R\subseteq X\times Y$.
  * A **crisp** binary relation indicates only presence (1) or absence (0) of each ordered pair $(x,y)$.
  * A **fuzzy** binary relation generalizes this by assigning each $(x,y)$ a membership grade $\mu_R(x,y)\in[0,1]$, expressing strength of association.

* **Tuples & Cartesian Products**

  * An **$r$-tuple** is an ordered list $(a_1,a_2,\dots,a_r)$.
  * The **Cartesian product** $A_1\times A_2\times\cdots\times A_r$ is the set of all such $r$-tuples with $a_i\in A_i$.
  * When $r=2$, $A\times B$ yields all ordered pairs $(a,b)$.

* **$r$-Ary Relations**

  * An **$r$-ary relation** is any subset of $A_1\times\cdots\times A_r$.
  * **Binary** ($r=2$), **ternary** ($r=3$), **quaternary** ($r=4$), etc.

* **Characteristic Function & Relation Matrix**

  * For finite $X,Y$, a relation $R$ is represented by a $\lvert X\rvert\times\lvert Y\rvert$ **relation matrix** $M_R$ of 0s and 1s.
  * Entry $M_R[i,j]=1$ iff $(x_i,y_j)\in R$.

* **Example (Crisp Relation)**

  * $X=\{2,4,6\},\,Y=\{p,q,r\}$.
  * Subset $S=\{(2,p),(4,q),(6,r)\}$.
  * Relation matrix has 1s on the diagonal, 0s elsewhere.

* **Relation Notation**

  * $R: X\to Y$ means $R\subseteq X\times Y$ associates elements of $X$ (domain) with those of $Y$ (codomain).

* **Special Relations**

  * **Constrained**: defined by a rule (e.g.\ $R=\{(x,y)\mid y=2x\}$).
  * **Unconstrained**: any arbitrary subset of $X\times Y$.
  * **Universal/Complete**: $R=X\times Y$ (all possible pairs).
  * **Identity**: $I_X=\{(x,x)\mid x\in X\}$.
  * **Null**: $R=\varnothing$ (no pairs).

* **Relation Cardinality & Power Set**

  * $\lvert R\rvert$ = number of ordered pairs in $R$.
  * Power set $P(S)$ = set of all subsets of $S$; if $\lvert S\rvert=n$, then $\lvert P(S)\rvert=2^n$.

* **Operations on Relations (Crisp)**

  * **Union**: $R_1\cup R_2$ = element‑wise OR of their matrices.
  * **Intersection**: $R_1\cap R_2$ = element‑wise AND.
  * **Complement**: $R^c=(X\times Y)\setminus R$ = matrix‑flip of 0↔1.
  * **Containment**: $R_1\subseteq R_2$ iff $M_{R_1}[i,j]\le M_{R_2}[i,j]$ ∀ $i,j$.

* **Algebraic Properties of Relations**

  * **Commutativity:** $R_1\cup R_2=R_2\cup R_1,\;R_1\cap R_2=R_2\cap R_1$
  * **Associativity:** $(R_1\cup R_2)\cup R_3=R_1\cup(R_2\cup R_3)$, similarly for ∩
  * **Distributivity:** $R_1\cap(R_2\cup R_3)=(R_1\cap R_2)\cup(R_1\cap R_3)$, etc.
  * **Involution:** $(R^c)^c=R$
  * **Idempotency:** $R\cup R=R,\;R\cap R=R$
  * **De Morgan’s:** $(R_1\cup R_2)^c=R_1^c\cap R_2^c,\;(R_1\cap R_2)^c=R_1^c\cup R_2^c$
  * **Excluded Middle:** $R\cup R^c=X\times Y$
  * **Contradiction:** $R\cap R^c=\varnothing$

* **Fuzzy Relations**

  * Replace 0/1 entries with grades $\mu_R(x,y)\in[0,1]$.
  * Union/intersection use max/min on membership grades.
  * Complement: $\mu_{R^c}(x,y)=1-\mu_R(x,y)$.




* **Classical Relation Composition**

  * Given $R\subseteq X\times Y$ and $S\subseteq Y\times Z$, their composition

    $$
      R\circ S \;=\;\bigl\{(x,z)\in X\times Z\;\bigm|\;\exists\,y\in Y:\,(x,y)\in R\;\wedge\;(y,z)\in S\bigr\}.
    $$
  * **Matrix form (Boolean “multiplication”):** for relation matrices $M_R$ ($\lvert X\rvert\times\lvert Y\rvert$) and $M_S$ ($\lvert Y\rvert\times\lvert Z\rvert$),

    $$
      (M_{R\circ S})_{i,k}
      = \bigvee_{j}\bigl(M_R{}_{i,j}\wedge M_S{}_{j,k}\bigr),
    $$

    where $\vee$ = OR, $\wedge$ = AND.

* **Example (Classical)**

  * $X=\{1,2\},\;Y=\{a,b\},\;Z=\{p,q\}$
  * $R=\{(1,a),(2,b)\},\;S=\{(a,p),(b,q)\}$
  * Thus
    $\;R\circ S=\{(1,p),(2,q)\}.$

* **Fuzzy Relation Composition**

  1. **Max–Min Composition**

     $$
       \mu_{R\circ S}(x,z)
       = \max_{y\in Y}\Bigl[\min\bigl(\mu_R(x,y),\,\mu_S(y,z)\bigr)\Bigr].
     $$

     * “Min” finds the weakest link in each $x\to y\to z$ path; “Max” selects the strongest of these.
  2. **Max–Product Composition**

     $$
       \mu_{R\circ S}(x,z)
       = \max_{y\in Y}\Bigl[\mu_R(x,y)\;\times\;\mu_S(y,z)\Bigr].
     $$

     * “Product” gives the combined strength of each path; “Max” picks the best.

* **Example (Max–Min & Max–Product)**

  * Using the same $R,S$ as above (with binary 0/1 entries):

    * Both compositions yield
      $\mu_{R\circ S}(1,p)=1,\;\mu(1,q)=0,\;\mu(2,p)=0,\;\mu(2,q)=1.$

* **Key Properties of Composition**

  * **Associative:** $(R\circ S)\circ T = R\circ(S\circ T)$
  * **Non‑commutative:** generally $R\circ S\neq S\circ R$
  * **Inverse:** $(R\circ S)^{-1} = S^{-1}\circ R^{-1}$

* **DIY Template**

  1. Write $M_R$ ($\lvert A\rvert\times\lvert B\rvert$) and $M_S$ ($\lvert B\rvert\times\lvert C\rvert$).
  2. Compute Boolean or fuzzy composition with the appropriate formula.
  3. List all resulting $(x,z)$ with membership > 0 (or =1 in crisp case).
  4. Optionally draw the bipartite arrow diagram $X\to Y\to Z$.

---









