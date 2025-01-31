---
title: "Self-calibrating code entering interface "
collection: projects
permalink: /projects/vault
date: 2019-08-01
excerpt: "A web-app to explain self-calibrating interfaces."
---

> **UPDATE:** The page below is deprecated and might be hard to understand without prior knowledge. Please read [https://arxiv.org/pdf/2212.05766.pdf](https://arxiv.org/pdf/2212.05766.pdf) for now.

## This interface can read your mind  
*Last update: August 2019*  

*"A web-app to explain self-calibrating interfaces."*

---

## Introduction

Below is a typical user interface. It is a code-entering device.  
- Look at the digit you want to type.  
- If it is yellow, click the yellow button.  
- If it is grey, click the grey button.  

The machine will figure out the digit you have in mind by elimination.

![Demo of interface](images/demo_1x2_2.gif)

With two big colored buttons, this interface is designed to remove most user choices and funnel you into standardized behavior. Designers use such approaches in apps like Instagram and Twitter to predict actions more easily.

But what if digital devices could adapt to your preferences? Below is the same interface, but the buttons have no predefined colors. You decide the buttons' colors in your mind, and the machine adapts on the fly.

---

## Examples of User Choices

| ![User 1](images/demo_3x3_fullpad_1.gif) | ![User 2](images/demo_3x3_fullpad_2.gif) | ![User 3](images/demo_3x3_fullpad_3.gif) |
|:---------------------------------------------:|:---------------------------------------------:|:---------------------------------------------:|
| User 1 choice                                 | User 2 choice                                 | User 3 choice                                 |

Notice how, once revealed, the color patterns on buttons are different for each user. This reflects their personal preferences. Each user typed in the same digit but they used the buttons differently to do so. Yet the machine was able to adapt, finding both what the user wanted to do (enter the digit 1) and how it was trying to do it (the colors associated to each button). I call these self-calibrating interfaces because they adapt to your preferences while you are using them. You will find below several options to play with these interfaces and gain a deeper understanding of how they work.

## Grasp it – look under the hood

For each version, a small explanatory text is provided along with a didactic video. If this is your first time, I recommend going through each version in order.

[Go to demo](https://jgrizou.com/projects/vault/demo)

### Grasp it – look under the hood

If you want to see how it works, I have built a little window into the machinery powering the interface. It provides detailed feedback about the current state of the machine. It also allows you to challenge the interface in complex ways. For example, I sometimes use these advanced versions to fool the machine into making a false prediction, or to select my actions such that it takes the longest possible time to identify a digit.

[Go to tutorial](https://jgrizou.com/contact/projects/vault/tuto)

### Wait but why?

Because I have consistently failed to explain what a self-calibrating interface does to other researchers, friends, or family in a few minutes. This web application is my attempt at explaining, showing, and getting people to feel what a self-calibrating interface does in one minute on my phone.

I also have the intuition that this technology can be useful. But I cannot figure out how on my own, I am too involved in the research and find it hard to think outside the box. By implementing this technology into an easy-to-share demonstration, I am hoping to reach a variety of people. And maybe one day someone will figure out a place to apply it for good. If you think of some application, feel free to [contact me](https://jgrizou.com/contact/).

### Resources

1. **The Open Vault Challenge – Learning how to build calibration-free interactive systems by cracking the code of a vault.**  
   Grizou, J. (2019). *International Joint Conferences on Artificial Intelligence.*  
   [pdf](https://arxiv.org/pdf/1906.02485.pdf)  
   [doi](https://doi.org/10.24963/ijcai.2019/942)  
   [project](https://jgrizou.github.io/website/projects/vault)

Detailed information, papers, and code available on [this project page](https://jgrizou.com/projects/thesis).

Feel free to [get in touch](https://jgrizou.com/contact/).

---

### Demo Images and Links

#### 2 buttons  
![2 buttons](images/demo_1x2_2-1.gif)  
[2 buttons demo](https://jgrizou.com/projects/vault/demo/1x2/)

#### 9 buttons  
![9 buttons](images/demo_3x3_fullpad_1.gif)  
[9 buttons demo](https://jgrizou.com/projects/vault/demo/3x3/)

#### Touch  
![Touch](images/demo_touch_1.gif)  
[Touch demo](https://jgrizou.com/projects/vault/demo/1x2/)

#### Draw  
![Draw](images/demo_draw_1.gif)  
[Draw demo](https://jgrizou.com/projects/vault/demo/1x2/)

#### Speak  
![Speak](images/demo_audio_1.gif)  
[speak demo](https://jgrizou.com/projects/vault/demo/1x2/)

#### Keyword  
![Keyword](images/demo_keyboard_1.gif)  
[Keyword demo](https://jgrizou.com/projects/vault/demo/1x2/)

