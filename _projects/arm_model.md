---
layout: single
classes: wide
title: "Modeling Arm Motion in 2-D"
excerpt: "I developed a biomechanically accurate model of the human arm that estimates effort costs."
header:
teaser: /images/arm_model/Muscle_diagram.png
collection: project
permalink: /projects/arm_model
author_profile: true
share: true
---

This project was aimed at developing an arm model that is capable of predicting the metabolic cost of arm reaching. By comparing neuromechanical proxies to metabolic cost we can determine if the are good approximations of effort.

The model uses movement trajectory from collected subject data to determine position and inverse kinematics and dynamics to solve for joint angles and joint torques. After determining joint torques multiple minimization functions determine muscle forces. From there an estimation of active state, neural drive to the muscles, and energetic expenditure is calculated. From there these are compared to metabolic cost.

Below shows the R^2 values for the commone proxies in a slightly older version of the model. We see that the energetics model has the best predictions of metabolic cost, with neural drive in a close second. A very common proxy, joint torque and joint torque squared, both to fairly poorly when compared to metabolic cost.

A full guide to the musculoskeletal model is shown in the pdf.

<embed src="https://gbruening.github.io/git_d3_test/">

<object data="/../images/arm_model/Full2.pdf" type="application/pdf" width = "240px" height="380px">
    <embed src="/../images/arm_model/Full2.pdf"> </embed>
</object>