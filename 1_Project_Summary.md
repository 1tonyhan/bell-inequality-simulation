# Bell's Theorem and the CHSH Inequality
**Summer project - July 2025.**

In this project, I explore the basics of quantum computing and how experimentation around Bell's theorem (through qiskit and using IBM cloud server QPUs) demonstrates violation of classical behaviour - pointing to non-classical behaviour, namely, entanglement.  

For this project, I followed IBM Quantum Platform's CHSH experiment tutorial, which I have linked in my Resources Used.md file, along with all of the other resources I used for this project. 

**Here is a summary of the Bell theorem as I understand it:**

First, to set the stage: I will use the example of a particle with a spin of 0 that decays into two smaller, separate particles with spin up or down. For simplicity, I will call these particles A and B henceforth. I will also set the premise that there is an assumption of no other angular momentum other than spin in this situation; meaning spin is conserved. This is an ideal assumption and makes this topic easier for me to understand.

Imagine A and B end up in two completely different places, and are being observed by two different people. These two people will observe the particles and measure their spin along an axis - lets say the vertical Z axis for now. This intrinsic property of angular momentum, once measured in one particle, will reveal the spin of the other particle due to conservation - for example, if A is measured to have spin up along Z, B must be measured to have spin down along Z (and vice versa) since they decayed from a 0 spin particle. Their spins must add to 0. Okay, so this tells us very little; only that spin is conserved.

Now what if we set 3 axis of measurement rather than 1? Now, even with the measurement along any axis to be either up or down, there are a lot more possible combinations of measurements. Say the observers of A and B can choose to measure the spin of their particle along any of the 3 axes, independently of whichever axis the other observer chooses to measure along (recall they are really far away from each other, no communication!). Then, they send ONLY their value (either up or down) to a third observer. The observer recieves no information about which axis, only the spin state.

<img src="/images/threeAxis.png" width="550">

**Figure 1.1: 3 Axes to measure spin along; For simplicity, all axes are in the same plane, and separated by $120^{\circ}$**

One can postulate that in this case, there is a certain maximum probability that the values the third observer recieves are the same! What is this maximum probability?

Well we have two theories to explain this. One is hidden variable theory, or classical mechanics, and the other is quantum mechanics. What are any of these? I will try my best to explain that here:

**Hidden variable theory** is like a set of rules that A and B must obey. For example, one rule is that if A is measured to have spin up along Z, B must be measured to have spin down along Z. (provided they started from a spin 0 particle). With this logic, we can build a set of rules for these 2 particles A and B. Essentially, this set shows all the possible states of the axes for A, and then all the corresponding possible states of the axes for B. Below is an image of the set of rules for A and B on 3 measurement axes:


<img src="/images/hiddenVariableRules.png" width="550">

**Figure 1.2: Hidden Variable theory table**

<br />
From this table, we can obtain the possibilities that the observer recieves the same value from the people looking at A and B. Basically, in any given row, if you pick one of the three values from A, and one of the three values from B, the probability they are the same number is 4/9 for all but the cases in the first and last rows. So this is the maximum possibility that the observer recieves the same number from A and B, if hidden variable theory is followed; an upper bound in this theory <sup><a id="fn1-ref" href="#fn1">1</a></sup>.

<br />
<br />

**Now, for quantum mechanics:** it turns out, if we look at the quantum mechanics side of things, the probability that this observer recieves the same number from A and B can exceed 4/9! How does this happen?

Exceeding the probability value of 4/9 for measuring the same spin along any 2 axis is given by a bit of geometry and linear algebra stemming from something called a bloch sphere. 

I will explain the bloch sphere in a separate file**INSERT LINK HERE LATER!**   [a relative link](main/2. Aside on Bloch Spheres.md), as it goes a bit more into the nitty gritty of things called qubits, which utilize this quantum behaviour to enable quantum computing!

Anyhow, from the bloch sphere, we get the behaviour that in quantum mechanics: on a given particle, the probability of measuring the same spin along 2 axes X and Y separated by an angle theta is given by this formula:

$$P(same) = \cos^2(\frac{\theta}{2})$$

Going back to our example of 




...







...


<br />


<br />





<br />


<a id="fn1"></a> 

[1] Here, I realized much later into the project that with IBM's tutorial, they recreate a more accessible experiment/visualization of bell's theorem with 3 axes rather than the original 2. I looked up the reason for this, and it was because scientists realized that with three equally spaces axes, measurements are rotationally invariant and generally more stable to test. This means the newer method is a lot more realistic to obtain results efficiently/effectively in the lab.  Why does this matter? with three angles, we have a different upper bound - 

[↩](#fn1-ref)
<a id="fn1-ref"></a>



