# PhD
## Proposals
### Bing Long
This research project aims to develop a novel framework for designing and simulating multi-agent systems that can cooperate or compete in complex and changing environments to achieve various goals. The framework will be inspired by some findings from mean-field game theory (MFGT) and evolutionary game theory (EGT), as well as evolutionary algorithms (EA), multi-armed bandits (MAB), and mechanism design (MD). 

MFGT studies strategic decision-making by small agents in very large populations, where each agent acts according to its own optimization problem, taking into account the aggregate behavior of other agents. 

EGT analyses Darwinian mechanisms with a system model with three main components: population, game, and replicator dynamics, where the evolution of strategies depends on their frequency-dependent fitness. EA are optimization methods that mimic natural selection processes by generating and evaluating candidate solutions using predefined operators. 

MAB are learning models that deal with the exploration-exploitation trade-off in sequential decision-making under uncertainty. 

MD is a branch of microeconomics that studies how to design rules or institutions that elicit desirable outcomes or behaviors from self-interested agents.

The proposed framework will combine these different approaches to define and guide several aspects of multi-agent systems, such as:

**- Population size, structure, and changing nature**
  The framework will use EA techniques to dynamically adjust the number and type of agents according to their performance and fitness. It will also allow for different sub-populations or groups of agents that can have different goals or preferences. The framework will also incorporate MFGT concepts to model how each agent interacts with a representative agent that captures the average effect of the population.
**- Optimal resource allocation**
  The framework will use MAB methods to allocate computational resources to each agent or group of agents based on their exploration-exploitation balance and expected rewards. It will also consider how resources can be shared or transferred among agents depending on their incentives and constraints.
**- Incentives and subsequent feedback loops, positive and negative**
  The framework will use MD principles to design reward functions or mechanisms that align the individual objectives of agents with the global or social objectives of the system. It will also account for how feedback loops can affect the learning and adaptation of agents over time.
**- Agent interactions, their types, and parameters**
  The framework will use EGT models to describe how agents play games with each other based on their strategies, payoffs, information, beliefs, etc. It will also consider how different types of interactions (e.g., cooperation, competition, coordination) can emerge or change depending on the environmental conditions or evolutionary pressures.
**- The environment in accordance with the final objective, its changing parameters**
  The framework will use EGT models to describe how the environment affects the fitness and evolution of strategies. It will also consider how agents can influence or modify their environment through their actions or signals. Moreover, it will allow for stochasticity or uncertainty in environmental parameters as well as spontaneous mutations or innovations.

The main contribution of this research project is to provide a general and flexible framework that can capture various aspects of multi-agent systems in complex and changing environments. The framework can be applied to various domains such as economics (e.g., trading robots), social sciences (e.g., voting processes), marketing (e.g., advertising campaigns), engineering (e.g., factory robots), etc. The expected outcomes are:

- A theoretical analysis of the properties and performance of the proposed framework under different settings and scenarios;
- A general mathematical model that captures the essential features of multi-agent systems inspired by mean-field game theory and evolutionary game theory; 
- A set of algorithms/rules that change different aspects of the model such as population structure, resource allocation, incentives, interactions, and environment in response to changing agents and circumstances in a non-discrete manner; 
- A computational implementation of the proposed framework using state-of-the-art algorithms and tools;
- A series of experiments and simulations using real-world data sets or synthetic benchmarks to validate and evaluate the proposed framework.

The main challenges are:
- Finding a suitable balance between generality and specificity in defining the components and parameters of the proposed framework;
- Dealing with scalability/performance issues that may arise when dealing with large populations or complex environments;
- Handling ethical issues when designing incentives or mechanisms that may affect human welfare or behavior.

### Bing Medium
The aim of this research is to develop a novel framework for designing and simulating multi-agent systems that can cooperate or compete in complex and changing environments. The framework will be inspired by some findings from mean-field game theory  , which studies strategic decision making by small interacting agents in very large populations, and evolutionary game theory  , which applies game theory to evolving populations in biology. The framework will also incorporate ideas from evolutionary algorithms, multi-armed bandits, and mechanism design. The main challenges are to define and guide the following aspects of multi-agent systems:

