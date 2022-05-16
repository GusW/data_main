# AI Accountability Essential Training

## 1 - Context of AI

---

### The Promise of AI

- `AI`
  - thinking machines that can learn from experience and operate without specific instructions
- `ML`
  - computer algorithms that learn from data to predict patterns or outcomes
- `Neural Networks`
  - algorithms with a hidden layer of nodes
- `Deep Learning`
  - specific kind of neural network with many well developed layers
- `Predictive modeling and analytics`
  - general practice of building model to predict specific outcomes

### General and Narrow AI

- `General or Strong AI`

  - General purpose thinking machines that can reason and learn on many topics, just like a human
  - Common in sci-fi
  - Focus of early research
  - Amount of info required and number of decisions that must be made grow exponentially in a combinatorial explosion

- `Narrow or Weak AI`
  - Focus on a specific domain or problem to solve
  - Dramatically reduces problem space and number of permutations that must be considered
  - Most growth in AI has been in these focused domains

---

## 2 - Technical Challenges of AI

---

### The challenge of classification errors

- `AI = Automated Categorization`
  - Supervised learning
    - AI puts new observations into existing criterion categories based on matches with existing data
  - Unsupervised learning
    - AI groups cases based on similarity of measured attributes without a specific criterion
    - how AI categorizes tumors, drives a car or transcribes speech to text
- `Defining Accuracy`
  - Misleading to rely on just total % of observations correctly categorized
  - When a category is rare, even high total accuracy can have massive errors
  - Mostly false positives

### The causes of classification errors

- `Bayes' Theorem`

  - The probability of an accurate conclusion given the data is affected by several factors
    - The probability of true positives
    - The probability of false positives
    - The base rate of the outcome

- `Identifying Rate Diseases`

  - Diagnoses can be bases on blood tests, MRIs, EKGs, etc
  - Assume that the prevalence of diseases can vary frin 1/100 to 1/1.000.000
  - Assume that AI correcly identifies 99% of patients who have the disease (true positives)
  - Assume that AI incorrecly identifies 1% of heatlhy patients as having the disease (false positives)

- `Identifying Diseases`
  | Rate | True Positives | False Positives | Ratio |
  | ------------- |:-------------:| :-----:|:-----:|
  | 1 in 100 | 9.900.000 | 9.900.000 | 1:1|
  | 1 in 1.000 | 990.00 | 9.990.000 |10:1|
  | 1 in 10.000 | 99.000 | 9.999.000 |101:1|
  | 1 in 100.000 | 9.900 | 9.999.900 |101:1|
  | 1 in 1.000.000 | 990 | 9.999.990 |101:1|

- `Contributions to Errors`

  - Limited variability in data sets
  - Homogeneous raters
  - Algorithms are evaluated by overall classification accuracy and not for bias in subgroups
  - Algorithms may not generalize well to new situations
  - Lack of accountability

- `Ovecoming Technical Problems`
  - These errors are primarily technical, not inherent to AI
  - Use more diverse training data
  - Use more diverse raters
  - Assess algorithms for bias
  - Check algorithms in new situations
  - Need clear determinations of accountability

### Bias in AI

- `AI Behaving Badly`
  - The Microsoft Tay twitter bot only took 12 hours to become a misogynistic, anti-Semitic, conspiracy theorist
  - COMPAS sentencing software gave inaccurate, racially-biased recidivism predictions for black and white defendants
  - PredPol predicted crimes much higher than atual rates in primarily minority neighborhoods, leading to increased policing
  - The Google online ad system showed much higher paying jobs to men than to women

### Supervised and unsupervised learning

- `Unsupervised Learning`
  - Data is not labeled with an outcome category
  - Goal os to find cases that are similar to each other based on provided data
  - Clustering is helpful for marketing segmentation
  - No one correct answer
- `Supervised Learning`
  - Observations are labeled with outcome
  - Predict outcome category with other variables
  - Apply model to new data
  - Accuracy is important
  - But limited to variables and categories in original data
  - Labels may be subjective

### Biased labeling of data

- `Objective` judgments are easy:
  - book
  - dog
  - shoes
  - tree
  - etc
- `Subjective` evaluations depend on who is judging
  - Exciting vs. noisy
  - Calm vs. boring
  - Risk vs. potential
  - Familiat vs. novel
  - Interrater reliability
    - Match between judge and user
- `Anchoring and Stability Biases`
  - The anchoring bias means that first impressions or judgments are strong and resistant to new information
  - Once a model is developed, new variables for each case may not have as much influence as they should
  - Stability bias means that the model makes consistent categorizations even when the outcome has fundamentally shifted
- `What to Do about AI Bias`
  - Deliberately gather more diverse data sets
  - Include lables from a wider range of judges
  - Monitor output of algorithms
  - Focus on small categories and edge cases
  - Laws and regulations may be necessary to address bias the same way privacy is

### Construct validity

