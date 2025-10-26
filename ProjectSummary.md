# Bell's Theorem and the CHSH Inequality
Summer project - July 2025.

In this project, I explore the basics of quantum computing and how experimentation around Bell's theorem (through qiskit and using IBM cloud server QPUs) demonstrates violation of classical behaviour - pointing to non-classical behaviour, namely, entanglement.  

For this project, I followed IBM Quantum Platform's CHSH experiment tutorial, which I have linked at the very bottom of this readme, along with all of the other resources I used for this project. 

Here is a summary of the Bell theorem as I understand it:

First, to set the stage: I will use the example of a particle with a spin of 0 that decays into two smaller, separate particles with spin up or down. For simplicity, I will call these particles A and B henceforth. I will also set the premise that there is an assumption of no other angular momentum other than spin in this situation; meaning spin is conserved. This is an ideal assumption and makes this topic easier for me to understand.

Imagine A and B end up in two completely different places, and are being observed by two different people. These two people will observe the particles and measure their spin along an axis - lets say the vertical Z axis for now. This intrinsic property of angular momentum, once measured in one particle, will reveal the spin of the other particle due to conservation - for example, if A is measured to have spin up along Z, B must be measured to have spin down along Z (and vice versa) since they decayed from a 0 spin particle. Their spins must add to 0. Okay, so this tells us very little; only that spin is conserved.

Now what if we set 3 axis of measurement rather than 1? Now, even with the measurement along any axis to be either up or down, there are a lot more possible combinations of measurements. Say the observers of A and B can choose to measure the spin of their particle along any of the 3 axes, independently of whichever axis the other observer chooses to measure along (recall they are really far away from each other, no communication!). Then, they send ONLY their value (either up or down) to a third observer. The observer recieves no information about which axis, only the spin state.

One can postulate that in this case, there is a certain maximum probability that the values the third observer recieves are the same! What is this maximum probability?

Well we have two theories to explain this. One is hidden variable theory, and the other is quantum mechanics. What are any of these? I will try my best to explain that here:

Hidden variable theory is like a set of rules that A and B must obey. For example, one rule is that if A is measured to have spin up along Z, B must be measured to have spin down along Z. (provided they started from a spin 0 particle). With this logic, we can build a set of rules for these 2 particles A and B. Essentially, this set shows all the possible states of the axes for A, and then all the corresponding possible states of the axes for B.

**insert table here**

From this table, we can obtain the possibilities that the observer recieves the same value from the people looking at A and B. Basically, in any given row, if you pick one of the three values from A, and one of the three values from B, the probability they are the same number is 4/9 for all but the cases in the first and last rows. So this is the maximum possibility that the observer recieves the same number from A and B, if hidden variable theory is followed; an upper bound in this theory. <sup>[1](#note_about_bounds)</sup>

Now, for quantum mechanics: it turns out, if we look at the quantum mechanics side of things, the probability that this observer recieves the same number from A and B can exceed 4/9! How does this happen?






...







...



Here is a timeline of this project, for those why may be interested (dd/mm/yyyy):<br />
  -30/06/2025 - Research of bell states, focus on tensor product and mathematical matrix representation of two qubit system states. Correlation and      anticorrelation. <br />
  -01/07/2025 - Research of bell states, how to create an entangled two qubit system using two qubits, a hadamard gate, and a CNOT gate. Learned how     the gates function. Matrix representation of CNOT gates, more linear algebra concerning qubit states. <br />
  -02/07/2025 - Basic proper notation of regular and superposition states, how the bell states are properly expressed in this notation. eg. |Φ⁺〉 = 
  |00〉 + |11〉 ) / √2 <br />
  -03/07/2025 - installation and learning of how to use qiskit and python, and how to link to IBM cloud servers to access real quantum hardware. <br />
  -07/07/2025 - Research of Bloch Spheres to improve understanding of quantum states. <br />
  -07/28/2025 - Research of the CHSH Inequality: more experimentally friendly version of the Bell inequality <br />

Here, I was on vacation with my family (I went to various places in France and Italy!), and then school started, where I started focusing on my studies more. I resumed this project much later after adjusting to my engineering physics workload, and finishing my first round of midterms.
  
  -10/23/2025 - Review of the CHSH experiment, using the IBM video. Followed the IBM tutorial and set up a virtual environment .venv for a jupyterNotebook, and actually performed the CHSH experiment on IBM QPUs by linking my IBM quantum platform account to the code. Plotted results.
  -10/25/2025 - Updated this ReadMe file, and further consolidated my understanding of how the upper bounds for hidden variable theory vs quantum mechanics was determined. I am still slightly confused about the quantum mechanics upper bound, so I will revisit tomorrow.
  -10/26/2025 - 
  




<br />


<br />

Generative AI was used in the following way:<br />
I learned the content from websites or videos, and asked ChatGPT to listen to me explain the topics to it, and give me critique on what I understand vs what I don't. I was able to consolidate my knowledge much more effectively this way.

<br />






<br />

<a name="note_about_bounds">1</a>: Here, I realized much later into the project that with IBM's tutorial, they recreate a more accessible experiment/visualization of bell's theorem with 3 axes rather than the original 2. I looked up the reason for this, and it was because scientists realized that with three equally spaces axes, measurements are rotationally invariant and generally more stable to test. This means the newer method is a lot more realistic to obtain results efficiently/effectively in the lab.  Why does this matter? with three angles, we have a different upper bound - 

