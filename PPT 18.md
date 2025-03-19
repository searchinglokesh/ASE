### **Petri Nets (PN) - Exam Notes**  
*(Based on ASE-Lecture18.pdf)*  

---

#### **1. Introduction**  
- **Origin**: Introduced by Carl Adam Petri (1960s).  
- **Applications**: Telecommunication, software engineering, transportation. Now recognized in reliability engineering (IEC 61508, 62551).  
- **Purpose**: Model system states, transitions, and dynamic behavior for reliability analysis.  

---

#### **2. Basic Concepts**  
- **Nodes**:  
  - **Places (Circles)**: Represent *states* (e.g., functioning, failed).  
  - **Transitions (Bars)**: Represent *events* (e.g., failure, repair).  
  - **Arcs**: Directed connections between places and transitions.  
- **Tokens**: Black dots in places indicating the current state. A PN with tokens is a *marked PN*.  
- **Firing**: Movement of tokens from input to output places via transitions.  

##### **Key Rules**:  
- **Enabling Condition**: A transition fires if input places have ≥ tokens matching the arc’s **multiplicity** (default=1 if unspecified).  
- **Inhibitor Arcs**: Block transitions if input places have ≥ tokens (denoted by a small circle on the arc).  

##### **Transition Types**:  
| Type          | Description                          | Distribution       |  
|---------------|--------------------------------------|--------------------|  
| Immediate     | Fires instantly when enabled.        | -                  |  
| Timed         | Fires after a delay.                 | Deterministic/Stochastic |  
| Stochastic PN (SPN) | All transitions are stochastic.      | Exponential/Geometric |  
| Generalized SPN (GSPN) | Mixes immediate and timed transitions. | Exponential only. |  

---

#### **3. Modeling with PN**  
##### **Failure Modes (e.g., DU/DD Failures)**:  
- **Working States**:  
  - \( P_{UW} \): No Dangerous Undetected (DU) failure.  
  - \( P_{DW} \): No Dangerous Detected (DD) failure.  
  - \( P_{SW} \): System working (no DU/DD failures).  
- **Failed States**:  
  - \( P_{UF} \): DU failure present.  
  - \( P_{DF} \): DD failure present.  
  - \( P_{SF} \): System failed (DU or DD).  
- **Transitions**:  
  - \( t_{DU} \): DU failure (rate \( \lambda_{DU} \)).  
  - \( t_{DD} \): DD failure (rate \( \lambda_{DD} \)).  

##### **Voted Systems**:  
- **Non-Repairable 1002 System**:  
  - Fails when both channels fail.  
  - Transitions: \( t_{1F} \), \( t_{2F} \) (channel failures), \( t_{SF} \) (immediate system failure).  
- **Repairable 1002 System**:  
  - Adds repair transitions \( t_{1R} \), \( t_{2R} \) (rates \( \mu_{1R} \), \( \mu_{2R} \)).  

##### **Fault Tree Gates**:  
- **OR Gate**: Fires if any input place has a token.  
- **AND Gate**: Fires only if all input places have tokens.  

---

#### **4. Advanced Modeling Techniques**  
- **Modularization**: Split PN into intrinsic (item behavior) and extrinsic (system-level links) modules.  
- **Predicates & Assertions**:  
  - **?? (Predicates)**: Conditions (e.g., `??nb_p4 > 0` checks token count).  
  - **!! (Assertions)**: Assign values (e.g., `!!A = In.C1` links local state to global).  
- **RBD-Driven PN**: Combines reliability block diagrams with PN modules for system-level analysis.  

---

#### **5. Analysis Tools & Metrics**  
- **Tools**: SHARPE, GRIF, MATLAB.  
- **Availability**: For repairable systems, calculate time spent in \( p_{SW} \) (working) vs. \( p_{SF} \) (failed).  

---

#### **6. Pros and Cons of PN**  
| **Pros**                          | **Cons**                          |  
|-----------------------------------|-----------------------------------|  
| Visual and intuitive modeling.    | Complexity increases with system size. |  
| Supports concurrency and timing.  | Requires software for analysis.   |  
| Aligns with IEC standards.        | Steep learning curve for advanced features. |  

---

**Key Takeaways**:  
- Master definitions of places, transitions, tokens, and firing rules.  
- Understand how to model DU/DD failures, voted systems, and fault trees.  
- Familiarize with tools (e.g., SHARPE) and metrics (availability).  
- Practice drawing PNs for AND/OR gates and inhibitor arcs.  

Good luck! 📚🔍