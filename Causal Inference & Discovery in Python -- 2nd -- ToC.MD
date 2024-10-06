# Causal Inference and Discovery with Python

## Preface 

## Part 1: Causality – an Introduction

### 1. Causality – Hey We Have Machine Learning So Why Even Bother?
#### A brief history of causality 4
#### Why causality? Ask babies! 5
- Interacting with the world 5
- Confounding – relationships that are not real 6
#### How not to lose money… and human lives 9
- A marketer’s dilemma 9
- Let’s play doctor! 10
- Associations in the wild 12
#### Wrapping it up 12
#### References 12


### 2. Judea Pearl and the Ladder of Causation
#### From associations to logic and imagination – the Ladder of Causation 15 
#### Associations 18
- Let’s practice! 20
#### What are interventions? 23
- Changing the world 24
- Correlation and causation 26
#### What are counterfactuals? 28
- Let’s get weird (but formal)! 28
- The fundamental problem of causal inference 30
- Computing counterfactuals 30
- Time to code! 32
#### Extra – is all machine learning causally the same? 33
- Causality and reinforcement learning 33 
- Causality and semi-supervised and unsupervised learning 34
#### Wrapping it up 34
#### References 35


### 3. Regression Observations and Interventions
#### Starting simple – observational data and linear regression 37 
- Linear regression 37 
- p-values and statistical significance 41 
- Geometric interpretation of linear regression 42 
- Reversing the order 42 
#### Should we always control for all available covariates? 44 
- Navigating the maze 45 
- If you don’t know where you’re going, you might end up somewhere else 45 
- Get involved! 48 
- To control or not to control? 48 
#### Regression and structural models 49  
- SCMs 49 
- Linear regression versus SCMs 49 
- Finding the link 49 
- Regression and causal effects 51 
#### Wrapping it up 53 
#### References 53 


### 4. Graphical Models
#### Graphs, graphs, graphs 55 
- Types of graphs 56 
- Graph representations 58 
- Graphs in Python 60 
#### What is a graphical model? 63 
- DAG your pardon? Directed acyclic graphs in the causal wonderland 64 
- Definitions of causality 64 
- DAGs and causality 65 
- Let’s get formal! 65 
- Limitations of DAGs 66 
#### Sources of causal graphs in the real world 66 
- Causal discovery 67 
- Expert knowledge 67 
- Combining causal discovery and expert knowledge 67 
#### Extra – is there causality beyond DAGs? 67  
- Dynamical systems 67 
- Cyclic SCMs 68 
#### Wrapping it up 68 
#### References 69


### 5. Forks Chains and Immoralities
#### Graphs and distributions and how to map between them 71 
- How to talk about independence 72 
- Choosing the right direction 73 
- Conditions and assumptions 74 
#### Chains, forks, and colliders or… immoralities 78 
- A chain of events 78 
- Chains 79 
- Forks 80 
- Colliders, immoralities, or v-structures 82 
- Ambiguous cases 84 
#### Forks, chains, colliders, and regression 85 
- Generating the chain dataset 87 
- Generating the fork dataset 88 
- Generating the collider dataset 89 
- Fitting the regression models 90 
#### Wrapping it up 93 
#### References 93 



## Part 2: Causal Inference  

### 6. Nodes Edges and Statistical (In)dependence 
#### You’re gonna keep ‘em d-separated 98 
- Practice makes perfect – d-separation 99 
#### Estimand first! 102 
- We live in a world of estimators 102 
- So, what is an estimand? 102 
#### The back-door criterion 104 
- What is the back-door criterion? 105 
- Back-door and equivalent estimands 105 
#### The front-door criterion 107 
- Can GPS lead us astray? 108 
- London cabbies and the magic pebble 109 
- Opening the front door 110 
- Three simple steps toward the front door 111 
- Front-door in practice 112 
#### Are there other criteria out there? Let’s do-calculus! 118 
- The three rules of do-calculus 119 
- Instrumental variables 120 
#### Wrapping it up 122 
#### Answer 122 
#### References 123


### 7. The Four-Step Process of Causal Inference  
#### Introduction to DoWhy and EconML 126 
- Python causal ecosystem 126 
- Why DoWhy? 128 
- Oui, mon ami, but what is DoWhy? 128 
- How about EconML? 129 
#### Step 1 – modeling the problem 130 
- Creating the graph 130 
- Building a CausalModel object 132 
#### Step 2 – identifying the estimand(s) 133 
#### Step 3 – obtaining estimates 134 
#### Step 4 – where’s my validation set? Refutation tests 135 
- How to validate causal models 135 
- Introduction to refutation tests 137 
#### Full example 139 
- Step 1 – encode the assumptions 140 
- Step 2 – getting the estimand 142 
- Step 3 – estimate! 142 
- Step 4 – refute them! 144 
#### Wrapping it up 149 
#### References 


