## Context

I have compiled some principles to hopefully serve as a snapshot of my software engineering philosophy and biases. Some of them are from well-known principles (e.g., [SOLID](https://en.wikipedia.org/wiki/SOLID), [Clean Code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)) while others were learned from personal experience. In any case, all of them have served me well throughout my career so far. **This list is by no means meant to be exhaustive and should NOT be regarded as my unequivocal set of rules for building quality software**. Although some of the items below could be considered as common sense, there are a few that can be a bit more debatable and I fully acknowledge that different approaches generally come with their pros and cons. That said, this compilation is my humble attempt at capturing the engineering values that I resonate with and feel quite strongly about.

## Sections

- [In General](#in-general)
- [On Code Design](#on-code-design)
- [On Writing Tests](#on-writing-tests)
- [On Dependencies](#on-dependencies)
- [Miscellaneous](#miscellaneous)

### In General

- There is no such thing as perfect requirements/design (i.e., constantly changing)
- Minimize assumptions
- Aim for a fast feedback loop
- Refrain from bikeshedding ([Law of Triviality](https://en.wikipedia.org/wiki/Law_of_triviality))
- There are always trade-offs when choosing an engineering approach
- When evaluating technical decisions, avoid false dichotomy

### On Code Design

- Favor explicit over implicit code
- Compile-time safety is worth it
- Cost of typing a few more lines of code can be overrated
- Depend on abstractions, not concretions ([Dependency Inversion](https://en.wikipedia.org/wiki/Dependency_inversion_principle))
- Encapsulate what varies
- Choose composition over inheritance
- Avoid leaky abstractions
- Prefer pure functions
- Avoid side effects and reliance on global state (define variables as "local" as possible)
- Strive for low coupling, high cohesion
- Be intentional about the responsibilities of each component
- Keep handler layer (e.g., controller) light
- Producing correct output is just the bare minimum
- Code readability is highly correlated with maintainability
- Clear is better than clever
- Write self-documenting code
- It helps to have related code close to each other
- Naming of variable/function/class should be expressive
- Avoid using flag arguments (split into separate functions instead)
- Handle errors gracefully
- Consider using guard clauses
- KISS ([Keep It Simple, Stupid](https://en.wikipedia.org/wiki/KISS_principle))
- A little duplication can be cheaper than a wrong abstraction ([The Wrong Abstraction](https://sandimetz.com/blog/2016/1/20/the-wrong-abstraction), [Rule of Three](<https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming)>))
- Do not be afraid to continuously refactor
- Standardize approaches within a particular codebase
- Avoid premature optimization

### On Writing Tests

- Prefer fresh fixtures
- Consider utilizing mocks to achieve pure unit tests that can run fast
- There is a cost to maintaining tests (test judiciously)

### On Dependencies

- Be mindful when adding dependencies since they come with inherent cost
- Prefer lightweight libraries over full-blown frameworks

### Miscellaneous

- Consider level of security relative to risk
- Minimize variance across different environments (e.g., local, staging, production)
- Use orthogonal env vars for configuration ([12-factor app](https://12factor.net/config))
