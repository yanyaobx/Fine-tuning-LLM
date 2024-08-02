# Physically Accurate Code Generation with Large Language Models for Industrial Control Systems

## Project Overview

This project aims to improve code generation for Industrial Control Systems (ICS) by integrating Large Language Models (LLMs) with a physics-based simulation. The objective is to produce an accurate testbed environment model that uses real-world sensor data to provide evaluative feedback on the generated code. This feedback loop allows for iterative code revision until the code is verified to be correct within the robotics simulator, such as Gazebo.

## Team Members

- **James McClure** (Masters of Embedded and Cyber-Physical Systems, University of California, Irvine, jhmcclur@uci.edu)
- **Ting Husn (Ted) Wu** (Masters of Embedded and Cyber-Physical Systems, University of California, Irvine, thwu2@uci.edu)
- **Yanyabobo (Ember) Xue** (Masters of Embedded and Cyber-Physical Systems, University of California, Irvine, yanyaobx@uci.edu)

## Abstract

The goal of this project is to create a pipeline that can automatically produce, improve, and implement PLC code, ensuring a closed-loop system from creation to use. By understanding how the testbed operates, generating code with LLMs, calibrating the simulator with real-world inputs, and optimizing the LLM based on feedback, we aim to improve the efficiency and robustness of the code.

## Keywords

OpenPLC, Gazebo, Large Language Models, Industrial Control Systems, Physics-based Simulation, Code Generation, Sensor Data Calibration

## Table of Contents

1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Setup](#setup)
4. [Usage](#usage)
5. [Results](#results)
6. [Conclusion](#conclusion)
7. [Acknowledgements](#acknowledgements)
8. [References](#references)
9. [Files](#files)

## Introduction

Programmable Logic Controllers (PLCs) play a critical role in industrial automation and control of cyber-physical systems. Traditional PLC software development is resource-intensive and time-consuming. This project leverages LLMs to streamline the process, using an automated pipeline to generate, test, and refine code until it meets operational and quality assurance standards.

## Objectives

- **Overall Objectives**: Develop an automated end-to-end programming pipeline for generating and validating PLC code using LLMs.
- **Specific Objectives for the Spring Quarter**:
  - Identify necessary hardware and software
  - Familiarize with structured text programming language and Gazebo simulator
  - Set up and train LLM (LLama-3)
  - Implement a feedback loop using OpenPLC and Gazebo
  - Integrate subsystems into a cohesive pipeline

## Setup

### Software Packages Used

- **Large Language Model**:
  - Ollama, Llama3, Google Colab, Hugging Face, Unsloth
- **OpenPLC Runtime**:
  - WSL2 VM (Ubuntu 22.04.4 LTS), OpenPLC Runtime Version 3, Visual Studio, Python 3.11.9
- **Gazebo**:
  - Gazebo Simulator Harmonic, Mosquitto, Autodesk Fusion 360

### Hardware Packages Used

- **Testbed**:
  - Fischertechnik Training Factory Industry 4.0 9V kit (Siemens S7-1500 PLC)

## Usage

### Running the Project

2. **Install Dependencies**:
   Follow the instructions in the `setup.sh` script to install all required software packages.

3. **Configure the Environment**:
   Set up your environment variables and configurations as outlined in the `config.md` file.

### Workflow

1. **Input Prompt**:
   - Provide a text file containing system requirements and specifications.
   
2. **Generate Code**:
   - The LLM generates structured text code based on the input prompt.

3. **Syntax Checking**:
   - The generated code is checked using OpenPLC.

4. **Simulation**:
   - The code is tested in a Gazebo simulation using real-world sensor data.

5. **Feedback Loop**:
   - Feedback from OpenPLC and Gazebo is used to iteratively refine the code.

6. **Deployment**:
   - Finalized code is uploaded to the Siemens S7-1500 PLC for real-world testing.

## Results

Our current progress includes designing and training a LoRa to optimize structured text code generation, demonstrating the use of OpenPLC for syntax checking, and developing a basic prototype for our master Python script. We have also created a customizable plugin for Gazebo and a simulation model that integrates with our pipeline.

## Conclusion

We have made significant strides towards developing an end-to-end automated pipeline for PLC code generation. Over the summer, we plan to integrate our subsystems fully and begin testing on our FischerTechnik testbed. By Fall Quarter, we aim to demonstrate the full pipeline's functionality from start to finish.

## Acknowledgements

We are grateful to Professor Mohammad Al Farque, Mohamad Habib Fakih, and Rahul Sirivas Dharmaji at the University of California, Irvine, for their guidance and support. We also thank Professor Quoc-Viet Dang and the University of California, Irvine, for financial support and Dr. Gustavo Quiros Araya from Siemens for technical assistance.

## References

1. Soliman, A., Shaheen, S. & Hadhoud, M. (2024). Leveraging pre-trained language models for code generation. Complex Intell. Syst. 10, 3955–3980. [DOI](https://doi.org/10.1007/s40747-024-01373-8)
2. "Leveraging Large Language Models (LLMs) for Efficient Coding: A Deep Dive into Code Generation and its Impact on the BFSI Industry," LinkedIn. [Link](https://www.linkedin.com/pulse/leveraging-large-language-models-llms-efficient-coding-deep-an)
3. Fakih, M. et al. (2024). LLM4PLC: Harnessing Large Language Models for Verifiable Programming of PLCs in Industrial Control Systems. In 46th International Conference on Software Engineering. [DOI](https://doi.org/10.1145/3639477.3639743)

## Files

- **LLM4PLC_LoRA.ipynb**: This Jupyter Notebook documents the independent training process for the Large Language Model (LLM) conducted by Yanyabobo (Ember) Xue.
- **Spring Project Report.pdf**: This is the group project report detailing the objectives, methodologies, and results of the project "Physically Accurate Code Generation with Large Language Models for Industrial Control Systems."

## Project Report

You can find the detailed project report [here](./Spring%20Project%20Report.pdf).
