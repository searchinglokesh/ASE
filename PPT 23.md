### **Structured Analysis & Design Exam Notes**

---

#### **1. Overview of Structured Analysis (SA) & Structured Design (SD)**
- **Structured Analysis**:
  - **Top-down decomposition** technique using **Data Flow Diagrams (DFDs)**.
  - Focuses on **functional requirements** exploration and validation.
  - Converts textual problem descriptions into **graphical models (DFDs)**.
  - **Key Principle**: Divide and conquer (decompose functions hierarchically).

- **Structured Design**:
  - Maps DFD functions to a **module structure (software architecture)**.
  - Aims for a form suitable for implementation (e.g., in C).

- **SA vs. Object-Oriented (OO) Design**:
  | **SA/SD**               | **OO Design**               |
  |--------------------------|------------------------------|
  | Top-down approach        | Bottom-up approach           |
  | Uses DFDs                | Uses UML                     |
  | Coded in C               | Coded in Java, C++, C#       |
  | Focus on functions       | Focus on objects/classes     |

---

#### **2. Data Flow Diagrams (DFDs)**
- **Purpose**: Model system functionalities, data flow, and interactions.
- **Key Symbols**:
  - **External Entity**: Rectangle (e.g., user, external system).
  - **Process/Bubble**: Circle (e.g., "search-book").
  - **Data Flow**: Directed arrow (annotated with data name).
  - **Data Store**: Symbol for logical/physical data storage (e.g., book-details).

- **DFD Levels**:
  1. **Context Diagram (Level 0)**: Single bubble representing the entire system with external entities.
  2. **Level 1 DFD**: Decomposes Level 0 into 3–7 high-level processes.
  3. **Lower Levels**: Further decompose each process until simple algorithms describe them.

- **Rules**:
  - **Decomposition**: 3–7 bubbles per level. Avoid <3 (redundant) or >7 (complexity).
  - **Synchronous vs. Asynchronous**:
    - Direct data flow (synchronous).
    - Data store connection (asynchronous).

---

#### **3. Hierarchical Decomposition**
- **Process**:
  1. Start with **context diagram**.
  2. Break into subfunctions (Level 1, Level 2, etc.).
  3. Stop decomposition when a process can be coded with a simple algorithm.

- **Example**: RMS Calculating Software
  - **Context Diagram**: Accepts 3 integers → outputs RMS.
  - **Level 1 DFD**:
    - Validate inputs → Calculate squares → Sum squares → Compute RMS → Display result.

---

#### **4. Data Dictionary**
- **Purpose**: Define all data items in DFDs to ensure consistency.
- **Key Operators**:
  - `+`: Composition (e.g., `a+b`).
  - `[]`: Selection (e.g., `[RMS, error]`).
  - `()`: Optional data (e.g., `a+(b)`).
  - `{}`: Iteration (e.g., `{name}*` for 0+ instances).
  - `=`: Equivalence (e.g., `grossPay = regularPay + overtimePay`).

- **Example Entry (RMS Software)**:
  ```plaintext
  numbers = valid-numbers = a + b + c
  a: integer  *input number*
  Result = [RMS, error]
  RMS: integer  *root mean square*
  error: string  *error message*
  ```

- **Importance**:
  - Avoids terminology conflicts.
  - CASE tools automate data dictionary management (e.g., queries, RDBMS storage).

---

#### **5. Key Considerations**
- **Pros of DFDs**:
  - Simple symbols/rules → Easy for non-technical stakeholders.
  - Hierarchical model manages cognitive complexity.
- **Pitfalls**:
  - Poor decomposition (too few/many bubbles).
  - Manual data dictionaries → error-prone (use CASE tools).

---

#### **6. SA/SD Methodologies**
- **Major Contributors**:
  - Constantine & Yourdon
  - Gane & Sarson
  - Hatley & Pirbhai
  - DeMarco & Yourdon

---

### **Summary for Quick Revision**
- **SA**: Top-down, DFDs, functional decomposition.
- **SD**: Maps DFDs to modules.
- **DFD Symbols**: External entity, process, data flow, data store.
- **Decomposition**: 3–7 bubbles per level.
- **Data Dictionary**: Ensures data consistency; uses CASE tools.
- **SA vs. OO**: Top-down vs. bottom-up, DFDs vs. UML, C vs. Java/C++.

**Good Luck!** 🌟