- `Clever Hans`
  - "Smart" horse who use to answer maths and logic questions by stamping
  - Proven to be falsy: would be stamping due to repetitions of sequential tasks:
    - Say something looking at its eyes
    - Look at their feet
    - Start stamping until they looked back at its eyes
- `Occam's Razor`
  - "One should not multiply entities beyond necessity"
  - The simplest explanation is usually the correct one
  - And the simplest answer usually generalizes best
- `Black Boxes`
  - A black box is something that converts input to output using an unknown or unexamined process
    - Mental processes
    - Genetic processes
    - Complex algorithms
- `Black Boxes and Construct Validity`
  - When a computer is explicitly programmed, it's possible to tell what information is processed and how
  - But black-box approaches like deep learning make the process nearly impossible to follow
  - Methods from psychological research are sometimes used to infer what the algorithms are doing
  - In psychological research, "construct validity" indexes how well the actual measurements match the intended ones

### Seeing the wrong thing

- `Predicting Sexuality from Profile Photos`
  - A deep learning project claimed to ble able to predict a person's sexuality from a profile photo
  - The researches attributed this to the affect of prenatal hormones on facial morphology, among other attributes
  - But secondary research found that nonphysical attributes like makeup or glasses worked as well
- `Data Leakage in Machine Learning Contests`
  - Data leakage refers to artifacts in the data that provide unintended clues to the outcomes
  - In machine learning contests, people build model on labeled data and test it on hold-out data
  - Models can be accurate without actually predicting the outcome
  - For example, the Big Data Utah - Taylor Swift Big Data Competition

### The absence of meaning

- `Predictive Analysis of Text`
  - Machine Learning algorithms to determine authorship, describe personality, or grade student essays
  - Often based on "bag of words" analyses
  - Ignores meaning completely
- `Predictive Elements`
  - Pronouns: he, she, me, you, ....
  - Articles: the, a, ...
  - Particles: if, then, however, ...
  - Conjunctions: and, but, or, ...
- `Essay-Grading Algorithms`
  - Word count
  - Ratio of upper and lower case letters
  - Number of subordinate clauses
  - Some algorithms claim to evaluate strength of argument, but still look at associations
- `The Alien Mind of Deep Learning`
  - Neural networks, including deep learning, may build up intermediate constructs
  - But these may bear no relationship to human categories
  - AI algorithms sometimes described as "aliens minds"
  - Always based on associations

### Vulnerability to attacks

- `Harassment by AI`
  - Intentionally manipulating an AI algorithm to produce inaccurate results
  - Different from the "unforced errors" of accidental miscategorization
  - Aimed at AI and not humans
  - Shows potential fragility of AI
- `Adversarial Machine Learning`
  - Also known as "adversarial examples"
    - Not to be confused with "generative adversarial networks"
  - Evasion attack
    - attack on the implemented model
  - Poisoning attack
    - attack on the model in development
  - Dodging
    - not being recognized as an object
  - Impersonating
    - being recognized as a specific, other object

### Attacking AI

- `Text`
  - HotFlip: White-Box Adversarial Examples for Text Classification
- `Audio`
  - _Nicholas Carlini_: Audio Adversarial Examples
- `Images`
  - Explaing and Harnessing Adversarial Examples (_Ian J. Goodfellow, Johathin Shlens & Christian Szegedy_)
  - Accessorize to a Crime: Real and Stealthy Attacks on State-of-the-Art Face Recognition (_Mahmood Sharif, Sruti Bhagavatula, Lujo Bauer, Micheal K. Reiter_)
  - Synthesizing Robust Adversarial Examples (_Anish Athalye, Logan Engstrom, Andrew Ilyas, Kevin Kwok_)
  - Physical Adversarial Examples Agains Deep Neural Networks (_BLAIR - Berkeley Artificial Intelligence Research_)

### Protecting AI

- `Two Kinds of Attacks`
  - Evasion attack
    - Attack on the implemented model
    - Requires creating new examples to fool the algorithm
    - Can potentially be defeated by updating and improving algorithm
  - Poisoning attack
    - Attack on the model in development
    - Bakes the mistakes into the algorithm
    - Frequently updated algorithms are especially vulnerable
- `How to Respond?`
  - Less trust, more security
  - White hat evaluation
  - Regular testing of performance against other algorithms
  - Create laws and regulations to address adversatial machine learning attacks

---

## 3 - Social Challenges of AI

---

### Dimensions of justice

### Justice and AI

### Moral Reasoning

### Relational Ethics

### Issues of authenticity

---

## 4 - Legal Challenges of AI

---

### General Data Protection Regulation (GDPR)

### Spurious discrimination

### The right to explanation

### Discrimination in data

### Discrimination in implementation

### Liability

### Accountability laws

---

## 5 - Safety Challenges of AI

---

### AI in life and death situations

### AI in the military

### The challenges of military AI

---

## 6 - Confronting the challenges of AI

---

### Strategies for developers

### Strategies for executives

### Strategies for public relations

### Strategies for regulators

### Strategies for consumers
