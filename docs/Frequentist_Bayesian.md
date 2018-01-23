[TOC]

------------------------------------------------------------------------

**Foreword**

-   Notes.

------------------------------------------------------------------------

So what does Bayesian statistics mean for A/B testing?

First, let’s summarize Bayesian and Frequentist approaches, and what the
difference between them is.

Frequentist
===========

Using a Frequentist method means making predictions on underlying truths
of the experiment using only data from the current experiment. We learn
frequentist statistics in entry-level statistics courses.

A t-test, where we ask, "Is this variation different from the control?"
is a basic building block of this approach. The focus is on the
observations alone; no other data is used and no judgment. The procedure
is objective and based solely on the test data and the assumed model.

Bayesian
========

In Bayesian statistics, past knowledge of similar experiments is encoded
into a statistical device known as a prior, and this prior is combined
with current experiment data to make a conclusion on the test at hand.
So, the biggest distinction is that Bayesian probability specifies that
there is some prior probability.

A fundamental aspect of Bayesian inference is updating your beliefs in
light of new evidence. Essentially, you start out with a prior belief
and then update it in light of new evidence.

For example, restaurant owners know that if by 5 p.m. there are 50
reservations, then they can predict there will be around 250 covers for
the night. This is a prior and can be updated with new sets of data.

Conclusion
==========

In the Bayesian approach, the parameters that we are trying to estimate,
are treated as random variables having some known prior distribution. In
the Frequentist approach, they are a fixed but unknown; there is no
probability associated with it. Random variables are governed by their
parameters (mean, variance, etc), and distributions (Gaussian, Poisson,
binomial, etc). The prior is just the prior belief about these
parameters.

In this way, we can think of the Bayesian approach to treating
probabilities as degrees of belief, rather than as frequencies generated
by some unknown process.

In summary, the difference is that in the Bayesian view, a probability
is assigned to a hypothesis. In the Frequentist view, a hypothesis is
tested without being assigned a probability.

------------------------------------------------------------------------

<table>
<thead>
<tr class="header">
<th></th>
<th align="left">Frequentist</th>
<th align="left">Bayesian</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Definition of probability</td>
<td align="left">Long-run expected frequency in repeated (actual or hypothetical) experiments (law of large numbers).</td>
<td align="left">Relative degree of belief in the state of the world.</td>
</tr>
<tr class="even">
<td>Point estimate</td>
<td align="left">Maximum likelihood estimate.</td>
<td align="left">Mean, mode, or median of the posterior probability distribution.</td>
</tr>
<tr class="odd">
<td>Confidence intervals for parameters</td>
<td align="left">Based on the likelihood ratio test; i.e., the expected probability distribution of the maximum likelihood estimate over many experiments.</td>
<td align="left">Credible intervals based on the posterior probability distribution.</td>
</tr>
<tr class="even">
<td>Confidence intervals for non-parameters</td>
<td align="left">Based on likelihood profile/ratio test, or by resampling from the sampling distribution of the parameter.</td>
<td align="left">Calculated directly from the distribution of parameters.</td>
</tr>
<tr class="odd">
<td>Model selection</td>
<td align="left">Discard terms that are not significantly different from a nested (null) model at a previously set confidence interval level.</td>
<td align="left">Retain terms in models, on the argument that processes are not absent simply because they are not statistically significant.</td>
</tr>
<tr class="even">
<td>Difficulties</td>
<td align="left">Confidence intervals are confusing (range that will contain the true value in a proportion alpha or repeated experiments); rejection of model terms of non-significance.</td>
<td align="left">Subjectivity; need to specify priors.</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------