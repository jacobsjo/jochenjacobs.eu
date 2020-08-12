---
layout: post
title: "Dynamic VR-Rendering camera vergence and separation"
tagline: "TAP 2019 Paper and Bachelor Thesis"
categories: project
author: "Jochen Jacobs"
---
For my bachelor thesis in computer-science at TU-Berlin I have investigated the possibility of using dynamic camera adjustments based on eye-sensor data. The idea was that this would help reduce the [Vergence-Accommodation-Confluct](https://medium.com/vrinflux-dot-com/vergence-accommodation-conflict-is-a-bitch-here-s-how-to-design-around-it-87dab1a7d9ba). However I found that this method does not work - possibly because of added nausea from the movement of the camera or wrong eye sensor data.

![Adjustment Methods](/assets/blog_assets/keep-it-simple/adjustments.jpg)

There is also a paper that developed from this research, presented at ACM SAP 2019 and published in ACM TAP 2019. You can find both the paper and the bachelor thesis below.

## Keep It Simple: Depth-based Dynamic Adjustment of Rendering for Head-mounted Displays Decreases Visual Comfort
Jochen Jacobs, Xi Wang and Mark Alexa - TU-Berlin - Published in TAP 2019, September 2019, Issue 3 (Special Issue on SAP 2019)

DOI: [10.1145/3353902](https://doi.org/10.1145/3353902)

PDF: [here](/assets/blog_assets/keep-it-simple/keepitsimple.pdf)

#### Abstract

Head-mounted displays cause discomfort. This is commonly attributed to conflicting depth cues, most prominently between vergence, which is consistent with object depth, and accommodation, which is adjusted to the near eye displays.

It is possible to adjust the camera parameters, specifically interocular distance and vergence angles, for rendering the virtual environment to minimize this conflict. This requires dynamic adjustment of the parameters based on object depth. In an experiment based on a visual search task, we evaluate how dynamic adjustment affects visual comfort compared to fixed camera parameters. We collect objective as well as subjective data. Results show that dynamic adjustment decreases common objective measures of visual comfort such as pupil diameter and blink rate by a statistically significant margin. The subjective evaluation of categories such as fatigue or eye irritation shows a similar trend but was inconclusive. This suggests that rendering with fixed camera parameters is the better choice for head-mounted displays, at least in scenarios similar to the ones used here.

## Bachelor Thesis: Dynamic Control of Interocular Distance and Vergence Angle in Rendering for Head-Mounted Stereo Displays
Jochen Jacobs - Jul 05, 2019

PDF: [here](/assets/blog_assets/keep-it-simple/BachelorThesis.pdf)

#### Abstract
In recent years, head-mounted displays have become increasingly popular. However, the well known vergence-accommodation conflict causes significant amount of discomfort. Some research has proposed to dynamically adjust the rendering to change the eye vergence needed for the currently focused object to match the accommodation.

This thesis uses camera vergence and separation to change the eye vergence based on the users gaze. To determine the gaze depth, a probabilistic algorithm is proposed that uses both measured eye-convergence and scene geometry. An experiment is conducted to determine whether the dynamic vergence and separation changes reduce fatigue. Fatigue is measured objectively (pupil diameter, pupil diameter variance, eye movement speed, blink rate, and reaction time) and subjectively using a questionnaire. The experiment is also used to evaluate the quality of the depth estimation algorithm.

Results show, that the output of the proposed algorithm to estimate the eye vergence depth is better than simple raycasting and ray intersection algorithms. However the objective evaluation of the adjustment method shows that it does not help reduce fatigue but in fact increases discomfort. The subjective evaluation was inconclusive but trends go into the same direction.
