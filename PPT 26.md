### **UML & Object-Oriented Design (OOD) Exam Notes**  
**Key Concepts**:  
- **UML** (Unified Modeling Language):  
  - ISO standard (2004).  
  - A **modeling language** (not a methodology) to document OO analysis/design.  
  - Standardizes notations from methodologies like OMT, Booch, OOSE.  
  - Managed by **OMG** (Object Management Group).  

---

### **UML Diagrams & Views**  
**Five Views of a System**:  
1. **User’s View**: Use Case diagrams.  
2. **Structural View**: Class, Object, Component, Deployment diagrams.  
3. **Behavioral View**: Sequence, Collaboration, State Chart, Activity diagrams.  
4. **Implementation View**: Component diagrams.  
5. **Environmental View**: Deployment diagrams.  

**Structural Diagrams**:  
- **Class Diagram**: Classes, relationships (inheritance, association).  
- **Object Diagram**: Instances of classes.  
- **Component Diagram**: Logical groupings (e.g., modules).  
- **Deployment Diagram**: Hardware nodes hosting components.  

**Behavioral Diagrams**:  
- **Use Case Diagram**: High-level system behaviors (user goals).  
- **Sequence Diagram**: Time-ordered message flow.  
- **Collaboration Diagram**: Object structure and messages.  
- **State Chart Diagram**: State changes (event-driven).  
- **Activity Diagram**: Workflow between activities.  

---

### **Practical Tips for UML Usage**  
- **Simple Systems**: Focus on **Use Case**, **Class**, and **one interaction diagram** (Sequence/Collaboration).  
- **State Chart**: Only if a class has **significant states** (e.g., ATM states: idle, processing).  
- **Deployment Diagram**: Needed for systems with **multiple hardware components**.  

**Quotes to Remember**:  
- *“UML is a large beast, but you don’t need all of it.”* – **Martin Fowler**  
- *“Use constructs relevant to your phase (analysis vs. design).”* – **Brian Henderson-Sellers**  

---

### **Use Case Modeling**  
**Purpose**:  
- Central model for requirements; defines **external behavior** without internal details.  
- Identifies **actors** (users, external systems) and their goals.  

**Elements**:  
- **Use Case**: Ellipse (e.g., *Issue Book* in a Library System).  
- **Actor**: Stick figure (e.g., *Customer*, *Clerk*).  
- **System Boundary**: Rectangle enclosing use cases.  
- **Relationships**:  
  - **Association**: Line between actor and use case.  
  - **Include**: Reusable behavior (e.g., *Validate User*).  
  - **Extend**: Optional behavior (e.g., *Gift Wrap* in *Perform Sale*).  
  - **Generalization**: Inheritance (e.g., *Pay via Credit Card* inherits from *Pay Membership Fee*).  

**Example**:  
**Video Store System** Use Cases:  
- Maintain Customers, Rent/Return Videos, Generate Reports.  
- *Search for Videos* is `<<include>>`d in multiple use cases.  

---

### **Use Case Description Template**  
1. **Name**: e.g., *ATM Withdraw Money*.  
2. **Actors**: Customer.  
3. **Preconditions**: ATM is ready, has cash/paper.  
4. **Postconditions**: Account balance updated, receipt printed.  
5. **Mainline Scenario**:  
   - Steps: Insert card → Enter PIN → Select amount → Dispense cash → Eject card.  
6. **Alternative Flows**:  
   - Authorization failed → Display error.  
   - Insufficient funds → Cancel transaction.  
7. **Exceptional Flows**: Power failure → Cancel transaction.  

---

### **Key Examples to Remember**  
1. **Library System**:  
   - Use Cases: *Issue Book*, *Return Book*, *Check Reservation* (`<<include>>`).  
2. **ATM Withdrawal**:  
   - Scenarios: Main success path vs. error handling (e.g., invalid PIN).  

---

### **Exam Focus Areas**  
- **Diagrams vs. Views**: Know which diagrams belong to which view.  
- **Use Case Relationships**: Differentiate *Include*, *Extend*, *Generalization*.  
- **Scenario Writing**: Pre/Post conditions, main/alternative flows.  
- **Diagram Symbols**: Actor (stick figure), Use Case (ellipse), system boundary (rectangle).  

**Mnemonic**: **I SEE UML**  
- **I**nclude, **E**xtend, **G**eneralization for Use Cases.  
- **S**tructural vs. **B**ehavioral diagrams.