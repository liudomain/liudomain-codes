Our code implementation is derived from the article "Noise Quantum Approximation Optimization Algorithm for Solving MaxCut Problem This paper analyzes and examines the Quantum Approximation Optimization Algorithm (QAOA) for addressing the maximum cut problem under noisy conditions. The implementation is conducted on both the Mindspore platform and the Google platform. However, it is essential to further investigate the differences between the simulator implementation and the actual hardware device on the respective platforms. The overall research contents are as follows:
Mindspore：
1.	Selection of noisy circuit optimizer: Adam, SGD, Momentum, Adagrad, Adadelta. Adam and Adagrad perform best on noisy circuits
2.	Diagram type analysis: Fully connected graph (node n=3-10), random graph (edge e=10-32), Noise coefficient ${{q}_{j}}\in [0.1,0.9]$. N increases, AR increases; n> After 5, it tends to balance E increases, AR is a wavy change.
3.	Noise type (full connection diagram n=5-10), Ideal, Depolarizing,  AmplitudeDamping , BitFlip, BitPhaseFlip, Pauli, PhaseDamping, PhaseFlip. AR value of noisy channel is less than ideal channel; As qubits increase, most noisy channels tend to zero.
4.	Circuit layer: Number of sides (e=10-40),Circuit layer (p=2-16). With the increase of edge e, it changes in wave shape; However, the effect is not obvious with the increase of line level p.
5.	Output state probability distribution: Comparison between the Noise Content and the Ideal Circuit in Solving the Maximum Cut in a 5-node Fully Connected Graph. In the case of noise, the probability of suboptimal solution increases and the probability of optimal solution decreases
Google(Appendix):
1.	Evolution effect of target loss function: Ideal, noisy channel (full connection diagram n=6). $A{{R}_{noise}}\le A{{R}_{ideal}}$
2.	Angle evolution: Correlation between angle evolution and initial parameter selection.
3.	In the case of noise, the probability of suboptimal solution increases and the probability of optimal solution decreases
