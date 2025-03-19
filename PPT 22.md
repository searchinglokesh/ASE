### **Best Notes for Exam Preparation: Software Design - II**

---

#### **1. Coupling**  
- **Definition**: Degree of interdependence between two modules.  
- **Types** (Low to High Coupling):  
  - **Data Coupling**: Communicates via parameters (elementary data items).  
  - **Stamp Coupling**: Communicates via composite data (e.g., arrays/structures).  
  - **Control Coupling**: Data directs execution flow (e.g., flags).  
  - **Common Coupling**: Shares global data.  
  - **Content Coupling**: Shares code (e.g., branching into another module).  
- **Key Point**: Aim for **low coupling** (data/stamp) for better modularity.

---

#### **2. Cohesion**  
- **Definition**: How well a module’s elements work together to achieve a single task.  
- **High Cohesion**: Good (module performs one task).  
- **Low Cohesion**: Bad (module handles multiple tasks).  

---

#### **3. Hierarchical Design**  
- **Structure Chart**: Tree-like diagram showing module organization.  
- **Key Metrics**:  
  - **Depth**: Number of control levels.  
  - **Width**: Span of control at a level.  
  - **Fan-out**: Modules directly controlled by a module. **High fan-out = Bad** (indicates low cohesion).  
  - **Fan-in**: Modules invoking a module. **High fan-in = Good** (code reuse).  
- **Layering Principle**: Modules can only call modules immediately below them.  
- **Abstraction**:  
  - Lower-level modules handle I/O.  
  - Upper-level modules manage workflows.  

---

#### **4. Function-Oriented Design (FOD)**  
- **Approach**:  
  - System = Set of functions.  
  - **Top-down decomposition**: Refine high-level functions into sub-functions.  
  - Centralized system state (global data accessible to all functions).  
- **Examples**:  
  - **Structured Design** (Constantine & Yourdon).  
  - **Fire Alarm System (FOD)**: Uses global arrays (`detector_status`, `alarm_status`) and functions (`ring_alarm`, `reset_alarm`).  

---

#### **5. Object-Oriented Design (OOD)**  
- **Approach**:  
  - System = Collection of **objects** (real-world entities).  
  - **Decentralized state**: Each object manages its own data.  
  - **Encapsulation**: Data + methods within objects.  
  - **Message Passing**: Objects communicate via methods.  
- **Examples**:  
  - **Fire Alarm System (OOD)**: Classes `detector` (attributes: status, location) and `alarm` (methods: `ring_alarm`, `reset_alarm`).  

---

#### **6. FOD vs OOD**  
| **Aspect**              | **Function-Oriented**               | **Object-Oriented**                 |  
|-------------------------|-------------------------------------|-------------------------------------|  
| **Basic Unit**           | Functions (verbs)                   | Objects (nouns)                     |  
| **State Management**     | Centralized global data             | Decentralized (per object)          |  
| **Design Focus**         | Grouping functions by hierarchy     | Grouping functions by data they use |  
| **Example**              | `update-employee-record` function   | `Employee` class with methods       |  

- **Key Quote**:  
  - *“Identify verbs for procedural design, nouns for OOD.” – Grady Booch*  

---

#### **7. Key Design Principles**  
- **Low Coupling + High Cohesion**: Ensure modules are independent and focused.  
- **High Fan-in**: Encourages code reuse.  
- **Layered Design**: Follow abstraction to avoid lower modules calling higher ones.  

---

#### **8. Example Summary**  
- **Fire Alarm System**:  
  - **FOD**: Global arrays + functions manipulate data.  
  - **OOD**: Objects (`detector`, `alarm`) encapsulate data and methods.  

---

**Good Luck!** Focus on understanding coupling types, cohesion, FOD/OOD differences, and design metrics (fan-in/out). Use examples to reinforce concepts! 🚀