- Population size, its structure, and changing nature: How many agents are needed to achieve a given goal? How are they organized into sub-populations or layers? How can they adapt their structure over time based on their performance or fitness?
- Optimal resource allocation: How much computational power should be allocated to each agent or sub-population? How can resources be dynamically adjusted based on exploration/exploitation trade-offs and feedback loops?
- Incentives and subsequent feedback loops, positive and negative: What are the reward functions that motivate the agents to act in a certain way? How can they be aligned with the global objective of the system? How can positive and negative feedback mechanisms be implemented to reinforce or correct behaviors?
- Agent interactions, their types, and parameters: How do agents communicate with each other? What are the rules that govern their cooperation or competition? What are the effects of different types of interactions (e.g., cooperation, coordination, competition) on the system dynamics?
- The environment in accordance with the final objective, its changing parameters: What is the nature of the environment that the agents operate in? How does it change over time due to external factors or agent actions? How can sub-goals be defined to guide the agents towards the final objective?

The expected outcomes of this research are:

- A general mathematical model that captures the essential features of multi-agent systems inspired by mean-field game theory and evolutionary game theory. 
- A set of algorithms/rules that change different aspects of the model such as population structure, resource allocation, incentives, interactions, and environment in response to changing agents and circumstances in a non-discrete manner. 
- A software platform that allows for designing and simulating various scenarios involving multi-agent systems with different objectives and constraints.
- A set of case studies that demonstrate the applicability and usefulness of the framework for various domains such as trading robots, voting processes, marketing simulations, factory robots etc.

### Bing + dynamic + set of rules
The aim of this research proposal is to develop a novel framework for designing and simulating multi-agent systems that can cooperate or compete in complex and changing environments. The framework will be inspired by concepts from mean-field game theory, evolutionary game theory, evolutionary algorithms, multi-armed bandits, and mechanism design. These concepts will help to define and guide the following aspects of the multi-agent system:

- Population size, structure, and dynamics: The number of agents, their characteristics, and their evolution over time will be determined by the problem domain and the desired outcomes. The framework will allow for flexible population structures that can change according to the environmental feedback and the agents' performance. The framework will also enable pruning of unnecessary or ineffective agents and sub-populations using criteria such as fitness or exploration/exploitation trade-offs.
- Resource allocation: The framework will optimize the computational resources allocated to each agent or sub-population based on their relevance and contribution to the overall goal. The resource allocation will also take into account the complexity and uncertainty of the environment and the agents' interactions.
- Incentives and feedback loops: The framework will define reward functions that align with the desired outcomes and motivate the agents to act accordingly. The reward functions will also incorporate positive and negative feedback loops that reinforce or discourage certain behaviors or strategies.
- Agent interactions: The framework will specify the types and parameters of agent interactions, such as cooperation, competition, communication, coordination, learning, etc. The interactions will be modeled by synapses and neuron connections with activation/inhibition functions that regulate the information flow among agents.
- Environment: The framework will characterize the environment in which the agents operate according to its features, dynamics, constraints, opportunities, etc. The environment will provide feedback/supervision to the agents as well as allow them to act semi-autonomously. Moreover, the environment will be subject to second-order changes caused by agent actions as well as spontaneous mutations that introduce variability and uncertainty.

One of the main objectives of this research proposal is to derive a set of rules that will enable the multi-agent system to adapt to changing circumstances in a dynamic and non-discrete manner. This means that the system will be able to adjust its population structure, resource allocation,incentives, interactions, and environment representation according to the evolving conditions and the emerging challenges or opportunities.
The rules will be based on causal learning, rather than correlative-generative learning, meaning that they will capture the underlying mechanisms and relationships that govern the system's behavior and performance.