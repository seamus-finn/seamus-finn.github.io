---
layout: project
title: "Sprint Training Advisor"
description: "A rule-based Python tool that generates sprint and strength sessions from a date-based training progression, applies soreness-based modifications, supports schedule shifts, and logs completed sessions."
technologies:
  - Python
  - CSV
  - datetime
  - pathlib
  - Rule-based logic
---

## Overview

Sprint Training Advisor is a Python-based tool built to streamline my sprint-training workflow.

The program calculates sprint, strength, tempo, endurance, and rest sessions from a date-based training progression. It can also modify the planned session based on soreness in the hips, calves, hamstrings, core, or quads.

## Features

- Calculates training sessions from a season start date
- Supports tempo, acceleration, top-speed, endurance, and rest days
- Uses week-specific special-endurance running sessions
- Provides soreness-based workout substitutions
- Includes indoor and rainy-day alternatives
- Includes recovery, mobility, core, and foot-strength options
- Logs completed workouts and notes to a CSV file
- Allows the workout log to be viewed, added to, edited, or deleted through Python
- Supports schedule shifting after missed sessions

## Technical Implementation

The program uses Python dictionaries to organize training sessions, soreness alternatives, lift progressions, and recovery options. It uses `datetime` to calculate the current training week and day from a selected date, and uses CSV file handling to store completed workout entries and notes.

## Code Repository

[View the full code repository](https://github.com/seamus-finn/sprint-training-advisor)
