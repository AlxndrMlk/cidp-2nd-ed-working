# Causal Inference and Discovery with Python

## Preface 

## Part 1: Causality – an Introduction

### 1. Causality – Hey We Have Machine Learning So Why Even Bother?
#### A brief history of causality
#### Why causality? Ask babies!
- Interacting with the world
- Confounding – relationships that are not real
#### How not to lose money… and human lives
- A marketer’s dilemma
- Let’s play doctor!
- Associations in the wild
#### Wrapping it up
#### References

### 2. Judea Pearl and the Ladder of Causation
#### From associations to logic and imagination – the Ladder of Causation
#### Associations
- Let’s practice!
#### What are interventions?
- Changing the world
- Correlation and causation
#### What are counterfactuals?
- Let’s get weird (but formal)!
- The fundamental problem of causal inference
- Computing counterfactuals
- Time to code!
#### Extra – is all machine learning causally the same?
- Causality and reinforcement learning
- Causality and semi-supervised and unsupervised learning
#### Wrapping it up
#### References

### 3. Regression Observations and Interventions
#### Starting simple – observational data and linear regression
- Linear regression
- p-values and statistical significance
- Geometric interpretation of linear regression
- Reversing the order
#### Should we always control for all available covariates?
- Navigating the maze
- If you don’t know where you’re going, you might end up somewhere else
- Get involved!
- To control or not to control?
#### Regression and structural models

- SCMs
- Linear regression versus SCMs
- Finding the link
- Regression and causal effects
#### Wrapping it up
#### References


### 4. Graphical Models
#### Graphs, graphs, graphs
- Types of graphs
- Graph representations
- Graphs in Python
#### What is a graphical model?
- DAG your pardon? Directed acyclic graphs in the causal wonderland
- Definitions of causality
- DAGs and causality
- Let’s get formal!
- Limitations of DAGs
#### Sources of causal graphs in the real world
- Causal discovery
- Expert knowledge
- Combining causal discovery and expert knowledge
#### Extra – is there causality beyond DAGs?

- Dynamical systems
- Cyclic SCMs
#### Wrapping it up
#### References

### 5. Forks Chains and Immoralities
#### Graphs and distributions and how to map between them
- How to talk about independence
- Choosing the right direction
- Conditions and assumptions
#### Chains, forks, and colliders or… immoralities
- A chain of events
- Chains
- Forks
- Colliders, immoralities, or v-structures
- Ambiguous cases
#### Forks, chains, colliders, and regression
- Generating the chain dataset
- Generating the fork dataset
- Generating the collider dataset
- Fitting the regression models
#### Wrapping it up
#### References



## Part 2: Causal Inference  

### 6. Nodes Edges and Statistical (In)dependence 
#### You’re gonna keep ‘em d-separated
- Practice makes perfect – d-separation
#### Estimand first!
- We live in a world of estimators
- So, what is an estimand?
#### The back-door criterion
- What is the back-door criterion?
- Back-door and equivalent estimands
#### The front-door criterion
- Can GPS lead us astray?
- London cabbies and the magic pebble
- Opening the front door
- Three simple steps toward the front door
- Front-door in practice
#### Are there other criteria out there? Let’s do-calculus!
- The three rules of do-calculus
- Instrumental variables
#### Wrapping it up
#### Answer
#### References

### 7. The Four-Step Process of Causal Inference  
#### Introduction to DoWhy and EconML
- Python causal ecosystem
- Why DoWhy?
- Oui, mon ami, but what is DoWhy?
- How about EconML?
#### Step 1 – modeling the problem
- Creating the graph
- Building a CausalModel object
#### Step 2 – identifying the estimand(s)
#### Step 3 – obtaining estimates
#### Step 4 – where’s my validation set? Refutation tests
- How to validate causal models
- Introduction to refutation tests
#### Full example
- Step 1 – encode the assumptions
- Step 2 – getting the estimand
- Step 3 – estimate!
- Step 4 – refute them!
#### Wrapping it up
#### References 


