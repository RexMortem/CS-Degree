**Artificial Intelligence (AI):** Techniques that make computers "smart". 

AI started out with **Good Old-Fashioned Artificial Intelligence (GOFAI)** which were rule-based systems (where the rules are designed by humans).

An example of GOFAI is SHRDLU which was a rule-based AI chatbot that contributed major advancements to NLP.

While SHRDLU was impressive, it could not learn and was limited by the knowledge it was given via human input; in contrast, **Machine Learning (ML)** methods allow machines to learn from their mistakes. 

ML often uses statistical methods to let computers learn (which you can explore in [[Year 3/CS342/Overview|CS342]]), and this module is focused on **Neural Computing (NC)** which are a specific form of ML that is inspired by the structure of the brain.

There is also **Deep Learning (DL)** which is a variant of NC where three or more layers are used in a multi-layer neural network.
## NC vs ML

ML: Determining the properties of the statistical model is called **machine learning**.

NC: Determining the properties of the neural network is called **learning rule**.

We already know $\text{NC} \subseteq \text{ML}$ - when should you use specifically NC instead of a different ML technique to learn?

| Scenario                 | ML    | NC    |
| ------------------------ | ----- | ----- |
| Choose Your Own Features | Yes   | No    |
| Training Data            | Small | Large |
| Training Time            | Short | Long  |
| Accuracy                 | Low   | High  |
