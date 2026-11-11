---
title: Intro to Quantum Mechanics
date: 2026-08-20 17:27:00 -0400
categories: [Physics]
math: true
tags: [physics]
---

Quantum mechanics has always felt like a miracle to me. No matter how many times I read about it or watch someone explain it, I seem to end up with more questions than answers.

I keep this blog as an exercise in self-explanation: an attempt to put my confusion into words, follow the questions that puzzle me, and see whether I can understand a little more than I did yesterday.

The conversation that follows never happened. Hypatia of Alexandria was a historical philosopher and mathematician; Juliet belongs to Shakespeare. They came from entirely different worlds and never had the chance to meet. For the sake of this little experiment, however, I have invited them both into the same room.

Perhaps history will object. Let's begin anyway.

*An imaginary dialogue between Hypatia of Alexandria and Juliet -*

## Probability is Uncertainty

Professor Hypatia tossed a fair coin into the air, caught it, and placed it beneath his palm.

"To be head or not to be?" she asked. 

Juliet glanced at her hand.

“ 50% chance of heads，50% chance of tails."

Hypatia smiled："Is the coin uncertain, Juliet, or are you?"

Juliet frowned. "What do you mean?"

"The coin has already settled. It is either heads or tails. There is no half-head, half-tail coin hiding beneath my palm. Your fifty percent describes your uncertainty because you cannot see it. The uncertainty belongs to your knowledge, not necessarily to the coin itself."

She continued:

"This is an example of what we call epistemic uncertainty — uncertainty arising from a lack of knowledge. In the idealized world of classical mechanics, if we knew every initial condition and every force acting on the coin, Newton's laws would, in principle, allow us to predict its final position."

Juliet considered this for a moment.

"So the coin is perfectly certain, and I am simply ignorant?"

"Precisely. At least, that is how our classical picture works."

Hypatia lifted her hand and revealed the coin.

"Now, Juliet, suppose we replace this coin with something much smaller. An electron, perhaps. Would you expect the same reasoning to hold?"

"Why wouldn't it? Surely an electron must also have a definite state, even if we cannot observe it."

Hypatia smiled.

"An entirely reasonable assumption. Unfortunately, nature has a rather inconvenient habit of challenging reasonable assumptions."

She walked towards the blackboard.

"Let us visit the laboratory."

### Two Path Experiment

Hypatia drew a simple experiment.

```
                   ┌── Slit 0 ──┐
[Electron Source] ─┤            ├──► [Screen X]
                   └── Slit 1 ──┘
 ```                                     

"Imagine firing electrons towards a barrier with two openings. Beyond the barrier is a screen that records where each electron arrives."

Juliet nodded.

"Simple enough. Each electron must pass through either slit 0 or slit 1."

"That is exactly what our classical intuition would suggest. Now, suppose we close slit 1 and leave slit 0 open. We measure the probability of an electron arriving at a particular region of the screen, X, and obtain 25%. We repeat the experiment with only slit 1 open, and obtain another 25%."

Hypatia wrote:

$$
P_0(X)=25%
$$

$$
P_1(X)=25%
$$

"Now, if both slits are open, what would you expect?"

Juliet answered without hesitation.

"Fifty percent! We simply add the two probabilities."

 $$P_{\text{total}} = P_0 + P_1 = 25\% + 25\% = 50\%$$

"Exactly. If an electron has already chosen one path, opening the other should not affect its journey, assuming the two paths do not otherwise influence one another."

She explained that scientists had performed experiments with electrons, even sending them through the apparatus one at a time.

Each electron arrived at the screen as a localized detection event — a single dot. Yet as more and more electrons accumulated, they gradually formed an interference pattern.

And at certain positions on the screen, such as X, the probability of detecting an electron could become zero when both slits were open, even though each slit alone allowed electrons to reach that region.

Juliet stared at the blackboard.

"Wait. Are you telling me that opening another path can make an electron less likely to arrive somewhere?"

"Indeed. The electron does not disappear. The two paths simply change the distribution of where it can be detected. At some positions they reinforce each other; at others, they cancel."

Juliet looked unconvinced.

"But how can two possibilities cancel each other? Surely probabilities cannot be negative."

"An excellent observation."

Hypatia picked up her chalk.

"You are right that ordinary probabilities are non-negative. But quantum mechanics does not add probabilities directly when different alternatives remain coherent. Instead, it adds something called **probability amplitudes**."

She wrote: $$P(X)=\lvert A_0(X)+A_1(X)\rvert^2$$

"Unlike ordinary probabilities, probability amplitudes can carry a phase. They can be positive, negative, or even complex numbers. Let's use a simplified example."

$$
A_0(X)=+0.5
$$

$$
A_1(X)=-0.5
$$

"Consider each path separately."

$$
P_0(X)=|+0.5|^2=25%
$$

$$
P_1(X)=|-0.5|^2=25%
$$