### 8. Causal Models – Assumptions and Challenges
#### I am the king of the world! But am I?
- In between
- Identifiability
- Lack of causal graphs
- Not enough data
- Unverifiable assumptions
- An elephant in the room – hopeful or hopeless?
- Let’s eat the elephant
#### Positivity
#### Exchangeability
- Exchangeable subjects
- Exchangeability versus confounding
#### …and more
- Modularity
- SUTVA
- Consistency
#### Call me names – spurious relationships in the wild
- Names, names, names
- Should I ask you or someone who’s not here?
- DAG them!
- More selection bias
#### Wrapping it up
#### References

### 9. Causal Inference and Machine Learning – from Matching to Meta-Learners
#### The basics I – matching
- Types of matching
- Treatment effects – ATE versus ATT/ATC
- Matching estimators
- Implementing matching
#### The basics II – propensity scores
- Matching in the wild
- Reducing the dimensionality with propensity scores
- Propensity score matching (PSM)
#### Inverse probability weighting (IPW)
- Many faces of propensity scores
- Formalizing IPW
- Implementing IPW
- IPW – practical considerations
#### S-Learner – the Lone Ranger
- The devil’s in the detail
- Mom, Dad, meet CATE
- Jokes aside, say hi to the heterogeneous crowd
- Waving the assumptions flag
- You’re the only one – modeling with S-Learner
- Small data
- S-Learner’s vulnerabilities
#### T-Learner – together we can do more
- Forcing the split on treatment
- T-Learner in four steps and a formula
- Implementing T-Learner
#### X-Learner – a step further
- Squeezing the lemon
- Reconstructing the X-Learner
- X-Learner – an alternative formulation
- Implementing X-Learner
#### Wrapping it up
#### References

### 10. Causal Inference and Machine Learning – Advanced Estimators Experiments Evaluations and More
#### Doubly robust methods – let’s get more!
- Do we need another thing?
- Doubly robust is not equal to bulletproof…
- …but it can bring a lot of value
- The secret doubly robust sauce
- Doubly robust estimator versus assumptions
- DR-Learner – crossing the chasm
- DR-Learners – more options
- Targeted maximum likelihood estimator
#### If machine learning is cool, how about double machine learning?
- Why DML and what’s so double about it?
- DML with DoWhy and EconML
- Hyperparameter tuning with DoWhy and EconML
- Is DML a golden bullet?
- Doubly robust versus DML
- What’s in it for me?
#### Causal Forests and more
- Causal trees
- Forests overflow
- Advantages of Causal Forests
- Causal Forest with DoWhy and EconML
#### Heterogeneous treatment effects with experimental data – the uplift odyssey
- The data
- Choosing the framework
- We don’t know half of the story
- Kevin’s challenge
- Opening the toolbox
- Uplift models and performance
- Other metrics for continuous outcomes with multiple treatments
- Confidence intervals
- Kevin’s challenge’s winning submission
- When should we use CATE estimators for experimental data?
- Model selection – a simplified guide
#### Uncertainty quantification for Meta-Learners: Conformal Prediction **NEW**
- Binary treatments and observational data
> *Author's note: Wang et al., 2024; Lei & Candes, 2021, Alaa et al., 2023*
- Continuous treatments and observational data
> *Author's note: Schroeder et al., 2024*
- Binary treatments and mixed data
> Author's note: Chen et al., 2024 (KDD)
#### Causal Chamber - your (sort of) real-world causal buddy **NEW**
#### Extra – counterfactual explanations 267 **NEW**
- Bad faith or tech that does not know?
#### Wrapping it up
#### References
### 11. Causal Inference and Machine Learning – Deep Learning, NLP, and Beyond
> Author's note: (In reply to Bhavesh Amin): We could theoretically split this chapter into 2-3 chapters, but that would probably result (adding other additions) in a book that is ~700-800 pages long. I am not sur if that's the right trajectory for this book. 
#### Going deeper – deep learning for heterogeneous treatment effects
- CATE goes deeper
- SNet
#### Transformers and causal inference
- The theory of meaning in five paragraphs
- Making computers understand language
- From philosophy to Python code
- LLMs and causality
- The three scenarios
- CausalBert
#### Prompting and semi-symbolic training to improve your LLM’s causal reasoning **NEW**
- Jane the Discoverer **NEW**
- CLadder **NEW**
- Axiomatic training **NEW**
#### Causality and time series – when an econometrician goes Bayesian
- Quasi-experiments
- Twitter acquisition and our googling patterns
- The logic of synthetic controls
- A visual introduction to the logic of synthetic controls
- Starting with the data
- Synthetic controls in code
- Challenges
#### Wrapping it up
#### References
### 12. Inference Under Hidden Confounding **NEW**
#### Detecting Hidden Confounding in The Data **NEW**
#### Partial Identification **NEW**
#### Proximal Inference **NEW**
#### Sensitivity Analysis **NEW**
#### Causal Inference from non-IID data **NEW**



