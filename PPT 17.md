### **Formal Specification Exam Notes**

---

#### **1. Introduction to Formal Methods**
- **Purpose**: 
  - Unambiguous specification using mathematical/logical techniques.
  - Reduce errors in critical systems (e.g., aerospace, medical devices).
- **Key Benefits**:
  - Clarify requirements, remove ambiguity, improve traceability.
  - Early error detection reduces rework costs.
- **Activities**:
  - Write formal specs → Validate (inspect, prove theorems) → Refine to code → Verify implementation.

---

#### **2. Types of Formal Specifications**
- **Model-Oriented**:
  - Constructs a system model using mathematical objects (sets, sequences).
  - Example: Representing a list as nested sets: `<a, b, a>` = `{a, {b, {a, {}}}}`.
- **Property-Oriented**:
  - Describes system behavior through axioms/rules.
  - Example: List operations (`nil`, `cons`, `head`, `tail`) with axioms:
    - `head(cons(x, xs)) = x`
    - `tail(cons(x, xs)) = xs`.

- **Specification Techniques**:
  - **Algebraic**: Focuses on operations and relationships (e.g., Larch, OBJ).
  - **Model-Based**: Uses state models (e.g., Z, VDM, B).

---

#### **3. Key Concepts**
- **Formal Proofs**:
  - Series of logical steps to validate specifications.
  - Example: Proof by contradiction (e.g., proving a book on loan cannot be requested).
- **Model Checking**:
  - Verifies if a system model satisfies desired properties.
- **Abstraction**:
  - Simplifies models to focus on essential properties (e.g., ignoring order in sets).

---

#### **4. Examples**
- **Library System**:
  - **Formalization**:
    - States: `S` (stacks), `R` (reserve), `L` (loaned).
    - Axioms: `S ⇔ ¬(R ∨ L)`, `Q ⇒ (S ∨ R)`.
  - **Theorem**: `L ⇒ ¬Q` (a loaned book cannot be requested).
    - Proof: Assume `L ∧ Q` → Contradiction with `Q ⇒ (S ∨ R)`.
- **Algebraic Specification (List ADT)**:
  ```plaintext
  sort List
  operations: Create, Cons, Head, Tail, Length
  axioms:
    Head(Cons(L, v)) = v if L=Create else Head(L)
    Tail(Cons(L, v)) = Create if L=Create else Cons(Tail(L), v)
  ```
- **Model-Based Specification (Z Notation)**:
  - Schemas define state and operations:
    ```plaintext
    Schema Hopper:
      contents: ℕ
      capacity: ℕ
      danger: ℕ
      light: {on, off}
      axioms: contents ≤ capacity, light = on ⇔ reading ≤ danger
    ```

---

#### **5. Benefits & Applications**
- **Critical Systems**: Air traffic control, medical devices, railway signaling.
- **Cost-Effectiveness**: Early error detection reduces development costs.
- **Formal vs. Informal**:
  - Formal specs are precise, unambiguous, and enable automated analysis.

---

#### **6. Key Differences**
- **Model vs. Property-Oriented**:
  - Model: Builds a structure (e.g., sets).
  - Property: Defines behavior via axioms.
- **Algebraic vs. Model-Based**:
  - Algebraic: Interface-focused (operations/axioms).
  - Model-Based: State-focused (e.g., Z schemas).

---

**Exam Tips**:
- Practice writing algebraic specs (e.g., Stack, AVLTree).
- Understand proof techniques (contradiction, induction).
- Compare Z notation with algebraic methods.
- Memorize examples (Library, Hopper, List ADT).

--- 

**Good Luck!** 🌟