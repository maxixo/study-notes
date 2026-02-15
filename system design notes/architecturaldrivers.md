1. The Challenge of Scope and Ambiguity
Designing a large-scale system involves a much higher level of abstraction than implementing a single method or algorithm 1.

Degrees of Freedom: In small tasks, inputs and outputs are often predefined. In system design, the range of possible solutions is massive, which can feel overwhelming 1, 2.

Defining the Solution: Requirements often come from non-technical stakeholders who only understand the problem, not the technical needs 3, 4.

The Power of Questions: Asking clarifying questions (e.g., "Is this a mobile or desktop experience?") is actually considered part of the design solution because it narrows down the infinite possibilities into a concrete plan 5.

2. Why Upfront Requirements are Critical
While small codebases can be refactored easily, large-scale systems represent a massive investment that is difficult to change "overnight" 6.
Resource Intensive: These projects often require multiple teams and months of engineering time 6.
Financial & Legal Weight: Organizations may have to purchase expensive hardware or software licenses upfront and enter into legally binding contracts with time commitments 6.
Reputational Risk: Failing to deliver a functional system on time can cause "irreversible damage" to a company’s brand and image 7.


3. The Three "Architectural Drivers"
The sources classify requirements into three categories that "drive" the final architectural decisions 8:
Functional Requirements (Features): These describe what the system does (e.g., "the system must display a map with nearby drivers") 9, 10. While important, functional requirements alone do not determine architecture, as many different designs can achieve the same feature 11.
Quality Attributes (Non-functional Requirements): These are properties the system must have, such as scalability, availability, reliability, and security 12. Crucially, these attributes are what actually dictate the software architecture 13.
System Constraints: These are the external boundaries, such as strict deadlines, limited budgets, or small team sizes 13. These constraints often force architects to make trade-offs and sacrifices they wouldn't otherwise choose 8, 13.


