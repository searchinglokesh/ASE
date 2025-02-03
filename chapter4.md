# Software Cost Estimation Techniques - Exam Notes

## Key Parameters to Estimate
- Size of software
- Effort required
- Project duration
- Total cost

## Software Cost Components
- Hardware and software costs
- Travel costs
- Effort costs (e.g., salaries)
- Overheads (building, light, heating)
  - Typically as much as effort costs

## Estimation Methods Taxonomy
1. **Top-down vs Bottom-up Approaches**
2. **Estimation Techniques**
   - Parametric/Algorithmic models
   - Expert opinion
   - Analogy-based methods
   - Price to win

## Project Size Metrics
### 1. Source Lines of Code (SLOC)
- Conceptually simple
- Limitations:
  - Programmer-dependent
  - Does not consider code complexity

### 2. Function Points (FP)
- Preferred over SLOC
- Advantages:
  - Independent of language, tools, methodologies
  - Can be estimated early in analysis/design
  - Based on user's external view of system

## Counterintuitive Productivity Observations
- Lower-level languages: More code, potentially more productive
- More verbose programmers might show higher productivity

## Expert Judgment Techniques
### Basic Methods
- Basic expert judgment
- Weighted average estimating
- Consensus estimating
- Delphi Method

### Delphi Estimation
**Process:**
- Team of experts and a coordinator
- Independent estimation
- Multiple estimation rounds
- Experts never meet directly

**Pros:**
- Potentially accurate
- Relatively simple

**Cons:**
- Hard to document expert factors
- Potential bias
- Dependence on expert experience

## Algorithmic/Parametric Models (e.g., COCOMO)
### Advantages
- Repeatable estimations
- Easy to modify and customize
- Efficient

### Limitations
- Cannot easily quantify exceptional conditions
- Sensitive to sizing and cost driver ratings

## Function Point Analysis (Albrecht/IFPUG)
### 5 Key Components
1. External Inputs
2. External Outputs
3. External Inquiries
4. Internal Logical Files
5. External Interface Files

### Calculation
- Unadjusted Function Points
- Value Adjustment Factor (VAF)
  - 14 general system characteristics
  - 0 = no influence
  - 5 = strong influence

## Exam Tips
- Understand the pros and cons of different estimation techniques
- Know the details of Function Point Analysis
- Be prepared to explain the Delphi method
- Recognize the limitations of traditional metrics like SLOC
