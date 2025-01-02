---
title: "Chemobot"
collection: projects
type: "Project"
permalink: /projects/chemobot
date: 2019-01-01
location: "University of Glasgow"
---

# Chemobot  
**Applying machine learning to the exploration of physicochemical systems**  

*Last update: January 2019*

How can AI help make discoveries on the bench in a chemistry lab? How can chemical systems help devise better AI algorithms? I explored these questions with the team I led in the [Cronin Group](https://www.chem.gla.ac.uk/cronin/). The group's cutting-edge knowledge combined with my experience from the developmental sciences allowed us to bring innovative ideas to the field, including the use of active learning, curiosity-driven exploration, and human comparative studies.

![Compilation of droplet behaviors – one of the systems we studied.](https://jgrizou.com/images/chemobot/droplet_behaviors.gif)

![Compilation of robotic platforms designed by the team.](https://jgrizou.com/images/chemobot/robotic_platforms.jpg)

## Approach  

I grew frustrated that most AI research was done on simulated environments. I wanted to see this technology used in the real world on systems we do not ourselves design nor understand – that is, not even on robots.  

The physical sciences seem fitting. In physics, chemistry, or biology, an important part of everyday research is to understand yet unknown systems. Scientists devise experiments and build instruments to query these systems with the aim to model, and later predict, their evolution.  

But because such systems are not yet fully understood, or are massively parallel, they cannot be simulated. There is no cheating with the physical sciences; you cannot speed up experiments, you cannot be 100% sure that you are controlling the right experimental variables, and you do not know the right answer. That is all the fun of it.  

This is in sharp contrast with the simulation, big data, and controlled robotic problems AI algorithms are designed on and for. If we ought to bring AI advances to experimental research in the labs, we need to drop the habit of thinking that experiments are free, unlimited, and well defined.  

Interestingly, a subfield of robotics, called [developmental robotics](https://en.wikipedia.org/wiki/Developmental_robotics), imposes similar constraints. Their aim is to build a robot that can learn like a child. A child has real-world constraints; it has limited time to interact with the world and has no complete built-in knowledge of the world around it. From its own body to modern objects like smartphones and bikes, a child has to learn it all in a few years by interacting with the world. To do so, a child constantly devises its own experiments to test the world around it, much like a scientist in its lab.  

As it turns out, I pursued my PhD under the supervision of [Pierre-Yves Oudeyer](https://www.pyoudeyer.com/), one of the pioneers of this field. Once I connected the dots, an ocean of research directions opened to bring principles from developmental robotics into the physical sciences. How can a laboratory robot be curious and devise its own questions about new systems? How could it learn a hierarchy of skills to produce increasingly more complex molecules autonomously? How could such machines learn from and collaborate with scientists? Could maturational constraints and the concept of embodiment help leverage the exploration power of algorithms on natural systems?  

Hence came the decision to join a chemistry lab for a postdoc.  

## Team  

[Lee Cronin](https://en.wikipedia.org/wiki/Lee_Cronin_(chemist)), a pioneer in the digitization of chemistry, welcomed me into [his lab](https://www.chem.gla.ac.uk/cronin/) and gave me the responsibility of an internal team to explore these questions.  

![The Chemobot team from 2015-2018 within the Cronin group, University of Glasgow. Missing is Kevin Donkers.](https://jgrizou.com/images/chemobot/team_photo.jpg)

The team was composed of Lee Cronin (PI), Jonathan Grizou (me), Abhishek Sharma, Jan Szymanski, James W. Taylor, Juan Manuel Parrilla Gutierrez, Laurie J. Points, Vasilios Duros, Sergio Martin Marti, Graham Keenan, and Kevin Donkers—a mix of chemists, computer scientists, and material scientists.  

The main challenge resided in good communication between team members. Chemists had to understand the limitations of computers in making sense of data, as well as the limitations of robots in manipulating things. Computer scientists (me above all) had to understand that chemistry is hard, requires time, and that not everything can be created at will.  

## Projects  

### Curiosity-driven exploration of oil-in-water droplets  

We developed a chemical robotic discovery assistant equipped with a curiosity algorithm (CA) that was set to explore the states a complex chemical system can exhibit, searching for novelty. This differs from optimization scenarios where a global target is defined beforehand.  

![The Dropfactory robot is able to perform, record, and clean 8 droplet experiments in parallel.](https://jgrizou.com/images/chemobot/dropfactory_robot.jpg)

By applying the CA-robot to the study of self-propelling multicomponent oil-in-water droplets, we observed an order of magnitude more variety of droplet behaviors than possible with a random parameter search given the same budget.  

We demonstrated that the CA-robot enabled the discovery of a sudden and highly specific response of droplets to slight temperature changes.  

![Summary of the results.](https://jgrizou.com/images/chemobot/summary_results.png)

Once the temperature dependence was discovered, six modes of self-propelled droplet motion were identified and classified using a time-temperature phase diagram and probed using a variety of techniques, including NMR, which allowed the design of a payload release system triggered by temperature.  

![Effect of temperature on droplet motion.](https://jgrizou.com/images/chemobot/temperature_effect.png)

**Resources**  
1. [A curious formulation robot enables the discovery of a novel protocell behavior](https://advances.sciencemag.org/content/6/5/eaay4237). Grizou, J., Points, L. J., Sharma, A., & Cronin, L. (2020). *Science Advances*.  
