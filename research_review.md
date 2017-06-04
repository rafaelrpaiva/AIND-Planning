
### Research Review - Planning and Search

As observed in [1], planning is the process of computing several steps of a problem-solving procedure before executing any of them, which is generally solved by search techniques. In Planning, states have structured representations which are used by the planning algorithms.

One important difference is the relationship between actions and outcome. Is this scenario, AI planning and searching is divided in two great groups:

* **Deterministic algorithms**, where each action has a unique outcome.
* **Non-deterministic algorithms**, where each action has a set of possible outcomes or resulting states.

In the beginning of studies, we had distinct approaches between these two scenarios. But most recently, a third perspective is combining both deterministic and non-deterministic approaches in **hybrid algorithms**.

This review presents a brief summary in these 3 perspectives.

#### Deterministic Approach

The **Classical Planning** evolves an environment that is fully observable, deterministic, finite, static and discrete, as presented in [2].

Classical Planning started several years ago, with lots of strategies presented in AIMA Book, 3rd edition, Chapter 10 [1]. Total-order vs. partial-order planning, forward vs. backward searching, and the usage of other patterns - planning graphs; first-order deduction over situation calculus axioms; encoding a planning problem as a Boolean satisfiability problem or as a constraint satisfaction problem - shows the different ways that world researchers are trying to improve and evolve in their solutions. Each of them has its adherents, and there is as yet no consensus on which is best. Competition and cross-fertilization among the approaches have resulted in significant gains in efficiency for planning systems.

A very efficient summary of this timeline was presented by Stuart Russel and Peter Norvig in the "Bibliographical and Historical Notes" of AIMA's Chapter 10 (3rd ed).

#### Non-deterministic Approach

However, "most real world environments are non-deterministic"[3]. It is our reality, and several researchers, as Schoppers (1987) [4], Cimatti et. al (1998) [3], Koenig et. al (1995) [5] and many others try to embrace this context.

For working with uncertainty, variations of planning under uncertainty include conformant planning ([6] and [7]), contingent  planning [8], and probabilistic contingent planning, with differences stemming from the assumptions on the properties of the actions and the observability (sensing capabilities). See e.g., [9] for a discussion.

#### Hybrid Approach

The most recent approach is revisiting these two aspects and try to take the best of them to solve problems. 
Kishimoto, Botea and Daly (2016) [10], for instance, presented a novel approach that combines the strength of both deterministic and nondeterministic search in order to achieve superior performance. 

Initially, an A\* search is used checking whether the resulting deterministic plan remains correct and optimal under uncertainty. When the plan is invalid, a backpropagation step through the A\*'s search graph improves the initial heuristic while preserving its admissibility. After the backpropagation, an AO* search is run with the new improved heuristic.

This approach has certainly good perspectives for future work, and it is reasonable to expect that combining different approaches can be very powerful for some areas, as in transportation and journey planning as above.

#### References
[1] Russell, S., & Norvig, P. (2005). AI a modern approach. Learning, 2(3), 4.

[2] Udacity Nanodegree Program Intelligence Artificial Engineer - Term 1 - Chapter 7 - Lesson 12.

[3] Cimatti, A., Roveri, M., and Traverso, p. (1998). Automatic OBDD-based Generation of Universal Plans in 
Non-Deterministic domains.

[4] Schoppers, M. J. 1987. Universal plans for Reactive Robots in Unpredictable Environments. In Proc. of IJCAI-87, 1039-1046.

[5] Koenig, S., and Simmons, R. 1995. Real-Time Search in Non-Deterministic Domains. In Proc. of IJCAI-95, 1660-1667.

[6] Robert P. Goldman and Mark S. Boddy, 'Expressive planning and explicit knowledge', in Proceedings of the 3rd International Conference on Artificial Intelligence Planning Systems (AIPS), pp. 110-117, (1996).

[7] D. E. Smith and D. S. Weld, 'Conformant Graphplan', in Proceedings of the 15th National Conference on Artificial Intelligence (AAAI), pp.889-896, (1998).

[8] M. A. Peot and D. E. Smith, 'Conditional nonlinear planning', in Proceedings of the 1st International Conference on Artificial Intelligence Planning Systems (AIPS), pp. 189-197, (1992).

[9] B. Bonet and H. Geffner, 'Planning with incomplete information as heuristic search in belief space', in Proceedings of the 5th International Conference on Artificial Intelligence Planning Systems, pp. 52-61, (2000).

[10] Kishimoto, A., Botea, A. and Daly, E. Combining Deterministic and Nondeterministic Search for Optimal Journey Planning Under Uncertainty. Proceedings of the 22nd European Conference on Artificial Intelligence, pp. 295 (2016).