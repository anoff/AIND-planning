# Literature research on AI Planning Evolutions

> Research for Udacity AI Nanodegree by Andreas Offenhaeuser, 2018

Planning in Artificial Intelligence refers to methods that determine a sequence of actions in order to achieve a pre-defined goal. One of the biggest challenges in solving planning problems is handling complex scenarios. Real world problems tend to have a high complexity and non-trivial solutions. Therefore improvements in this field often try to either better model real world scenarios or solve them more efficiently. [1, page 375]

### Partially Observable Markov Decision Process (POMDP)

The classic Markov Decision Process requires full observability. POMDP on the other hand can handle scenarios in which the actual state is not fully detectable by the agent. This is often the case in real world scenarios due to sensor limitations. To solve this POMDP uses probability distributions [2]. These probability distributions can e.g. be inferred from the uncertainty in the agents measurement equipment. Through continous observation and interaction with the problem space the agent can gather knowledge and optimize the probabilities for the available state space.

### Metaplanning Techniques

Since the STRIPS algorithm in 1971 by Fikes and Nilsson several planning systems have emerged that tried to combine existing and new approaches to build planners for specific domains [4, page 63]. With the appearance of _Metaplanning_ algorithms like OPM (1979 by Hayes-Roth) and PRS (1987 by Georgeff and Lansky) the planning theory gained an additional layer of complexity. With _Metaplanning_ the agent not only decides which actions to take to reach a new state but also modifies its own strategy and planning behavior to achieve the best possible outcome. [4, page 66]

### Solution Extraction as Constraint Satisfaction

Extracting the solution out of a _Graphplan_ might have exponential complexity [3, page 98]. Falkenhainer and Forbus described in 1988 how _dynamic Constraint Satisfaction Problems_ can be used to narrow down a search problems using intermediate values (sub-goal). Finding sub-goals generates new constraints to the surrounding search levels which shrinks the possible search space and therefore improves search duration. [3, page 99]

## Sources

[1] [Artificial Intelligence: A Modern Approach](http://aima.cs.berkeley.edu/2nd-ed/newchap11.pdf), Norvig and Russell, Second Edition 2002

[2] [Planning and acting in partially observable
stochastic domains](http://people.csail.mit.edu/lpk/papers/aij98-pomdp.pdf), Kaelbling, Littman and Cassandra,1998

[3] [Recent Advances in AI Planning](https://www.aaai.org/ojs/index.php/aimagazine/article/view/1459/1358), Wild, Published in AI Magazine Volume 20 Number 2 (1999)

[4] [AI Planning: Systems and Techniques](https://www.aaai.org/ojs/index.php/aimagazine/article/view/833/751), Hendler, Tate and Drummomd, Published in AI Magazine Volume 11 Number 2 (1990) 