---
layout: project
title: "Virtual Driven Oscillator Laboratory"
description: "A Python computational physics project modeling free, damped, and driven harmonic oscillations, including numerical integration, resonance analysis, and quality-factor extraction."
order: 1
image: assets/images/resonance_curve
technologies:
  - Python
  - NumPy
  - SciPy
  - Matplotlib
  - Computational Physics
---

## Overview

Virtual Driven Oscillator Laboratory is a Python computational extension of the free, damped, and driven oscillator physics studied in Cornell PHYS 2214 Lab 2.

The project progresses through three models:

1. Free undamped oscillation
2. Damped free oscillation
3. Driven damped oscillation and resonance

## Features

- Analytical and numerical modeling of free oscillations
- Damped oscillation classification and decay analysis
- Numerical integration using `scipy.integrate.solve_ivp`
- Resonance frequency sweep
- Steady-state amplitude measurement
- Resonance bandwidth analysis
- Quality-factor calculation from resonance
- CSV data output and Matplotlib visualization

## Technical Implementation

The project solves second-order oscillator differential equations numerically by rewriting them as coupled first-order equations. NumPy is used for numerical data handling, SciPy for differential-equation integration, and Matplotlib for visualization.

The driven model performs a frequency sweep to construct a resonance curve and estimates the quality factor from the half-power bandwidth.

## Code Repository

[View the full code repository](YOUR-GITHUB-REPOSITORY-URL)
