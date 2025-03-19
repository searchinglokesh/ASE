### **Software Design - I: Key Exam Notes**

---

#### **1. Design Phase Overview**  
- **Objective**: Transform **SRS document** into a **Design Document** (implementable in code).  
- **Key Outputs**:  
  - Module structure, control/invocation relationships, interfaces, data structures, algorithms.  
  - **Program Structure (Software Architecture)**: Represented via structure charts, Jackson/Warnier-Orr diagrams.  

---

#### **2. Stages of Design**  
1. **High-Level Design**:  
   - Identifies **modules**, their **control relationships**, and **interfaces**.  
   - Outcome: Tree-like structure chart (software architecture).  
2. **Detailed Design**:  
   - Specifies **data structures** and **algorithms** for each module.  
   - Outcome: **Module specifications**.  

---

#### **3. Characteristics of Good Software Design**  
- **Correctness**: Implements all functionalities accurately.  
- **Understandability**: Easy to comprehend (critical for maintenance).  
- **Efficiency**: Optimizes resource usage.  
- **Maintainability**: Easy to modify.  

---

#### **4. Improving Understandability**  
- **Modularity**:  
  - Decompose into **independent modules** (divide and conquer).  
  - Benefits: Reduced complexity, easier debugging, reusability.  
- **Layering**: Arrange modules hierarchically (tree structure).  

---

#### **5. Cohesion & Coupling**  
| **Concept**       | **Definition**                                  | **Ideal**          |  
|--------------------|------------------------------------------------|--------------------|  
| **Cohesion**       | Functional strength of a module.               | **High Cohesion**  |  
| **Coupling**       | Degree of interdependence between modules.     | **Low Coupling**   |  

**Why Functional Independence (High Cohesion + Low Coupling)?**  
- Reduces error propagation.  
- Enhances reusability.  
- Simplifies maintenance.  

---

#### **6. Types of Cohesion** (Order: Worst to Best)  
1. **Coincidental**: Random tasks (e.g., `Module AAA` with unrelated functions).  
2. **Logical**: Similar operations (e.g., `print` module handling different outputs).  
3. **Temporal**: Tasks executed in same time span (e.g., `init()` for startup).  
4. **Procedural**: Part of a procedure/algorithm (e.g., message decoding steps).  
5. **Communicational**: Operate on same data (e.g., functions on a student array).  
6. **Sequential**: Output of one task is input to the next.  
7. **Functional**: Single function (e.g., payroll management).  

---

#### **7. Determining Cohesion**  
- Describe the module’s function in **one sentence**:  
  - **Compound sentence**: Sequential/communicational cohesion.  
  - Words like *“first,” “then”* → Sequential cohesion.  
  - Words like *“initialize”* → Temporal cohesion.  

---

#### **8. Key Takeaways**  
- **Avoid High Coupling**: Makes modifications difficult.  
- **Aim for Functional Cohesion**: Simplifies understanding and testing.  
- **Design Iteratively**: Refine through multiple steps for robustness.  

---

**Good Luck!** 🚀  
*Focus on examples and diagrams (e.g., structure charts) for exam questions.*