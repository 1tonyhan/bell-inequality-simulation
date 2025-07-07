# Bell's Theorem and the CHSH Inequality
Summer project - July 2025.

In this project, I explore the basics of quantum computing and how experimentation around Bell's theorem (through qiskit and using IBM cloud server QPUs) demonstrates violation of classical behaviour - pointing to non-classical behaviour, namely, entanglement. 

For this project, I have set up a single quantum circuit through Qiskit using Python. With this circuit, I used IBM's cloud server access to test the CHSH inequality and recorded my results. After placing the data in matlab to visualize it, 

Here is a brief summary of the Bell theorem as I understand it:

First, to set the stage: I will use the example of a particle with a spin of 0 that decays into two separate but entangled particles with spin of +/- 1/2. (+ is spin up, - is spin down) For simplicity, I will call these particles A and B henceforth. I will also set the premise that there is an assumption of no other angular momentum other than spin in this situation; meaning spin is conserved.

Imagine A and B end up in two completely different places, and are being observed by two different people. These two people will observe the particles and measure their spin. This intrinsic property of angular momentum, once measured in one particle, will reveal the spin of the other particle due to conservation - this is entanglement; taking a measurement on one particle instantly reveals the state of the other particle. For example, if A is measured as up spin, B must be measured as down spin (and vice versa) since they decayed from a 0 spin particle.

...


Here is a timeline of this project, for those why may be interested (dd/mm/yyyy):<br />
  *30/06/2025 - Research of bell states, focus on tensor product and mathematical matrix representation of two qubit system states. Correlation and      anticorrelation. <br />
  *01/07/2025 - Research of bell states, how to create an entangled two qubit system using two qubits, a hadamard gate, and a CNOT gate. Learned how     the gates function. Matrix representation of CNOT gates, more linear algebra concerning qubit states. <br />
  *02/07/2025 - Basic proper notation of regular and superposition states, how the bell states are properly expressed in this notation. eg. |Φ⁺〉 = 
  |00〉 + |11〉 ) / √2 <br />
  *03/07/2025 - installation and learning of how to use qiskit and python, and how to link to IBM cloud servers to access real quantum hardware. <br />
  *07/07/2025 - Research of Bloch Spheres to improve understanding of quantum states. <br />
  *


Here is a list of resources I used to complete this project:<br />
https://www.youtube.com/watch?v=pS69lqCMdy8 - IBM video on bell's inequality<br />
https://www.youtube.com/watch?v=qd-tKr0LJTM - Bell's inequality by a professor on youtube<br />
https://medium.com/quantum-untangled/quantum-states-and-the-bloch-sphere-9f3c0c445ea3 - Bloch Spheres<br />
https://qubit.guide/6.3-chsh-inequality - CHSH Inequality; online textbook<br />
