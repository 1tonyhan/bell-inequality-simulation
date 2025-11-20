# Bell's Theorem and the CHSH Inequality

**Summer project - July 2025.**

In this project, I explore the basics of quantum computing and how experimentation around Bell's theorem (through qiskit and using IBM cloud server QPUs) demonstrates violation of classical behaviour - pointing to non-classical behaviour, namely, entanglement.  

For this project, I followed IBM Quantum Platform's CHSH experiment tutorial, which I have linked in my Resources Used.md file, along with all of the other resources I used for this project. 

### Here is a summary of the Bell theorem as I understand it:

First, to set the stage: I will use the example of a particle with a spin of 0 that decays into two smaller, separate particles with spin up or down. For simplicity, I will call these particles A and B henceforth. I will also set the premise that there is an assumption of no other angular momentum other than spin in this situation; meaning spin is conserved. This is an ideal assumption and makes this topic easier for me to understand.

Imagine A and B end up in two completely different places, and are being observed by two different people. These two people will observe the particles and measure their spin along an axis - lets say the vertical Z axis for now. This intrinsic property of angular momentum, once measured in one particle, will reveal the spin of the other particle due to conservation - for example, if A is measured to have spin up along Z, B must be measured to have spin down along Z (and vice versa) since they decayed from a 0 spin particle. Their spins must add to 0. Okay, so this tells us very little; only that spin is conserved.

Now what if we set 3 axis of measurement rather than 1? Now, even with the measurement along any axis to be either up or down, there are a lot more possible combinations of measurements. Say the observers of A and B can choose to measure the spin of their particle along any of the 3 axes, independently of whichever axis the other observer chooses to measure along (recall they are really far away from each other, no communication!). Then, they send ONLY their value (either up or down) to a third observer. The observer recieves no information about which axis, only the spin state.

<img src="/images/threeAxis.png" width="550">

**Figure 1.1: 3 Axes to measure spin along; For simplicity, all axes are in the same plane, and separated by $120^{\circ}$**
<a name="threeAxis"></a>

One can postulate that in this case, there is a certain maximum probability that the values the third observer recieves are the same! What is this maximum probability?

Well we have two theories to explain this. One is hidden variable theory, or classical mechanics, and the other is quantum mechanics. What are any of these? I will try my best to explain that here:

***Hidden variable theory*** is like a set of rules that A and B must obey. For example, one rule is that if A is measured to have spin up along Z, B must be measured to have spin down along Z. (provided they started from a spin 0 particle). With this logic, we can build a set of rules for these 2 particles A and B. Essentially, this set shows all the possible states of the axes for A, and then all the corresponding possible states of the axes for B. Below is an image of the set of rules for A and B on 3 measurement axes:


<img src="/images/hiddenVariableRules.png" width="550">

**Figure 1.2: Hidden Variable theory table**

<br />
Note: in this table, I have set spin down is 0 and spin up is 1.

<br />

From this table, we can obtain the possibilities that the observer recieves the same value from the people looking at A and B. Basically, in any given row (apart from the first and last; I will exclude these as they have no chance of meeting the requirements), if you pick one of the three values from A, and one of the three values from B, the probability they are the same number is 4/9 for all apart from the cases in the first and last rows. So this is the maximum possibility that the observer recieves the same number from A and B, if hidden variable theory is followed; 4/9 is an upper bound in this theory <sup><a id="fn1-ref" href="#fn1">1</a></sup>.

<br />
<br />

***Now, for quantum mechanics:*** it turns out, if we look at the quantum mechanics side of things, the probability that this observer recieves the same number from A and B can exceed 4/9! How does this happen?

Exceeding the probability value of 4/9 for measuring the same spin along any 2 axis is given by a bit of geometry and linear algebra stemming from something called a bloch sphere.


<a name="blochAnchor"></a>

I will explain the bloch sphere in [a separate file](2_Aside_on_Bloch_Spheres.md), as it goes a bit more into the nitty gritty of things called qubits, which utilize this quantum behaviour to enable quantum computing! Please give it a read, as I think it will help greatly with understanding where the rest of what I am about to explain comes from :)


Anyhow, from the bloch sphere, we get the behaviour that in quantum mechanics: on a given particle, the probability of measuring the same spin along 2 axes X and Y separated by an angle theta is given by this formula:

$$P(same) = \cos^2(\frac{\theta}{2})$$

Okay, so how does this relate to our example of particles A and B, each with 3 axes to measure spin along?

Let me set up a test/example case. Suppose that:

- Along one of the axes on particle A (lets say axis 1, the upwards axis for now - see figure 1.1 or the figure 1.3 below), we measure spin up. That means along the same axis, we must measure spin down on B.
- Recall that we have an external observer that recieves either 'spin up' or 'spin down' from A and B. We want the probability that the observer recieves the SAME response


Looking at the same axis on B will obviously given the observer 2 different responses, so it is not so useful; So lets look at the two other axes on B.

In this case, we already know that the spin along axis 1 on particle B is down. Let's use this fact, in tandem with the rule $$P(same) = \cos^2(\frac{\theta}{2})$$ to examine the spin on axis 2 and 3:

<img src="/images/case1.png" width="550">

**Figure 1.3: Quantum Mechanics, case 1**


As we can see, the angle formed by the spin down vector on B with axis 2 or 3 is $60^{\circ}$. Using the cosine rule, we get that there is a 3/4 chance that 2 or 3 will be measured as spin down, meaning a 1/4 chance to be measured as spin up and thus the same as particle A's measurement. Keep this value 1/4 in mind.

This is not the end of it!! we previously assumed that A is measured as spin up along axis 1. There is another case, where A is measured as spin down along 1, so B is measured spin up along 1! The numbers for B come along slightly differently:

<img src="/images/case2.png" width="550">

**Figure 1.4: Quantum Mechanics, case 2**


Here, we can see that the angle formed by the spin up vector on B with axis 2 or 3 is now $120^{\circ}$! So following the cosine rule: we get that there is a 1/4 chance that 2 or 3 will be measured as spin up, meaning a 3/4 chance to be measured as spin down and matching particle A's measurement.

Now we have these 2 values, 1/4 and 3/4. What do we do now? Well, we know that A has a 50% chance to be measured as spin up along 1, and a 50% chance to be measured as spin down along 1. So knowing that either case is equally probable to occur, we can simply take the average of 1/4 and 3/4, giving us a value of 1/2!

And whaddya know, 1/2 is larger than that value of 4/9 we got from classical mechanics! We can exceed the maximum correlation that classical mechanics predicts; Quantum mechanics beats classical mechanics! (by 0.5/9, or about 0.05555...)

And the beauty? It holds regardless of which orientation we look at; whether we make the assumptions we did about axis 1, 2 or 3 on A; this experiment is rotationally symmetric!!

That's pretty cool, but what are the implications, if there even are any? What difference does a value of 0.5/9 even make? Why is this worth winning the 2021 nobel prize in physics for?




...







...


<br />


<br />





<br />


<a id="fn1"></a> 

[1] Here, I realized much later into the project that with IBM's tutorial, they recreate a more accessible experiment/visualization of bell's theorem with 3 axes rather than the original 2. I looked up the reason for this, and it was because scientists realized that with three equally spaces axes, measurements are rotationally invariant and generally more stable to test. This means the newer method is a lot more realistic to obtain results efficiently/effectively in the lab.  Why does this matter? with three angles, we have a different upper bound - 

[return to [1]](#fn1-ref)
<a id="fn1-ref"></a>



