# Risk-Averse Distributional Reinforcement Learning

This repository contains Tex and other files for my Master Thesis.

See `thesis.pdf` for the full text. See https://github.com/Silvicek/cvar-algorithms for the code.

## Abstract

Conditional Value-at-Risk (CVaR) is a well-known measure of risk that has been
used for decades in the financial sector and has been directly equated to robustness,
an important component of Artificial Intelligence (AI) safety. In this thesis we
focus on optimizing CVaR in the context of Reinforcement Learning, a branch of
Machine Learning that has brought significant attention to AI due to its generality
and potential.

As a first original contribution, we extend the CVaR Value Iteration algorithm
(Chow et al. [20]) by utilizing the distributional nature of the CVaR objective. The
proposed extension reduces computational complexity of the original algorithm from
polynomial to linear and we prove it is equivalent to the said algorithm for continuous
distributions.

Secondly, based on the improved procedure, we propose a sampling version of
CVaR Value Iteration we call CVaR Q-learning. We also derive a distributional
policy improvement algorithm, prove its validity, and later use it as a heuristic for
extracting the optimal policy from the converged CVaR Q-learning algorithm.

Finally, to show the scalability of our method, we propose an approximate Q-learning
algorithm by reformulating the CVaR Temporal Difference update rule as
a loss function which we later use in a deep learning context.

All proposed methods are experimentally analyzed, using a risk-sensitive gridworld
environment for CVaR Value Iteration and Q-learning and a challenging visual environment
for the approximate CVaR Q-learning algorithm. All trained agents are
able to learn risk-sensitive policies, including the Deep CVaR Q-learning agent which
learns how to avoid risk from raw pixels.