## Part 3: Causal Discovery
### 13. Can I Have a Causal Graph Please?
#### Sources of causal knowledge
- You and I, oversaturated
- The power of a surprise
#### Scientific insights
- The logic of science
- Hypotheses are a species
- One logic, many ways
- Controlled experiments
- Randomized controlled trials (RCTs)
- From experiments to graphs
- Simulations
#### Personal experience and domain knowledge
- Personal experiences
- Domain knowledge
#### Causal structure learning
#### Wrapping it up
#### References

### 14. Causal Discovery and Machine Learning – from Assumptions to Applications
#### Causal discovery – assumptions refresher
- Gearing up
- Always trying to be faithful…
- …but it’s difficult sometimes
- Minimalism is a virtue
#### The four (and a half) families
- The four streams
#### Introduction to gCastle
- Hello, gCastle!
- Synthetic data in gCastle
- Fitting your first causal discovery model
- Visualizing the model
- Model evaluation metrics
#### Constraint-based causal discovery
- Constraints and independence
- Leveraging the independence structure to recover the graph
- PC algorithm – hidden challenges
- PC algorithm for categorical data
#### Score-based causal discovery
- Tabula rasa – starting fresh
- GES – scoring
- GES in gCastle
#### Functional causal discovery
- The blessings of asymmetry
- ANM model
- Assessing independence
- LiNGAM time
#### Score-matching causal discovery **NEW**
#### Gradient-based causal discovery
- What exactly is so gradient about you?
- Shed no tears
- GOLEMs don’t cry
- The comparison
#### Encoding expert knowledge
- What is expert knowledge?
- Expert knowledge in gCastle
#### Wrapping it up
#### References


### 15. Causal Discovery and Machine Learning – Advanced Deep Learning and Beyond  
#### Advanced causal discovery with deep learning
> Author's note: we will replace the DECI sections with transformer-baseds supervised learning approaches as they seem much more useful in practice
- From generative models to causality 372 **REMOVE**
- Looking back to learn who you are 373 **REMOVE**
- DECI’s internal building blocks 373 **REMOVE**
- DECI in code 375 **REMOVE**
- DECI is end-to-end 387 **REMOVE**
- Causal discovery and supervised learning **NEW**
- Is that (black) magic!? **NEW**
- Building your structure-learning transformer **NEW**
#### Causal discovery under hidden confounding
- The FCI algorithm
- Other approaches to confounded data
#### Causal discovery from time-series data **NEW**
> Author's note: Shimizu & Maeda, 2024, Runge
#### Extra – going beyond observations
- ENCO
- ABCI
#### Assumption violations in causal discovery **NEW**
> Author's note: https://arxiv.org/abs/2310.13387
#### Causal discovery benchmarking with causalAssembly **NEW**
#### Causal discovery – real-world applications, challenges, and open problems
#### Wrapping it up!
#### References

### 16. Causality and Business **NEW**
#### Real-world use cases **NEW**
#### How causal doers go from vision to implementation **NEW**
#### Most frequent challenges **NEW**
#### Wrapping it up! **NEW**

### 17. Epilogue
#### What we’ve learned in this book
#### Five steps to get the best out of your causal project
- Starting with a question
- Obtaining expert knowledge
- Generating hypothetical graph(s)
- Check identifiability
- Falsifying hypotheses
#### Causality and business 403 **REMOVE**
- How causal doers go from vision to implementation **REMOVE**
#### Toward the future of causal ML **UPDATED**
- Where are we now and where are we heading?
- Causal benchmarks
- Causal data fusion
- Intervening agents
- Causal structure learning
- Imitation learning
#### Learning causality
#### Let’s stay in touch
#### Wrapping it up
#### References
