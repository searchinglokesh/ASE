### **Exam Preparation Notes: Requirements Specification & Analysis**

---

#### **1. Decision Trees vs. Decision Tables**  
**Decision Trees**  
- **Structure**:  
  - **Edges** = Conditions.  
  - **Leaf nodes** = Actions.  
- **Use Case**: LMS (Library Membership System) example:  
  - **New Member**: Collect details → Create record → Print bill.  
  - **Renewal**: Validate member → Update expiry date → Print bill.  
  - **Cancel**: Validate → Cancel membership → Print cheque → Delete record.  
   ![[Pasted image 20250319223954.png]]
- **Advantages**: Easy to visualize for small conditions.  

**Decision Tables**  
- **Structure**:  
  - **Upper rows**: Conditions.  
  - **Lower rows**: Actions.  
  - **Columns** = Rules (e.g., "If condition X, then action Y").  
- **Example**:  
  | Conditions           | Rule 1 | Rule 2 | Rule 3 |  
  |----------------------|--------|--------|--------|  
  | Valid Selection      | NO     | YES    | YES    |  
  | New Member           | --     | YES    | NO     |  
  | **Actions**          |        |        |        |  
  | Display Error        | YES    | --     | --     |  
  | Ask Member Details   | --     | YES    | --     |  
- **Advantages**: Covers all condition combinations.  

**Comparison**  
| **Aspect**          | Decision Tree                     | Decision Table                     |  
|----------------------|-----------------------------------|------------------------------------|  
| **Ease of Use**      | Better for small conditions       | Better for complex combinations    |  
| **Visual Clarity**   | Intuitive flowchart               | Tabular structure                  |  

---

#### **2. Formal vs. Semiformal Specifications**  
**Formal Specifications**  
- **Techniques**: Logic, set theory, algebraic specs, finite state machines.  
- **Pros**:  
  - No ambiguity (mathematically precise).  
  - Automated verification.  
- **Cons**:  
  - Steep learning curve.  
  - Struggles with complex systems.  

**Semiformal Specifications**  
- **Examples**:  
  - **SADT**: Structured Analysis and Design Technique (diagrammatic).  
  - **PSL/PSA**: Problem Statement Language/Analyzer (text-based).  
- **Pros**: Balances structure with flexibility.  

**Executable Specifications (4GLs)**  
- **Features**:  
  - Prototype directly from specs (e.g., 4GLs like SQL).  
  - **Pros**: Fast development, reusable components.  
  - **Cons**: Slow execution, limited to functional requirements.  

---

#### **3. Requirements Analysis & SRS Document**  
**Key Objectives**:  
- Gather, clarify, and validate user requirements.  
- Remove inconsistencies.  

**SRS Document Structure**:  
1. **Introduction**: Purpose, scope, audience.  
2. **General Description**:  
   - Product perspective, functions, user characteristics.  
3. **Specific Requirements**:  
   - Functional, performance, design constraints, acceptance criteria.  

**Stakeholders in a Library System**:  
- Library staff, users, technical support, local authorities, suppliers.  

**Success Metrics**:  
- On-time delivery, budget adherence, user certification.  

---

#### **4. Summary & Key Takeaways**  
- **Decision Tools**: Use trees for simplicity, tables for completeness.  
- **Formal Specs**: Precise but complex; semiformal for flexibility.  
- **SRS**: Critical blueprint; includes functional/non-functional requirements.  
- **4GLs**: Enable rapid prototyping but lack efficiency.  

---

**Exam Focus Areas**:  
- LMS workflow (decision tree example).  
- Differences between decision trees/tables.  
- Pros/cons of formal specs.  
- SRS structure and stakeholders.  

Good luck! 📚✨