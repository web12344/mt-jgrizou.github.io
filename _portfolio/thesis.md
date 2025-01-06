---
title: "PhD Thesis"
collection: projects
type: "Project"
permalink: /projects/thesis
date: 2017-12-15
location: "Inria / University of Bordeaux"
---

# An intriguing AI paradigm: interactive learning from unlabeled instructions
*Last update: January 2019*

*Providing you neither know the game of chess nor the French language, could you learn the rules of chess from a person speaking French? In machine learning, this problem is usually avoided by freezing one of the unknowns (e.g. chess or french) during a calibration phase. During my PhD, I tackled the full problem and proposed an innovative solution based on a measure of consistency of the interaction. We applied our method to human-robot and brain-computer interaction and studied how humans solve this problem. This work was awarded a PhD price handed by Cédric Villani (2010 Fields Medal).*

![Illustration of consistency. The same dataset is labelled according to 3 different tasks. The left labelling is the most consistent with the structure of the data. How do we measure this?](https://jgrizou.com/wp-content/uploads/2022/11/bci_intuition.jpg)

---

### Content

### Approach
*Can an agent learn a task from human instruction signals without knowing the meaning of the communicative signals? Can we learn from unlabeled instructions?* [1](https://jgrizou.com/projects/thesis/#fn1)

The problem resembles a chicken-and-egg scenario: to learn the task you need to know the meaning of the instructions (interactive learning), and to learn the meaning of the instructions you need to know the task (supervised learning).

However, a common assumption is made when tackling each of the above problems independently: the user providing the instructions or labels is acting consistently with respect to the task and to its own signal-to-meaning mapping. In short, the user is not acting randomly but is trying to guide the machine towards one goal and using the same signal to mean the same things. The user is consistent.

![Illustration of consistency. The same dataset is labelled according to 3 different tasks. The left labelling is the most consistent with the structure of the user signals - indicating the user was probably teaching that task.](https://jgrizou.com/wp-content/uploads/2022/11/bci_intuition.jpg)

---

Hence, by measuring the consistency of the user signal-to-meaning mapping with respect to different tasks, we are able to recover both the task and the signal-to-meaning mapping, solving the chicken-and-egg problem without the need for an explicit calibration phase. And we do so while avoiding the combinatorial explosion that would occur if we tried to generate hypotheses over the joint [task, signal-to-meaning] space, most prevalent when the signals are continuous.

Our contribution is a variety of methods to measure the consistency of an interaction, as well as a planning algorithm based on the uncertainty of that measure. We further proposed methods to scale this work to continuous state domains, infinite numbers of tasks, and multiple interaction frame hypotheses. We further applied these methods to a human-robot learning task using speech as the modality of interaction and to brain-computer interfaces with real subjects.

I am currently working on a simple and visual explanation of this research. In the meantime, please refer to the videos and documents in the [additional resources section](https://jgrizou.github.io/website/projects/thesis/#additional-resources).

---

### Team
PhD advisors: [Manuel Lopes](https://scholar.google.com/citations?user=kqkq_coAAAAJ&hl=fr&oi=ao) and [Pierre-Yves Oudeyer](http://www.pyoudeyer.com/).

BCI collaborators: [Iñaki Itturate](http://people.epfl.ch/inaki.iturrate) and [Luis Montesano](http://webdiis.unizar.es/~montesan/web/).

---

### Projects

### Online Demo
I am currently designing a web application to demonstrate the concept of self-calibrating interfaces. A preliminary version of the challenge is available online as a puzzle game: [Open Vault Challenge](http://discourse.cri-paris.org/t/introduction-to-the-open-vault-challenge/201) and more details are available here: [arxiv paper](https://arxiv.org/pdf/1906.02485.pdf).

The demo takes the form of a challenge to open a vault. The vault is secured by a 4-digit code that can be typed via a simple user interface on a screen. You have access to videos of a user entering the code into the interface and can watch it as much as required. The challenge is to crack the code, open the vault, and collect its content.

![Staffs and students trying to crack the code.](https://jgrizou.com/wp-content/uploads/2022/11/vault_people.jpeg)

---

There are 5 levels of increasing complexity, and from level 3 onward the interface is built using the calibration-free interface paradigms presented on this page, making it difficult for an observer to infer what the user is typing as the meaning associated with each button/action is decided on the fly by the human.

#### Resources
1. **The Open Vault Challenge–Learning how to build calibration-free interactive systems by cracking the code of a vault.** Grizou, Jonathan (2019). *International Joint Conferences on Artificial Intelligence.* [pdf](https://arxiv.org/pdf/1906.02485.pdf) [project](https://jgrizou.github.io/website/projects/thesis)

---

### Application to Brain-Computer Interfaces
In brain-computer interfaces (BCI), an explicit calibration phase is typically required to build a decoder that translates raw electroencephalography (EEG) signals from the brain of a user into meaningful instructions. By applying our method to BCI, we remove the need for a calibration phase.

The experimental setup is shown below. The user has to guide an agent towards a specific location of its choosing on the grid. The user informs the agent by thinking yes or no after each movement. The user’s brain activity is recorded and used as our unlabeled feedback signal. Similar setups are used to help persons with handicaps to spell.

![A grid is displayed on the screen. The user wants the green dot to move towards the red square.](https://jgrizou.com/wp-content/uploads/2022/11/bci_setup-768x362.png)

---

A calibration procedure would run for a fixed period of interaction, say 400 movements of the green dot, before the user can actually start controlling the device. With our method, the system is able to estimate when sufficient evidence has been accumulated and can solve a first task after only 85 iterations in the example below case.

![Diagram of the experimental setup](https://jgrizou.com/wp-content/uploads/2022/11/bci_self_vs_calib-768x357.png)

---

The method has been evaluated in closed-loop online experiments with 8 users. The results show that it is possible to have a usable BCI control from the beginning of the experiment without any prior calibration. Furthermore, comparisons with simulations and previous results obtained using standard calibration hint that both the quality of recorded signals and the performance of the system were comparable to those obtained with a standard calibration approach.

#### Resources
1. **Exploiting task constraints for self-calibrated brain-machine interface control using error-related potentials.** Iturrate, I., Grizou, J., Omedes, J., Oudeyer, P., Lopes, M., et al. (2015). *PloS one.* [pdf](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0131491) [github](https://github.com/flowersteam/self_calibration_BCI_plosOne_2015)
2. **Calibration-Free BCI Based Control.** Grizou, J., Iturrate, I., Montesano, L., Oudeyer, P.-Y., & Lopes, M. (2014). *International AAAI Conference on Artificial Intelligence.* [pdf](https://hal.archives-ouvertes.fr/hal-00984068/PDF/grizou2014calibration.pdf) [poster](https://github.com/jgrizou/publications/tree/master/paper/conference/2014_aaai)
3. **Interactive Learning from Unlabeled Instructions.** Grizou, J., Iturrate, I., Montesano, L., Oudeyer, P.-Y., & Lopes, M. (2014). *Conference on Uncertainty in Artificial Intelligence (UAI).* [pdf](https://hal.archives-ouvertes.fr/hal-01007689/PDF/grizou2014interactive.pdf) [poster](https://github.com/jgrizou/publications/tree/master/paper/conference/2014_uai)

---

### Application to Human-Robot Interaction
Our first demonstration of this work involved a pick-and-place robot that had to identify the cube configuration the user had in mind. The user provided feedback instructions (correct/incorrect) with their voice. Thanks to our approach, the user could use any word desired to mean correct or incorrect, e.g., ‘dog’ for *correct* and ‘cat’ for *incorrect*, which worked as well as ‘yes’ and ‘no’.

![Pick and place demo](https://www.youtube.com/embed/FoIFTQZc9vM?controls=1&rel=0&playsinline=0&modestbranding=0&autoplay=0&enablejsapi=1&origin=https%3A%2F%2Fjgrizou.com&widgetid=1)

---

Example of interaction. The robot performs an action and I provide feedback on the action according to its optimality towards building a specific cube configuration I have in mind. I use my voice to provide the feedback, and the robot does not know initially which sounds I use to mean correct or incorrect. Not my best video 🙂

