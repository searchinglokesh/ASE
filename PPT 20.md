### **Best Notes for Petri Nets Exam Preparation**

---

#### **1. Behavioral vs. Structural Properties**
- **Behavioral Properties**: Depend on initial marking (e.g., reachability, liveness).
- **Structural Properties**: Independent of initial marking (e.g., structural liveness, conservativeness).

---

#### **2. Key Behavioral Properties**
1. **Reachability**  
   - \( M_n \) is reachable from \( M_0 \) if a firing sequence \( \sigma \) transforms \( M_0 \) to \( M_n \).  
   - **Reachability Set**: \( R(M_0) \).  
   - **Problem**: Decidable but exponential. Equality of languages (\( L(N, M_0) \)) is undecidable.  

2. **Boundedness**  
   - **k-bounded**: No place exceeds \( k \) tokens in any \( M \in R(M_0) \).  
   - **Safe**: 1-bounded (critical for buffers/registers).  

3. **Liveness**  
   - **Levels**:  
     - **L0 (Dead)**: Never fires.  
     - **L1 (Potentially firable)**: Fires at least once.  
     - **L4 (Live)**: Always firable from any \( M \in R(M_0) \).  
   - A net is **Lk-live** if all transitions are Lk-live.  

4. **Reversibility & Home State**  
   - **Reversible**: \( M_0 \) is reachable from all \( M \in R(M_0) \).  
   - **Home State**: A marking \( M' \) reachable from all \( M \in R(M_0) \).  

5. **Coverability**  
   - \( M \) is coverable if \( \exists M' \geq M \) in \( R(M_0) \).  
   - **Link to L1-liveness**: \( t \) is L1-live iff its enabling marking is coverable.  

6. **Persistence**  
   - Firing a transition does not disable others.  
   - Safe persistent nets can be transformed into marked graphs.  

7. **Synchronic Distance**  
   - Measures dependence between transitions:  
     \( d_{ij} = \max |\sigma(t_i) - \sigma(t_j)| \) over all firing sequences \( \sigma \).  

8. **Fairness**  
   - **B-fair**: Bounded difference in firings between transitions.  
   - **Unconditional Fairness**: All transitions fire infinitely often in infinite sequences.  
   - **Relationship**: B-fair ⇒ Unconditionally fair (and vice versa for bounded nets).  

---

#### **3. Structural Properties**
1. **Structural Liveness**: Exists a live initial marking.  
2. **Controllability**: Any marking reachable from any other.  
3. **Structural Boundedness**: Bounded for all \( M_0 \).  
4. **Conservativeness**: Weighted token sum \( M^T y = \text{constant} \).  
5. **Repetitiveness**: Infinite firing of transitions.  
6. **Consistency**: Cyclic behavior with all transitions firing.  
7. **Structural B-fairness**: B-fair for any \( M_0 \).  

---

#### **4. Subclasses of Petri Nets**
1. **State Machine (SM)**  
   - Each transition has **1 input and 1 output place**.  
   - No synchronization.  

2. **Marked Graph (MG)**  
   - Each place has **1 input and 1 output transition**.  
   - No conflicts.  

3. **Free-Choice (FC)**  
   - Shared input places imply identical output transitions.  
   - No confusion (asymmetric/symmetric).  

4. **Extended Free-Choice (EFC)**  
   - \( p_1 \bullet = p_2 \bullet \) if they share an output transition.  

5. **Asymmetric Choice (AC)**  
   - \( p_1 \bullet \subseteq p_2 \bullet \) or vice versa if overlapping.  
   - Allows asymmetric confusion.  

---

#### **5. Key Relationships**
- **Boundedness, Liveness, Reversibility**: Independent (e.g., a net can be bounded but not live).  
- **Synchronic Distance**: Example: \( d_{12} = 1 \), \( d_{13} = \infty \).  
- **Structural B-fairness**: Equivalence relation; strongly connected MGs are structurally B-fair.  

---

#### **6. Formal Definition**
A Petri net is a 5-tuple: \( PN = (P, T, F, W, M_0) \), where:  
- \( P \): Set of places.  
- \( T \): Set of transitions.  
- \( F \subseteq (P \times T) \cup (T \times P) \): Flow relation.  
- \( W \): Arc weights.  
- \( M_0 \): Initial marking.  

---

#### **7. Key Diagrams & Examples**
- **Bounded vs. Safe**: 2-bounded vs. 1-bounded.  
- **Live vs. Non-live**: Dead transitions (L0) vs. live transitions (L4).  
- **Subclass Venn Diagram**: SMs ⊂ FCs ⊂ EFCs ⊂ ACs.  

---

**Exam Tips**:  
- Focus on definitions, differences (e.g., SM vs. MG), and relationships (e.g., B-fair ⇒ Unconditional fair).  
- Practice calculating synchronic distance and identifying subclass constraints.  
- Memorize key theorems (e.g., coverability ⇔ L1-liveness).  

Good luck! 🚀