# bell-inequality-simulation
Summer project - July 2025.

In this project, I explore the basics of quantum computing and how experimentation around the bell inequality (through qiskit and using IBM cloud server QPUs) demonstrates violation of
classical mechanic behaviour - pointing to quantum behaviour, namely, entanglement. 

Here is a brief summary of the bell inequality as I understand it:

First, to set the stage: I will use the example of a particle with a spin of 0 that decays into two separate but entangled particles with spin of +/- 1/2. (+ is spin up, - is spin down) For simplicity, I will call these particles A and B henceforth. I will also set the premise that there is an assumption of no other angular momentum other than spin in this situation; meaning spin is conserved.

Imagine A and B end up in two completely different places, and are being observed by two different people. These two people will observe the particles and measure their spin. This intrinsic property of angular momentum, once measured in one particle, will reveal the spin of the other particle due to conservation - this is entanglement; taking a measurement on one particle instantly reveals the state of the other particle. For example, if A is measured as up spin, B must be measured as down spin (and vice versa) since they decayed from a 0 spin particle.


Here is a timeline of this project, for those why may be interested (dd/mm/yyyy):<br />
  *30/06/2025 - Research of bell states, focus on tensor product and mathematical matrix representation of two qubit system states. Correlation and      anticorrelation. <br />
  *01/07/2025 - Research of bell states, how to create an entangled two qubit system using two qubits, a hadamard gate, and a CNOT gate. Learned how     the gates function. Matrix representation of CNOT gates, more linear algebra concerning qubit states. <br />
  *02/07/2025 - Basic proper notation of regular and superposition states, how the bell states are properly expressed in this notation. eg. |Φ⁺〉 = 
  |00〉 + |11〉 ) / √2 <br />
  *03/07/2025 - installation and learning of how to use qiskit and python, and how to link to IBM cloud servers to access real quantum hardware. <br />


Here is a list of resources I used to complete this project:
