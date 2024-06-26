Paper outline

Title: Is posterior inference usually easy, in all graphical models?
or: The complexity of inference on typical-case observations in worst-case Bayesian networks.

- Background / technical introduction
    - The task of posterior inference is, given P, X, Y, y, to characterize P(X | Y = y)
        - This can mean a few things:
            - Compute P(X = x | Y = y)
            - Sample x ~ P(X | Y = y)
            - Compute some sort of CDF
        - Algorithmically, that means
            - ., ., .
        - We can also ask for approximations:
            - Relative PMF approximation
            - Additive PMF approximation
            - Sampling with tolerable error
            - Approximate CDF computation
        - Reductions among these:
            - If we can do Relative PMF, we can do Additive PMF.  If we can do Approx CDF, we can do Additive PMF via subtraction.
            - If we can do sampling, then given an upper bound on the domain size we can stochastically do Additive PMF via Monte Carlo estimation.
            - Thus, if it is the case that we can’t do additive PMF approximation on small sets X, we can’t do relative PMR, nor CDF, and if we can’t stochastically do additive PMF, we also can’t do sampling
    - It is known that even being able to do additive PMF approximation in graphical models would imply P = NP.
    - But I argue a more natural question is whether we can do this on typical-case observations.
        - State the definition of this for additive approximation
        - Maybe state definitions for the other problems (or just say it is the same idea — there is a set of observations with high probability, on which we can solve the previously articulated problems)
    - In this paper, I prove that:
        - If for any graphical model a ptime algorithm exists which can do additive PMF approximation on typical observations, then secure PRGs with constant-factor stretch do not exist
        - If for any graphical model a probabilistic ptime algorithm exists which can do additive PMF approximation on typical observations, then secure PRGs with exponential stretch do not exist
        - Both of these are proven for sets X with 1 variable (which would be the easiest case for an algorithm), and sets Y with many variables.
        - I also show that if Y is guaranteed to be small, there exist probabilistic algorithms that solve the problem in the typical case, so having large Y is necessary for any hardness result of this sort.
- Technical core section
    - Prove the main 2 results
    - State corollaries
    - Prove inference is easy if Y is small
- Related work
    - Related problems
        - Distributions & Complexity.
            - Quickly summarize P Samp, etc., and say how it is different than the study of conditional distributions
        - Inference in continuous distributions
            - Under standard formulations, can actually be noncomputable (Ackerman, Freer, Roy)
    - Hardness of inference
        - Cooper; Dagum & Luby
        - Uniform generation <=> counting is easy
    - When is inference easy? (Tractability results)
        - Majority ksat ()
            - Note that we actually only needed majority checks in the proof in this paper — but not for Ksat.
        - Dagum & Luby’s parametrized complexity result (+ cite Kwisthout for other parametrized complexity results)
            - My conjecture: in the typical-case, can replace this Dagum & Luby parametrized result with a bound on mutual information or chi-squared information
            - But the intuition is that these results are for the case where observations are uninformative
        - Another case where inference should be easy: only loose coupling.
            - Moitra 2017


