# ML_Final_Project

## Launch in Google Colab
Use this link [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cdm106/ML_Final_Project/blob/main/Final_Project_CDM_1.ipynb) to launch the jupyter notebook in Google Colab. 

## Requirements
The notebook needs to access to the accompaning `Movie.xlsx` file. I suggest downloading it and uploading it to the runtime environment (instructions for upload in notebook) once you launch the notebook.

The Neo4J database tool call relies on a "sandbox" database which is not persitant.  I can keep the one running for ~7 days (till 5/8/2025), after that I will need to start a new one and send you the credentials via Discord. 

# Notebook Description
The Google Colab notebook is a pipeline that demonstrates the merger of generative AI with agentic AI, e.g. tool calling. This is a very simple example that mimicks the "pipeline" of Reasoning WithOut Observation (ReWOO) 1,2 . Note that encapsulating the true nature of ReWOO in a single notebook would be prohibitive in the time allowed. Instead, I attempt to capture the spirit of ReWOO through a "very simple" example.

In true ReWOO, there are three interwoven modules:

Planner
Worker
Solver
The planner breaks the problem down step by step, here I emulate this with instructing the Large Language Model on how to break down the steps to generate a Cypher query from natural language.

The worker uses tools to verify each step, in this case the program utilizes an API to interact with a graph database tool along with the solver to verify the n th  step, generation of Cypher code from natural language.

The solver integrates all of the subtasks and corresponding evidence to generate a conclusion. In this notebook, the solver takes the database tool response along with the original natural language question to generate a concluding natural language answer to the users questions.

This is a companion to the survey report: The Interplay of Reasoning and Agentic Artificial Intelligence: An Introduction Survey, which is also uploaded to the GitHub Repository.
