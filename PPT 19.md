### Exam Notes: Petri Nets (Based on Lecture 19)

#### **1. Introduction**  
- **Inventor**: Carl Adam Petri (1962).  
- **Purpose**: Model concurrency, synchronization in distributed systems; visual tool with strong mathematical foundation.  
- **Comparisons**: Similar to State Transition Diagrams (STDs) but better suited for concurrent processes.  

---

#### **2. Basic Elements**  
- **Places**: Circles representing system states.  
- **Transitions**: Rectangles representing events/actions.  
- **Arcs**: Arrows connecting places to transitions or vice versa.  
- **Tokens**: Black dots in places denoting current state(s).  

---

#### **3. How Petri Nets Work**  
- **Firing Rules**:  
  - A transition is **enabled** if all input places have sufficient tokens.  
  - Firing removes tokens from input places and adds tokens to output places.  
  - Example: In EFTPOS system, entering digits and pressing "OK" triggers transitions.  

---

#### **4. Key Concepts**  
- **Concurrency**: Multiple transitions fire independently (e.g., waiter serving two customers in a restaurant).  
- **Synchronization**: Transitions requiring tokens from multiple places (e.g., vending machine needing coins).  
- **Non-determinism**: Conflicts/choices (e.g., selecting between two actions).  

---

#### **5. Behavioral Properties**  
1. **Reachability**: Can the system reach a specific state?  
2. **Boundedness**: Ensures no overflow of tokens in places (e.g., limited buffer capacity).  
3. **Liveness**: Guarantees the system won’t deadlock.  

---

#### **6. Examples**  
- **EFTPOS System**:  
  - **Normal Scenario**: 4 digits + OK.  
  - **Exceptional Scenario**: 3 digits + OK (highlighting token movement).  
- **Vending Machine**:  
  - Scenarios for 15c/20c snacks using 5c/10c coins (no change).  
- **Restaurant**:  
  - Two scenarios showing concurrency (waiter serving customers in different orders).  

---

#### **7. Petri Net Structures**  
- **Sequences**: Linear flow of transitions.  
- **Concurrency**: Parallel execution (e.g., serving multiple customers).  
- **Conflict/Choice**: Non-deterministic paths (e.g., selecting a snack).  
- **Synchronization**: Combining multiple inputs (e.g., coins required for a snack).  

---

#### **8. Advanced Petri Nets**  
- **High-Level Nets**: Tokens have "colors" (complex data).  
- **Timed Nets**: Delays in transitions/places (fixed or intervals).  
- **Stochastic Nets**: Random delays (exponential distribution).  
- **Object-Oriented Nets**: Tokens as objects with methods/attributes.  

---

#### **9. Key Takeaways**  
- Petri nets excel in modeling **concurrent systems** with mathematical rigor.  
- Tokens represent state changes; transitions model actions.  
- Understand **reachability, boundedness, liveness** for system validation.  
- Examples (EFTPOS, vending machine, restaurant) illustrate real-world applications.  

**Exam Tip**: Practice drawing Petri nets for given scenarios and analyze token movements!