### 8. Causal Models – Assumptions and Challenges
#### I am the king of the world! But am I? 152
- In between 152
- Identifiability 153
- Lack of causal graphs 153
- Not enough data 154
- Unverifiable assumptions 156
- An elephant in the room – hopeful or hopeless? 156
- Let’s eat the elephant 156
#### Positivity 157
#### Exchangeability 161
- Exchangeable subjects 161
- Exchangeability versus confounding 161
#### …and more 162
- Modularity 162
- SUTVA 164
- Consistency 164
#### Call me names – spurious relationships in the wild 165
- Names, names, names 165
- Should I ask you or someone who’s not here? 166
- DAG them! 166
- More selection bias 168
#### Wrapping it up 169
#### References 17


### 9. Causal Inference and Machine Learning – from Matching to Meta-Learners
#### The basics I – matching 174
- Types of matching 174
- Treatment effects – ATE versus ATT/ATC 175
- Matching estimators 176
- Implementing matching 178
#### The basics II – propensity scores 183
- Matching in the wild 183
- Reducing the dimensionality with propensity scores 185
- Propensity score matching (PSM) 185
#### Inverse probability weighting (IPW) 186
- Many faces of propensity scores 186
- Formalizing IPW 187
- Implementing IPW 187
- IPW – practical considerations 188
#### S-Learner – the Lone Ranger 188
- The devil’s in the detail 189
- Mom, Dad, meet CATE 190
- Jokes aside, say hi to the heterogeneous crowd 190
- Waving the assumptions flag 192
- You’re the only one – modeling with S-Learner 192
- Small data 198
- S-Learner’s vulnerabilities 199
#### T-Learner – together we can do more 200
- Forcing the split on treatment 200
- T-Learner in four steps and a formula 201
- Implementing T-Learner 202
#### X-Learner – a step further 204
- Squeezing the lemon 204
- Reconstructing the X-Learner 205
- X-Learner – an alternative formulation 207
- Implementing X-Learner 208
#### Wrapping it up 212
#### References 213


### 10. Causal Inference and Machine Learning – Advanced Estimators Experiments Evaluations and More
#### Doubly robust methods – let’s get more! 216
- Do we need another thing? 216
- Doubly robust is not equal to bulletproof… 218
- …but it can bring a lot of value 218
- The secret doubly robust sauce 218
- Doubly robust estimator versus assumptions 220
- DR-Learner – crossing the chasm 220
- DR-Learners – more options 224
- Targeted maximum likelihood estimator 224
#### If machine learning is cool, how about double machine learning? 227
- Why DML and what’s so double about it? 228
- DML with DoWhy and EconML 231
- Hyperparameter tuning with DoWhy and EconML 234
- Is DML a golden bullet? 239
- Doubly robust versus DML 240
- What’s in it for me? 241
#### Causal Forests and more 242
- Causal trees 242
- Forests overflow 242
- Advantages of Causal Forests 242
- Causal Forest with DoWhy and EconML 243 
#### Heterogeneous treatment effects with experimental data – the uplift odyssey 245
- The data 245
- Choosing the framework 251
- We don’t know half of the story 251
- Kevin’s challenge 252
- Opening the toolbox 253
- Uplift models and performance 257
- Other metrics for continuous outcomes with multiple treatments 262
- Confidence intervals 263
- Kevin’s challenge’s winning submission 264
- When should we use CATE estimators for experimental data? 264
- Model selection – a simplified guide 265
#### Uncertainty quantification for Meta-Learners: Conformal Prediction **NEW**
- Binary treatments and observational data
> *Author's note: Wang et al., 2024; Lei & Candes, 2021, Alaa et al., 2023*
- Continuous treatments and observational data
> *Author's note: Schroeder et al., 2024*
- Binary treatments and mixed data
> Author's note: Chen et al., 2024 (KDD)
#### Causal Chamber - your (sort of) real-world causal buddy **NEW**
#### Extra – counterfactual explanations 267 **NEW**
- Bad faith or tech that does not know? 267
#### Wrapping it up 268
#### References 269

### 11. Causal Inference and Machine Learning – Deep Learning, NLP, and Beyond
> Author's note: (In reply to Bhavesh Amin): We could theoretically split this chapter into 2-3 chapters, but that would probably result (adding other additions) in a book that is ~700-800 pages long. I am not sur if that's the right trajectory for this book. 
#### Going deeper – deep learning for heterogeneous treatment effects 274 
- CATE goes deeper 274 
- SNet 276 
#### Transformers and causal inference 284 
- The theory of meaning in five paragraphs 285 
- Making computers understand language 285 
- From philosophy to Python code 286 
- LLMs and causality 286 
- The three scenarios 288 
- CausalBert 292 
#### Prompting and semi-symbolic training to improve your LLM’s causal reasoning **NEW**
- Jane the Discoverer **NEW**
- CLadder **NEW**
- Axiomatic training **NEW**
#### Causality and time series – when an econometrician goes Bayesian 297 
- Quasi-experiments 297
- Twitter acquisition and our googling patterns 298
- The logic of synthetic controls 298
- A visual introduction to the logic of synthetic controls 300
- Starting with the data 302
- Synthetic controls in code 303
- Challenges 30 
#### Wrapping it up 309
#### References 309