"But when both paths are available, we first add their amplitudes, then take the squared magnitude."

$$
\begin{aligned}
P(X)&=|A_0(X)+A_1(X)|^2\
&=|0.5-0.5|^2\
&=0
\end{aligned}
$$

Juliet looked at the equation again.

"So two nonzero contributions can add up to zero?"

"Precisely. This is called **destructive interference**."

Hypatia continued:

"Classical waves can also interfere. Think of two water waves meeting: depending on their relative phases, they can reinforce or cancel one another. But the remarkable thing about quantum mechanics is that even individual electrons, detected as particles, gradually build up a wave-like interference pattern."

She added:

"Of course, we should not imagine an electron as literally being a tiny water wave. The probability amplitude is a mathematical object used to predict the outcomes of experiments."

Juliet remained silent for a moment.

"Then perhaps the electron really does take both paths?"

Hypatia considered her question.

"That is a useful way to begin imagining it, but we must be careful. In the standard quantum mechanical description, both possible paths contribute to the final outcome through their probability amplitudes. We can no longer simply picture the electron as a tiny classical ball that secretly chose one path before leaving the source."

"But what if we put a detector beside each slit and find out which path the electron takes?"

"Then the interference disappears. When the experimental arrangement records which-path information, the alternatives no longer interfere in the same way. Notice that this does not require a human being to look at the detector. A physical interaction is enough."

Juliet sighed.

"I thought I understood what a probability was."

Hypatia laughed.

"Perhaps it is time to learn a new mathematical language."

## The State as a Vector

Juliet looked at the equations on the blackboard.

"If we cannot simply describe the electron as having secretly chosen one path, how do we describe its state before measurement?"

"Let us borrow an idea from ordinary geometry: the vector."

Hypatia drew a two-dimensional coordinate system.

"In familiar geometry, a vector can be expressed as a combination of two basis vectors."

$$
\vec{v}=x\vec{e}_x+y\vec{e}_y
$$

"The two basis vectors, \(\vec{e}_x\) and
\(\vec{e}_y\), represent two independent directions.
The coefficients \(x\) and \(y\) tell us how much
of each direction contributes to the vector.

Quantum mechanics uses a similar mathematical structure.

For our simplified two-path system, let's call the
two possible states \(|0\rangle\) and \(|1\rangle\):"

$$
|0\rangle =
\begin{pmatrix}
1\\
0
\end{pmatrix},
\qquad
|1\rangle =
\begin{pmatrix}
0\\
1
\end{pmatrix}
$$

"These are called **basis states**. They represent
the two possible paths in our simplified model.

A quantum state can then be expressed as a linear
combination of the two:

$$
|\psi\rangle
=
\alpha|0\rangle+\beta|1\rangle
=
\begin{pmatrix}
\alpha\\
\beta
\end{pmatrix}
$$

This is the **Quantum State Vector**."

Juliet examined the expression.

"So \(\alpha\) and \(\beta\) tell us the probabilities of finding the electron in either path?"

"Not quite. They are probability amplitudes, not probabilities themselves. They can even be complex numbers."

"A two-level quantum system is often called a qubit in quantum information. The qubit is the quantum system; this vector describes the state it occupies."

Juliet looked at the vector again.

"So the state is like an arrow pointing somewhere between the two axes?"

"That is a helpful geometric analogy, but do not take it too literally. The state vector lives in an abstract mathematical space, not in the ordinary physical space around us. Its components can also be complex numbers, so it is not always an ordinary arrow that we can draw on paper."

Hypatia paused.

"But there is something even more interesting. A quantum state contains more information than a list of probabilities."

### The Born Rule & Measurement

Juliet interrupted.

"Then how do we actually obtain a definite result? When we measure an electron, we never observe a mysterious mixture of two paths. We detect one outcome or the other."

"That brings us to the Born Rule."

Hypatia wrote:

$$
P(0)=|\alpha|^2
$$

$$
P(1)=|\beta|^2
$$

"The Born Rule tells us how to turn probability amplitudes into actual measurement probabilities. If our two-state system is properly normalized, then:"

$$
|\alpha|^2+|\beta|^2=1
$$

"For example, consider a qubit in the following state:"

$$
|\psi\rangle=
\frac{1}{\sqrt{2}}|0\rangle+
\frac{1}{\sqrt{2}}|1\rangle
$$

"Measuring it in the basis of $$\lvert 0\rangle$$ and $$\lvert 1\rangle$$ gives us a 50% probability of obtaining either result."

Juliet nodded.

"All right. But what happens at the moment of measurement?"

Hypatia put down her chalk.

"According to the standard textbook description, when we measure the system, we obtain one definite outcome. If the result is 0, the state is updated to $$\lvert 0\rangle$$. If the result is 1, it is updated to $$\lvert 1\rangle$$."

She wrote:

