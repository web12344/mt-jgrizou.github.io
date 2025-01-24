---
title: "Chemobot"
collection: projects
type: "Project"
permalink: /projects/chemobot
date: 2019-01-01
location: "University of Glasgow"
---

# Applying Machine Learning to the Exploration of Physicochemical Systems

_Last update: January 2019_

*How can AI help make discoveries on the bench in a chemistry lab? How can chemical systems help devise better AI algorithms?*  
I explored those questions with the team I led in the [Cronin Group](http://www.chem.gla.ac.uk/cronin/). The group’s cutting-edge knowledge combined with my experience from the developmental sciences allowed us to bring innovative ideas to the field, including the use of active learning, curiosity-driven exploration, and human comparative studies.

## Videos

### Droplets Compilation
<iframe width="640" height="360" src="https://www.youtube.com/embed/RC_nc0P_crc" frameborder="0" allowfullscreen></iframe>  
_Compilation of droplet behaviors – one of the systems we studied._

### Droplet Robots Compilation
<iframe width="640" height="360" src="https://www.youtube.com/embed/_pAtu3atYN8" frameborder="0" allowfullscreen></iframe>  
_Compilation of robotic platforms designed by the team._

---

## Content

- [Approach](#approach)
- [Team](#team)
- [Projects](#projects)
  - [Curiosity-driven exploration on a laboratory robot](#dropfactory)
  - [Active learning in crystallization experiments](#human-vs-robots)
  - [Hierarchical exploration of gold nanoparticles](#nanobot)
  - [Physical environment as an experiment variable](#flowbot)
  - [AI to better understand self-propelled droplets](#surfbot)
  - [Black-box optimization of self-propelled droplets](#dropbot)
- [Resources](#additional-resources)
- [Personal Notes](#personal-notes)

---

## Approach

I grew frustrated that most AI research was done on simulated environments. I wanted to see this technology used in the real world on systems we do not ourselves design nor understand – that is, not even on robots.

The physical sciences seem fitting. In physics, chemistry, or biology, an important part of everyday research is to understand yet unknown systems. Scientists devise experiments and build instruments to query these systems with the aim of modeling, and later predicting, their evolution.

This is in sharp contrast with simulation, big data, and controlled robotic problems AI algorithms are designed on and for.  
[1] If we ought to bring AI advances to experimental research in labs, we need to drop the habit of thinking that experiments are free, unlimited, and well-defined.

### Connecting Developmental Robotics and Physical Sciences

A subfield of robotics, called [developmental robotics](https://en.wikipedia.org/wiki/Developmental_robotics), imposes similar constraints. Their aim is to build a robot that can learn like a child. This opened an ocean of research directions to bring principles from developmental robotics into the physical sciences.

---

## Team

![The Chemobot Team](https://jgrizou.com/wp-content/uploads/2022/11/team.png)  
_The Chemobot team from 2015–2018 within the Cronin group, University of Glasgow. Missing: Kevin Donkers._

The team was composed of Lee Cronin (PI), Jonathan Grizou (me), Abhishek Sharma, Jan Szymanski, James W. Taylor, Juan Manuel Parrilla Gutierrez, Laurie J. Points, Vasilios Duros, Sergio Martin Marti, Graham Keenan, and Kevin Donkers. A mix of chemists, computer scientists, and material scientists.

---

## Projects

### Curiosity-Driven Exploration of Oil-in-Water Droplets

<iframe width="640" height="360" src="https://www.youtube.com/embed/bY5OoRBJkf0" frameborder="0" allowfullscreen></iframe>  
The [Dropfactory robot](https://github.com/croningp/dropfactory) is able to perform, record, and clean 8 droplet experiments in parallel.

By applying the CA-robot to the study of self-propelling multicomponent oil-in-water droplets, we observed an order of magnitude more variety of droplet behaviors than possible with a random parameter search given the same budget. We discovered a sudden and highly specific response of droplets to slight temperature changes.

---

**[More information and tools](https://github.com/croningp)**  

## Summary of Results

![Summary of the results](https://jgrizou.com/wp-content/uploads/2022/11/dropfactory_result-768x600.png)

<figcaption>
Summary of the results. Left: (A) % of explored space. CA explored 3.3 times more than random. (B, C) Observations made by each method for each repeat; each scatter dot represents a single droplet experiment. CA (B) leads to a greater variety of observations than random (C). Right: Effect of temperature. (D) Number of experiments with a speed faster than 3 mms-1. A change of only ca. 4.4°C led to a significant difference in the observed droplet behaviours when using the CA (395 vs 93, p=0.005), which is not observed when using random (28 vs 19, p=0.22). This is confirmed by (E) and (F) which show the distribution of observation. The CA enabled the discovery of the temperature effect.
</figcaption>

---

Once the temperature dependence was discovered, six modes of self-propelled droplet motion were identified and classified using a time-temperature phase diagram and probed using a variety of techniques including NMR, which allowed the design of a payload release system triggered by temperature. This work illustrates how target-free search can significantly increase the rate of unpredictable observations leading to new discoveries with potential applications in formulation chemistry.

### Video: Effect of Temperature on Droplet Motion

<iframe width="640" height="360" src="https://www.youtube.com/embed/80yAmBkzdmM?controls=1&rel=0&playsinline=0&modestbranding=0&cc_load_policy=0&autoplay=0" frameborder="0" allowfullscreen></iframe>

---

## Resources

1. **A curious formulation robot enables the discovery of a novel protocell behavior.**  
   Grizou, J., Points, L. J., Sharma, A. & Cronin, L. (2020). *Science Advances*.  
   [PDF](https://advances.sciencemag.org/content/6/5/eaay4237.full.pdf) | [DOI](https://doi.org/10.1126/sciadv.aay4237) | [Robot Design](https://github.com/croningp/dropfactory) | [Experiment Code](https://github.com/croningp/dropfactory_exploration) | [Analysis Code](https://github.com/croningp/dropfactory_analysis) | [Project](https://jgrizou.github.io/website/projects/chemobot#dropfactory)

---

## Human vs Robots

![Automated platform in the lab](https://jgrizou.com/wp-content/uploads/2022/11/hvr_pom.png)
![Experimental setup](https://jgrizou.com/wp-content/uploads/2022/11/hvr_platform.png)

The discovery of new gigantic molecules formed by self-assembly and crystal growth is challenging as it combines two contingent events: the formation of a new molecule and its crystallization. We constructed an automated workflow that can probe both events and employed it for a new polyoxometalate cluster which has a trigonal-ring type architecture.

### Representation of Methods

![Experimental method](https://jgrizou.com/wp-content/uploads/2022/11/hvr_diagram.png)  
Representation of the experimental method showing how the automated and bench work was done.

![Schematic diagram](https://jgrizou.com/wp-content/uploads/2022/11/hvr_method.png)  
Schematic diagram of the exploration methods. All experiments are performed on a crystallization robotic platform.

---

A critical constraint was that we could only perform 10 experiments per day. We ran the active learning in batches of 10 experiments, performing 10 iterations for a total of 100 experiments per method and repeat. This required 10 days and significant reagents to validate the approach for the first time. The results showed that the active learning algorithmic search increased the crystallization prediction accuracy to **82.4 ± 0.7%** compared to **77.1 ± 0.9%** from human experimenters given the same experimental budget.

### Results

![Prediction Accuracy](https://jgrizou.com/wp-content/uploads/2022/11/hvr_result.png)  
Average for the crystallization prediction accuracy between the classes of crystals and non-crystals for the three methods, using a RandomForest classifier.

---

## Additional Resources

1. **Intuition-enabled Machine Learning beats the Competition when Joint Human-Robot Teams perform Inorganic Chemical Experiments.**  
   Duros, V., Grizou, J., Sharma, A., Mehr, S.H.M., et al. (2019). *Journal of Chemical Information and Modeling*.  
   [PDF](https://pubs.acs.org/doi/pdf/10.1021/acs.jcim.9b00304) | [Journal](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.9b00304) | [Project](https://jgrizou.github.io/website/projects/chemobot#human-vs-robots)

2. **Human vs Robots in the Discovery and Crystallization of Gigantic Polyoxometalates.**  
   Grizou, J., Duros, V., Xuan, W., et al.

   
