# [Building Resilient FE Architecture](https://www.youtube.com/watch?v=TqfbAXCCVwE&t=1508s)


The *second system effect* (also known as second-system syndrome) is the tendency of small, elegant,
and successful systems to be succeeded by over-engineered, bloated systems, due to inflated
expectations and overconfidence.

How can we our system more resilient to inevitable change? - Good architecture.

Architecture as enabling constraints.

3 constraints you can use today for more resilient frontend architecture
- source code dependencies must point inward.
  - big ball of mud.
  - layered
  - modular
- be conservation about code reuse 
  - decoupled > DRY. Code reuse is not a goal in and of itself.
  - avoid coupling that diverges over time
- Enforce your boundaries