$$
\alpha|0\rangle+\beta|1\rangle
\xrightarrow{\text{measurement}}
\begin{cases}
|0\rangle & \text{with probability }|\alpha|^2\\
|1\rangle & \text{with probability }|\beta|^2
\end{cases}
$$

"This is commonly called *wavefunction collapse*."

Juliet looked puzzled.

"But why does measurement cause the state to collapse?"

Hypatia smiled.

"That is a much harder question than it first appears. Measurement is a physical interaction between a quantum system and a measuring apparatus, not simply a human being looking at something. The standard formalism tells us how to calculate the possible outcomes and update the state after one is obtained. But precisely how a single definite outcome emerges is part of what physicists call the *measurement problem*."

Juliet leaned back.

"So even after all these equations, we still don't entirely agree on what measurement means?"

"Indeed. Learning physics does not always mean eliminating mysteries. Sometimes it means discovering that the mystery is much deeper than we first imagined."

### The Sign(h) no pun intended

Hypatia returned to the blackboard.

"Before we move on, Juliet, I want to show you one more thing. Suppose I give you two different quantum states."

$$
|\psi_+\rangle=
\frac{1}{\sqrt{2}}|0\rangle+
\frac{1}{\sqrt{2}}|1\rangle
$$

$$
|\psi_-\rangle=
\frac{1}{\sqrt{2}}|0\rangle-
\frac{1}{\sqrt{2}}|1\rangle
$$

"Now, if we measure either state in the $$\bigl(\lvert 0\rangle,\lvert 1\rangle\bigr)$$ basis, what probabilities do you expect?"

Juliet calculated.

"Fifty percent for 0, fifty percent for 1. For both states."

"Correct. So, are these two states identical?"

Juliet hesitated.

"They have the same probabilities. I would be tempted to say yes."

"Look closer. One has a plus sign, the other a minus sign."

Juliet frowned.

"But when we square the amplitudes, the signs disappear!"

"Exactly. In this particular measurement, you cannot distinguish them. But they are not the same quantum state."

Hypatia drew two more symbols:

$$
|+\rangle=
\frac{1}{\sqrt{2}}(|0\rangle+|1\rangle)
$$

$$
|-\rangle=
\frac{1}{\sqrt{2}}(|0\rangle-|1\rangle)
$$

"Imagine a different measuring apparatus, one that recombines the two paths and measures in this new basis. The first state will give you the (+) outcome, while the second will give you the (-) outcome."

Juliet's eyes widened.

"So even though they have identical probabilities in the first measurement, they behave differently in another?"

"Precisely. That difference comes from their relative phase."

Hypatia continued:

"Remember, probability amplitudes can carry phase information. The relative phase between different components determines how they interfere. The plus and minus signs in our example represent two different relative phases."

Juliet stared at the equations.

"Then a quantum state is not merely a list of probabilities."

"Now you understand why we need the state vector. It preserves information that an ordinary probability distribution would throw away."

For the first time, Juliet began to see that the mathematics was not merely a complicated way of expressing uncertainty. It was describing something richer.

## The Schrödinger Equation

Juliet looked at the state vector once more.

"Professor, if a quantum state contains all this information, does it change over time? What happens if we simply leave the electron alone?"

"An excellent question. An isolated quantum system continues to evolve even when we are not measuring it."

Hypatia wrote the final equation on the blackboard:

$$\hat{H}|\psi(t)\rangle
$$

"This is the Schrödinger Equation. It describes how a quantum state evolves over time."

She pointed to the Hamiltonian, $$(\hat{H})$$.

"It is the operator associated with the system's total energy, and it determines the rule governing this evolution. For a simple two-state system, you can imagine the state vector changing direction in an abstract state space, somewhat like a rotating arrow. The analogy is not literal, of course; the electron is not physically spinning around in our familiar space."

Juliet looked at the equation.

"So the Schrödinger Equation describes how the state evolves, while the Born Rule tells us what probabilities we obtain when we measure it?"

Hypatia nodded.

"Exactly. Between measurements, an isolated system follows a continuous and mathematically predictable evolution. Measurement, in the standard textbook description, is governed by a different rule."

Juliet smiled faintly.

"I think I finally have a map. I am not sure I know how to navigate it yet."

"That," said Hypatia, "is a rather good place to begin."

## Beyond This Blog

Hooray! We've reached the end of this little introduction to quantum mechanics.

Am I any less confused than when I started? Well... I'm not entirely sure. Sometimes it feels as though quantum mechanics flows into one side of my brain and straight out the other.

I still have so many questions. Why does measurement change the state of a quantum system? What exactly happens when a wavefunction collapses? How do these seemingly abstract mathematical ideas translate into real-world applications?

Perhaps I haven't really understood quantum mechanics yet. But at least I've learned a few new languages to describe the things I don't understand: superposition, probability amplitudes, state vectors, and the Schrödinger equation.

Maybe that's what this blog is really about. Not necessarily arriving at answers, but learning to ask better questions.

