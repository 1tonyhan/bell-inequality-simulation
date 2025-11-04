**Here is an aside on Bloch Spheres**

I think that this concept is quite important for understanding where the probability of measuring the same state on an axis X and Y separated by an angle theta comes from in quantum mechanics. For me, I was not willing to accept simply that this probability $P(same) = cos^2 (\frac{\theta}{2})$ with no explanation of where this comes from. So I took a look as to why this is the case, and that led me to the concept of a bloch sphere.

I will not delve too deeply into how a bloch sphere works, as that is not the focus of my project; I will offer a brief overview of what I think you would need to know, to understand where the upper bound in the CHSH experiment for quantum mechanics' argument comes from. Essentially, a bloch sphere is a way to represent quantum states in a more visually accessible way, to make it easier for our human brains to understand. Here is a brief explanation: 

A qubit or quantum state $\ket{\psi}$ is represented by: 

$$\ket{\psi} = \alpha \ket{0} + \beta \ket{1}$$

What do any of these mean? 

$\ket{0}$ is essentially a state where there is a 100% chance to measure spin up, whereas $\ket{1}$ is essentially a state where there is a 100% chance to measure spin down. (you can think of these as non quantum states, or classical states).

The quantum state $\ket{\psi}$ is basically composed of a superposition of the two classical states $\ket{0}$ and $\ket{1}$. These two classical states have probability amplitudes, $\alpha$ and $\beta$ respecively. They are special in that $\alpha^2 + \beta^2 = 1$ (the probability of measuring something in the quantum state $\ket{\psi}$ is 1), and $\alpha^2$ is the probability of measuring $\ket{0}$; $\beta^2$ is the probability of measuring $\ket{1}$.

However, we have a problem in representing such a state in reality: $\alpha$ and $\beta$ are complex numbers! That means that both values have a real and an imaginary part. So theoretically, to represent a quantum state $\ket{\psi}$ as is, we would need some 4 dimentional graph... which is super hard to visualize. So researchers set out to find a better 'tool' to visualize these quantum states. 

Eventually, researchers were able to connect the work of physicist Felix Bloch to the geometric representation that is now commonly known today as the Bloch Sphere! (hence it being named after him).

I will not show the derivation of how the bloch sphere represents this, as that is not one of my goals for this project; it is also because I don't understand it well enough to feel confident explaining it.

Basically, through some elegant 'massaging' of the equation for $\ket{\psi}$, a conversion to polar coordinates, then using euler's identity and some geometry, the the form of a qubit can be represented as a vector in a 3d unit sphere. This vector only requires 2 parameters as opposed to the 4 we would need if we did not have the bloch sphere. These two parameters are $\phi$ and $\theta$. $\phi$ represents the angle between the positive x axis, and the vector's projection onto the x-y plane.  $\theta$ represents the angle between the positive Z axis and the vector itself.

If you are familiar with a 3d polar coordinate system, this is exactly the same concept!

<img src="/images/blochSpheree.png" width="550">

**Figure 2.1: Bloch sphere coordinate system**

<br />

From the bloch sphere, the quantum state $\ket{\psi}$ can be written as such:

$$\ket{\psi} = cos(\frac{\theta}{2}) \ket{0} + e^{i \phi} sin(\frac{\theta}{2}) \ket{1}$$

where $0 \le \theta \le \pi$ and $0 \le \phi \le 2 \pi$

Okay, well now that we have this, what else can we know? well, we can write the point on the sphere as we would in any 3d coordinate system of (x, y, z) using the parameters $\phi$ and $\theta$:

$\ket{\psi}$ on the unit sphere (x, y, z) is: ( $sin \theta cos \phi$ , $sin \theta sin \phi$ , $cos \theta$ )

This is exactly the same as a 3d polar coordinate system!

This point has a corresponding unit vector (as do all points on the surface of the bloch sphere, as its radius is 1), that can be written: 

< $sin \theta cos \phi$ , $sin \theta sin \phi$ , $cos \theta$ >

We can now imagine that we have 2 axes we would like to measure along. Each one will be represented by a vector, which I will arbitrarily name X and Y. X and Y are two different axes along which we can measure the state of a qubit! Or in my case, as I've been talking about throughout the rest of the project, X and Y are two different axes along which to the spins of particles A or B!

If I measure X, the probability of measuring Y to be in the same state as X is the **scalar projection** of X onto Y; that is, we are basically looking at how much of X is shared Y each other. Intuitively, this makes sense in relating to probability of the states being the same.

In terms of unit vectors, the scalar projection is simply given by $cos \theta$. However, $cos \theta$ exists on [-1, 1], which is not ideal as we are looking at probability; we want probability to be on [0, 1]. Furthermore, we want opposite states to have no overlap; -1 (spin down) and 1 (spin up) are opposite states, but if we keep the formula as is, we are saying that they are basically the same vector but opposite directions. So we can normalize it as such:

$$P(same) = \frac{1+cos \theta}{2}$$
$$ \\{ P | 0 \le P \le 1 \\} $$

Now notice the form of this equation; it looks a lot like one of the half angle trigonometric identities: 

$$cos^2 \theta = \frac{1+cos(2 \theta)}{2}$$

So we can re-write:

$$P(same) = cos^2 (\frac{\theta}{2})$$

So for example: on particle A, given 2 axes X and Y separated by an angle $\theta$, the probability that Y is measured to be the same state as X is $cos^2 (\frac{\theta}{2})$!

The same can be said about an X and Y on particle B!

Now that you understand where this cosine relationship comes from, you can [return to the original document!](1_Project_Summary.md#blochAnchor).

