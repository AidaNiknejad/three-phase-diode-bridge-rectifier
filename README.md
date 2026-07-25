# Three-Phase Six-Pulse Diode Bridge Rectifier

A MATLAB/Simulink project focused on modeling and analyzing a three-phase six-pulse diode bridge rectifier with a resistive-inductive load.

## Project Overview

The purpose of this project is to investigate the operation of an uncontrolled three-phase diode bridge rectifier and compare the simulation results with theoretical relationships.

The rectifier converts a balanced three-phase AC voltage into a six-pulse DC output voltage.

The project analyzes:

- Load voltage and current
- Source phase current
- Current through one bridge diode
- Reverse voltage across the diode
- Average and RMS current values
- Diode conduction losses
- Agreement between theoretical and simulated results

## System Parameters

| Parameter | Value |
|---|---:|
| Line-to-line RMS voltage | 480 V |
| Source frequency | 60 Hz |
| Load resistance | 100 Ω |
| Load inductance | 15 mH |
| Diode forward voltage | 0.8 V |
| Diode on-state resistance | 0.001 Ω |
| Simulation time | 0.1 s |
| Sample time | 5e-5 s |

## Simulink Model

The model was developed using Specialized Power Systems blocks, including:

- Three-Phase Source
- Three-Phase V-I Measurement
- Universal Bridge
- Series RLC Branch
- Current Measurement
- Voltage Measurement
- Multimeter
- Product
- Powergui
- To Workspace blocks

The Universal Bridge contains six diodes. At each instant, two diodes conduct, and the conducting pair changes every 60 electrical degrees.

## Theoretical Analysis

The average output voltage of an ideal three-phase diode bridge is approximately:

```text
Vo_avg = 1.35 × VLL_rms
