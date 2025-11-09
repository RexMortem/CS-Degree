
## Naive Bayesian Classification

Recall Bayes' Rule:

$P(A|B) \cdot P(B) = P(B|A) \cdot P(A)$

Using Bayes' Rule, we have:
$P(\text{spam}|\text{words}) = \frac{P(\text{words}|\text{spam}) \cdot P(\text{spam})}{P(\text{words})}$

This is saying that we can calculate the probability of it being spam if it contains these words, by knowing:
- the probability of an email being spam (how often does spam show up?)
- the probability of the words showing up
- the probability of these words showing up in spam (how often do they show up in the sampled spam emails?)

### Naive Bayes Assumption


###  Optimising Naive Bayesian

- We require the probability of words showing up, which is hard to compute and requires large samples
	- With $d$ words/features, you need $2^{d}$ unique samples to see each combination once
	- And there are usually a *lot* of features for spam filtering (high-dimensional)

**Solution:** We don't actually have to have the probability of words showing up. 

When classifying words as spam, we compare $P(\text{spam}|\text{words})$ against $P(\text{not spam}|\text{words})$. Let's expand this out: 

$P(\text{spam}|\text{words}) > P(\text{not spam}|\text{words}) \equiv$
$\frac{P(\text{words}|\text{spam}) \cdot P(\text{spam})}{P(\text{words})} > \frac{P(\text{words}|\text{not spam}) \cdot P(\text{not spam})}{P(\text{words})} \equiv$
$P(\text{words}|\text{spam}) \cdot P(\text{spam}) > P(\text{words}|\text{not spam}) \cdot P(\text{not spam}).$


### What if a feature has no samples?

What if none of the samples contain a feature e.g. in this case, it could be a word "trillionaire". 

If none of the samples contain "trillionaire", then $P(\text{contains trillionaire}|\text{spam}) = 0$. So when we compare $P(\text{contains trillionaire}|\text{spam}) \cdot P(\text{spam}) > P(\text{contains trillionaire}|\text{not spam}) \cdot P(\text{not spam})$, we get $0 > 0$ so it never gets classified as spam.

**Solution:** Use Laplace smoothing. This is the equivalent of introducing two fake spam emails: one where "trillionaire" shows up, and one where it doesn't. How do we do this?