### 12. Inference Under Hidden Confounding **NEW**
#### Detecting Hidden Confounding in The Data **NEW**
#### Partial Identification **NEW**
#### Proximal Inference **NEW**
#### Sensitivity Analysis **NEW**
#### Causal Inference from non-IID data **NEW**



## Part 3: Causal Discovery
### 13. Can I Have a Causal Graph Please?
#### Sources of causal knowledge 316 
- You and I, oversaturated 316 
- The power of a surprise 317 
#### Scientific insights 317 
- The logic of science 318 
- Hypotheses are a species 318 
- One logic, many ways 319 
- Controlled experiments 319 
- Randomized controlled trials (RCTs) 320 
- From experiments to graphs 321 
- Simulations 321 
#### Personal experience and domain knowledge 321 
- Personal experiences 322 
- Domain knowledge 323 
#### Causal structure learning 323 
#### Wrapping it up 324 
#### References 324 

### 14. Causal Discovery and Machine Learning – from Assumptions to Applications
#### Causal discovery – assumptions refresher 328 
- Gearing up 328 
- Always trying to be faithful… 328 
- …but it’s difficult sometimes 328 
- Minimalism is a virtue 329 
#### The four (and a half) families 329 
- The four streams 329 
#### Introduction to gCastle 331 
- Hello, gCastle! 331 
- Synthetic data in gCastle 331 
- Fitting your first causal discovery model 336 
- Visualizing the model 336 
- Model evaluation metrics 338 
#### Constraint-based causal discovery 341 
- Constraints and independence 341 
- Leveraging the independence structure to recover the graph 342 
- PC algorithm – hidden challenges 345 
- PC algorithm for categorical data 346 
#### Score-based causal discovery 347 
- Tabula rasa – starting fresh 347 
- GES – scoring 347 
- GES in gCastle 348
#### Functional causal discovery 349 
- The blessings of asymmetry 349 
- ANM model 350 
- Assessing independence 353 
- LiNGAM time 355 
#### Score-matching causal discovery **NEW**
#### Gradient-based causal discovery 360 
- What exactly is so gradient about you? 360 
- Shed no tears 362 
- GOLEMs don’t cry 363 
- The comparison 363 
#### Encoding expert knowledge 366 
- What is expert knowledge? 366 
- Expert knowledge in gCastle 366 
#### Wrapping it up 368 
#### References 368 


### 15. Causal Discovery and Machine Learning – Advanced Deep Learning and Beyond  
#### Advanced causal discovery with deep learning 372 
> Author's note: we will replace the DECI sections with transformer-baseds supervised learning approaches as they seem much more useful in practice
- From generative models to causality 372 **REMOVE**
- Looking back to learn who you are 373 **REMOVE**
- DECI’s internal building blocks 373 **REMOVE**
- DECI in code 375 **REMOVE**
- DECI is end-to-end 387 **REMOVE**
- Causal discovery and supervised learning **NEW**
- Is that (black) magic!? **NEW**
- Building your structure-learning transformer **NEW**
#### Causal discovery under hidden confounding 387 
- The FCI algorithm 388 
- Other approaches to confounded data 392 
#### Causal discovery from time-series data **NEW**
> Author's note: Shimizu & Maeda, 2024, Runge
#### Extra – going beyond observations 393 
- ENCO 393 
- ABCI 393
#### Assumption violations in causal discovery **NEW**
> Author's note: https://arxiv.org/abs/2310.13387
#### Causal discovery benchmarking with causalAssembly **NEW**
#### Causal discovery – real-world applications, challenges, and open problems 394 
#### Wrapping it up! 395 
#### References 396 

### 16. Causality and Business **NEW**
#### Real-world use cases **NEW**
#### How causal doers go from vision to implementation **NEW**
#### Most frequent challenges **NEW**
#### Wrapping it up! **NEW**

### 17. Epilogue
#### What we’ve learned in this book
#### Five steps to get the best out of your causal project 400 
- Starting with a question 400 
- Obtaining expert knowledge 401 
- Generating hypothetical graph(s) 401 
- Check identifiability 402 
- Falsifying hypotheses 402 
#### Causality and business 403 **REMOVE**
- How causal doers go from vision to implementation **REMOVE**
#### Toward the future of causal ML **UPDATED**
- Where are we now and where are we heading? 406 
- Causal benchmarks 406 
- Causal data fusion 407
- Intervening agents 407 
- Causal structure learning 408 
- Imitation learning 408 
#### Learning causality 409 
#### Let’s stay in touch 410 
#### Wrapping it up 411 
#### References 411 
