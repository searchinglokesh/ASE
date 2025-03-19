**Formal Specification Notes: Timing Constraints**  
*Based on Dr. Sangharatna Godboley's PPT*  

---

### **Key Concepts**  
1. **Timing Constraints**:  
   - Expressed via **events** (stimuli/responses) that can be instantaneous or durational.  
   - **Two Types**:  
     - **Performance Constraints**: System response limitations (e.g., response time).  
     - **Behavioral Constraints**: Environment/user action limitations (e.g., input timing).  

---

### **Finite State Machines (FSMs)**  
- Model systems with **states**, **transitions**, and **events**.  
- **Components**:  
  - States, input/output symbols, transition function.  
  - **Moore Machine**: Output depends on the *state*.  
  - **Mealy Machine**: Output depends on the *transition*.  

**Example (Phone System)**:  
- States: *Await first digit*, *Await second digit*, etc.  
- Transitions: Triggered by events (e.g., *First digit* starts a timer).  
- **Timer Alarms**: Artificial stimuli to enforce timing constraints (e.g., 20-second limit between digits).  

---

### **Types of Timing Constraints**  
1. **Maximum Constraints**:  
   - **S-S (Stimulus-Stimulus)**: Max time between two stimuli (e.g., 20s between dialing digits).  
   - **S-R (Stimulus-Response)**: Max time for system response (e.g., dial tone within 20s of off-hook).  
   - **R-S (Response-Stimulus)**: Max time for next stimulus after response.  
   - **R-R (Response-Response)**: Max time between two responses (e.g., 0.5s delay between ring tones).  

2. **Minimum Constraints**:  
   - **S-S**: Min time between stimuli (e.g., 0.5s between digits).  
   - **Behavioral Impact**: System must handle violations (e.g., beep if user dials too fast).  

3. **Durational Constraints**:  
   - Event must last a specific duration (e.g., hold button for 15–30s to reach operator).  

---

### **FSM Representation Examples**  
1. **Maximum S-R Constraint**:  
   - *Offhook* → Start timer(20) → If timer expires, trigger *Alarm/Dial tone*.  
2. **Minimum S-S Constraint**:  
   - Dialing digits too fast triggers *beeping* and resets the timer.  
3. **Durational Constraint**:  
   - Pressing a button for 15s/30s/45s leads to different outcomes (e.g., local/international operator).  

---

### **Summary & Challenges**  
- **Formal Specification Pros**: Precision, unambiguous requirements.  
- **Cons**: Complexity, steep learning curve.  
- **Timing Constraints in FSMs**: Use timers and state transitions to model deadlines, durations, and delays.  
- **Key References**: Somerville (Ch. 10), Mall (Ch. 3), Dasarathy’s IEEE paper (1985).  

---

**Next Lecture**: Real-time system design with Ward and Mellor’s structured analysis.  

---  
**Exam Focus**: Understand FSM diagrams, constraint types (max/min/durational), and how timers enforce timing rules. Practice converting scenarios (e.g., phone systems) into FSMs with constraints.