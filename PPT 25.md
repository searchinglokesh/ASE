### **Structured Analysis & Design - Key Notes for Exam**

---

#### **1. Structured Design Overview**
- **Aim**: Transform DFD (Data Flow Diagram) into a **Structure Chart** representing software architecture.
- **Structure Chart** shows:
  - Modules and their dependencies.
  - Parameters passed between modules.
  - **No procedural details** (e.g., how functionality is achieved).

---

#### **2. Structure Chart Components**
- **Modules**: Represented by **rectangular boxes** with module names.
- **Control Flow**: Arrows indicate module invocation direction.
- **Data Flow**: Arrows show data passed between modules.
- **Library Modules**: Double-edged rectangles (used by multiple modules).
- **Selection**: Diamond symbol (conditional invocation of modules).
- **Repetition**: Loop around arrows (repeated module calls).
- **Root Module**: Single top-level module; hierarchical layers with no circular dependencies (e.g., Module A → B, but B ↛ A).

---

#### **3. Structure Chart Principles**
- **Abstraction**: Lower-level modules cannot invoke higher-level ones.
- **Layered Design**: Modules arranged in levels for clarity and maintainability.
- **Shortcomings**:
  - Does not show **order** of module invocation.
  - Does not indicate **frequency** of module calls.

---

#### **4. Flow Chart vs. Structure Chart**
| **Feature**         | **Flow Chart**                | **Structure Chart**               |
|----------------------|-------------------------------|------------------------------------|
| **Focus**            | Control flow in a system      | Module hierarchy and interaction  |
| **Data Interchange** | Not represented               | Explicitly shown via data arrows  |
| **Ordering**         | Sequential tasks emphasized   | Order suppressed                  |
| **Modules**          | Hard to identify              | Clearly defined modules           |

---

#### **5. DFD → Structure Chart Strategies**
##### **A. Transform Analysis**
- **Steps**:
  1. Divide DFD into 3 parts:
     - **Afferent Branch**: Input processing (physical → logical).
     - **Central Transform**: Core processing (e.g., calculations, validations).
     - **Efferent Branch**: Output processing (logical → physical).
  2. Create modules for each part; refine by **factoring** (adding submodules like error handling, initialization).
- **Example**: RMS Calculator:
  - *Afferent*: Read & validate numbers.
  - *Central Transform*: Calculate RMS.
  - *Efferent*: Display result.

##### **B. Transaction Analysis**
- Used for **transaction-driven systems** (e.g., menu-driven apps).
- **Steps**:
  1. Identify transactions (input triggers, e.g., order type).
  2. Create a **transaction center** module to route to specific transaction modules.
- **Example**: Tic-Tac-Toe Game:
  - Handle moves, check win/draw conditions, update board.

---

#### **6. Key Concepts**
- **Factoring**: Breaking modules into subcomponents (e.g., read/write modules, error handling).
- **Good Design**: Hierarchical, layered, no circular dependencies.
- **CASE Tools**: Support DFD balancing, data dictionary maintenance.

---

#### **7. Examples**
- **RMS Calculator**:
  - Modules: Read, Validate, Calculate, Display.
- **Tic-Tac-Toe**:
  - Modules: Handle player moves, Check win/draw, Update board.

---

#### **8. Summary**
- **SA/SD Methodology**:
  - **Structured Analysis**: Focuses on DFDs.
  - **Structured Design**: Focuses on Structure Charts.
- **DFDs** are popular for simplicity; CASE tools automate checks.

---

**Exam Tips**:  
- Memorize symbols in structure charts (e.g., diamond = selection).  
- Differentiate Transform vs. Transaction Analysis with examples.  
- Practice drawing structure charts for simple systems (e.g., ATM, library system).  

Good luck! 🚀