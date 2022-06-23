## Encapsulating EF Core 6 Usage
- by Vladimir Khorikov
- The usage of EF Core 6 is a vast and complicated topic. This course will teach you how to do this in a way that maintains proper encapsulation and abstraction.

- OVERVIEW:
  - C# Programming language. EF Core.

- UNDERSTANDING ENCAPSULATION & ABSTRACTION:
  - Encapsulation:
    - Interconnected with abstraction. Different principles.
    - Protecting data integrity. Help to enforce invariants so that they are never violated.
    - "Information hiding." Less risk of corrupting the class internals.
    - "Bundling of data & operations together." Perform integrity checks before modifying data.
    - e.g.:
    ```csharp
      public class Triangle
      {
        public IEnumerable<Edge> Edges { get; }
        public Triangle(IEnumerable<Edge> edges) => Edges = edges;
      }
    ```
    - NOTE: Add guard clause. e.g.: edges.Length = 3.
    - Encapsulation is highly related to the notion of a rich domain model.
  - Abstraction:
    - The amplification of the essential (the current task) and the elimination of the irrelevant (all other tasks.)
    - Programming guidelines limit the growth of complexity. Abstractions help focus on a single task.
    - In the general sense, abstract classes and interfaces are not abstractions.
    - A good abstraction allows one to focus on a single application concern. Bad? You need to consider nmultiple concerns.
    - Abstraction = Single responsibility principle. Abstractions can form heirarchies. Build complex logic nd easily as simple logic.
    - Allows to express complex ideas in code as easily as simplistic ideas.
      1. Amplify the essential: WHAT the coe does.
      2. Elimate the irrelevant: HOW the code performs said task.
  - Differences between:
    - Encapsulation: Data consistency. Save cycles on figuring out if an operation is legal.
    - Abstraction: Amplification of essential & elimination of irrelevant. Focus on a single task. What's. Not how's.
  - Summary:
    - Encapslation: Act of protecting data integrity.
      - Information hiding. Bundling dara & operations together.
      - Helps reduce the mental burden required to maintain data consistency.
    - Abstraction: Amplification of the essential & elimination of the irrelevant.
      - Helps focus on one task at a time.
      - Helps focus on what's (intent,) and not how's (implementation details.)
      - Abstractions can form heirchies, helping to express complex ideas just as easily as simple ideas.

- ENCAPSULATION THE DB CONTEXT:
  - 
  
- THE GREAT REPOSITORY DEBATE:
- AVOIDING COMMON ANTI-PATTERNS:
- CHOOSING BETWEEN IQUERABLE & IENUMERABLE:
