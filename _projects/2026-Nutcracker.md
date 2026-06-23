---
layout: project
title: "Nutcracker Design Project: Statics & Mechanics"
description: Designed a functional nutcracker to meet specified force and usability constraints using statics, moment equilibrium, and beam deflection analysis. The project included force modeling, geometric design, and cross-section optimization.
order: 2
image: assets/images/nutcracker_diagram_1.png
---

## Overview

This project focused on designing a usable nutcracker that could generate the required cracking force while satisfying geometric, material, and deflection constraints. The design used static equilibrium, moment analysis, and beam deflection calculations to determine the required handle geometry and material selection.

| Parameter | Value |
|---|---:|
| Required force to crack nut | 2220 N |
| Applied user force | 500 N |
| Nut radius | 1 cm |
| Maximum allowed deflection | ≤ 2% of beam length |
| Selected material | Structural steel |
| Elastic modulus | 200 GPa |

---

## Part 1: Force and Geometry Analysis
The first stage of the design used moment equilibrium about the nutcracker pin. This point was selected because it allowed the applied handle force and the nut reaction force to be related through their moment arms.

The distance from the pin to the nut was defined as \(x_1\), while the distance from the pin to the applied user force was defined as \(x_1 + x_2\). Using the required nut-cracking force and the maximum applied user force. Taking the moment about the pin would allow me to find the two values of x_1 and x_2 such that it would balance the forces sufficiently. The handle length was selected so that the applied force could generate enough moment to crack the nut. With these lengths found I used the results to create the diagram below.

This geometry produced a usable design because the user only needed to apply 500 N at each handle while maintaining a 1 cm nut gap.

![Nutcracker geometry diagram]({{ "/assets/images/nutcracker_diagram_1.png" | relative_url }}){: .project-image }

---

## Part 2: Beam Deflection and Material Selection

The second stage of the design analyzed the elastic deflection of the nutcracker handles. The objective was to select a beam cross-section and material that would keep the vertical deflection below 2% of the beam length while remaining as mass-efficient as possible.

The design requirements were:

1. Determine the location of maximum elastic deflection in the handles.
2. Select a beam cross-section and material that limits vertical deflection to less than 2% of the handle length.
3. Present the final nutcracker geometry and beam model.

  Deflection Analysis

For this part 2, I assume the nutcracker to be modeled as shown in the diagram in the bottom of the page. This allows for the equations from the appendix to be applied. 
**Structural Modeling and Beam Selection**

**(a) Free-Body Diagram and Loading Assumptions**

A free-body diagram was created to model the nutcracker handle under the applied loading condition. The system was simplified to include three primary external forces:

1. The applied user force of 500 N.
2. The reaction force from the nut.
3. The reaction force at the pin support.

Using the given handle geometry, the beam was modeled using the beam deflection appendix from *Statics and Mechanics of Materials* by Ferdinand P. Beer. The location of maximum deflection was modeled as:


x_m = √((L² - a²) / 3)


where:

* (L) is the length of the handle.
* (a) is the distance parameter defined by the loading geometry.
* (x_m) is the location of maximum deflection.

Using the known handle length and:

a = 2 cm

the location of maximum deflection was calculated as:

x_m = 3.80 cm

This value was used to identify the critical location where the handle experiences its largest displacement under the applied load.

**(b) Maximum Deflection Requirement and Material Selection**

The maximum allowable deflection was limited to 2% of the handle length. Therefore, the allowable deflection was defined as:

Y_max = 0.02L

Using the same beam deflection appendix, the maximum deflection equation was written as:

Y_max = [P a (L² - a²)^(3/2)] / [9√3 E I L]

where:

* (P) is the applied force.
* (a) is the geometric loading parameter.
* (L) is the handle length.
* (E) is the elastic modulus of the material.
* (I) is the area moment of inertia of the cross-section.

Since the applied force, handle length, and loading geometry were already defined, the remaining design variables were the material stiffness and cross-sectional stiffness. These are represented by (E) and (I), respectively. Therefore, the design problem was reduced to selecting a material and cross-section that provided a sufficient value of (EI).

The deflection equation was rearranged to solve for the required stiffness relationship:

EI = [P a (L² - a²)^(3/2)] / [9√3 L Y_max]

Since:

Y_max = 0.02L

the required area moment of inertia for a selected material can be written as:

I_req = [P a (L² - a²)^(3/2)] / [9√3 E L (0.02L)]

This equation shows that the required cross-section depends heavily on the elastic modulus (E) of the material. A material with a larger elastic modulus requires a smaller area moment of inertia to satisfy the same deflection limit.

Structural steel was selected because it has a high elastic modulus and resists elastic deformation effectively under the applied loading conditions. For structural steel, the elastic modulus was taken as:

E = 200 GPa

Using this value of (E), the required area moment of inertia was compared against available W-beam sections. Based on this comparison, the selected section was:

W18 × 106

The W18×106 section was selected because it satisfied the deflection requirement while providing an effective balance between stiffness and mass. Therefore, the final beam selection was based on both the material stiffness of structural steel and the geometric stiffness provided by the selected W-beam cross-section. The W18×106 section served as an analytical reference for evaluating bending and deflection. These results informed the required geometry and material properties of the final nutcracker design.

![Final nutcracker beam model]({{ "/assets/images/nutcracker_diagram_2.png" | relative_url }}){: .project-image }

---

## Concepts Used

- Static equilibrium
- Moment analysis
- Beam deflection modeling
- Material selection
- Cross-section optimization
- Structural steel design
- Engineering design constraints

---

## Key Result

The final design satisfied the required nut-cracking force while keeping the handle deflection below the allowable 2% limit. The project demonstrated how statics and mechanics of materials can be used to convert force requirements into a functional mechanical design.
