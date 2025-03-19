### Best Notes for ASE Lecture 24: Structured Analysis and Design (DFD Focus)  
**Key Topics:** Balancing DFDs, Numbering, Examples, Data Dictionaries, Guidelines, Errors, Shortcomings  

---

#### **1. Balancing DFDs**  
- **Rule**: Data flowing into/out of a parent bubble must match the data flows in the decomposed child diagram.  
  - *Example*: If Level 1 bubble P3 has input `c` and outputs `d, e`, its Level 2 decomposition must also have `c` as input and `d, e` as outputs.  

---

#### **2. Numbering Bubbles**  
- **Hierarchical Structure**:  
  - Context Diagram: Bubble numbered **0**.  
  - Level 1: Bubbles numbered **0.1, 0.2, 0.3**, etc.  
  - Decomposition: Bubble `x` decomposed into **x.1, x.2, x.3**, etc.  

---

#### **3. Examples**  
- **Tic-Tac-Toe Game**:  
  - **Context Diagram**:  
    - External Entities: Human Player.  
    - Processes: Display game board, accept moves, check win/draw.  
  - **Data Dictionary**:  
    - `move = integer`, `board = {integer}9`, `result = string`.  

- **Trading-House Automation System (TAS)**:  
  - **Key Processes**:  
    - Check credit-worthiness → Validate items → Inventory check → Generate bills/pending orders.  
  - **Data Dictionary**:  
    - `order = customer-id + {items + quantity}*`  
    - `pending-orders = customer-id + {items + quantity}*`  

---

#### **4. Data Dictionary**  
- Defines data elements, structures, and relationships.  
- *Example Entries*:  
  - `bill = {item + quantity + price}* + total-amount + customer-address`  
  - `response = [bill + material-issue-slip, reject-message]`  

---

#### **5. Guidelines for Constructing DFDs**  
- **Context Diagram**:  
  - Only **1 bubble** (system) with all external entities (e.g., Customer, Manager).  
- **Level Decomposition**:  
  - 3–7 bubbles per diagram; decompose further if needed.  
- **Avoid**:  
  - Control flow (e.g., conditional arrows).  
  - External entities in lower-level DFDs.  

---

#### **6. Common Errors**  
- **Unbalanced DFDs**: Mismatched data flows between parent and child diagrams.  
- **Control Flow Representation**: Using arrows to show conditions (e.g., "if-else").  
- **Naming Issues**: Unnamed data flows or using nouns for bubble names (use verbs).  
- **Over-Decomposition**: Too many bubbles at a single level.  

---

#### **7. Shortcomings of DFDs**  
- **Imprecise Functionality**: Labels (e.g., "find-book-position") lack detailed logic (error handling, edge cases).  
- **No Control Information**: Order of execution or conditions not captured.  
- **Subjective Decomposition**: No strict rules for stopping decomposition; analyst judgment required.  

---

#### **8. Tools**  
- **Commercial**: Visio, SmartDraw, Edraw.  
- **Free**: Dia (GNU).  
- **Caution**: Tools aid design but don’t replace analytical skills.  

---

### **Exam Tips**  
- Practice balancing DFDs using the TAS example.  
- Memorize numbering rules and data dictionary syntax.  
- Avoid control flow representation in DFDs.  
- Focus on SRS alignment: Include all required functions, exclude assumptions.  

Good luck! 📚✨