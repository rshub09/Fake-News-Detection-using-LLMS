<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
   
</head>

<body>

<h1>LLM-Based Fake News Classification with Chain-of-Thought Reasoning</h1>

<p>
This project investigates the use of large language models (LLMs) for automated fact-checking
and truthfulness classification of political statements using the LIAR dataset.
The system evaluates both binary and multi-class classification settings using
Chain-of-Thought (CoT) prompt engineering with GPT-4.
</p>

<hr>

<h2>Project Objective</h2>
<p>
The primary goal of this project is to assess whether reasoning-enabled LLM prompts
can improve classification performance on complex, real-world political text data.
The project focuses on transparency, interpretability, and reproducibility of LLM-based predictions.
</p>

<hr>

<h2>Dataset</h2>
<p>
The project uses the <strong>LIAR dataset</strong>, a widely used benchmark dataset for
fake news and political fact-checking research.
It consists of short political statements labelled across six levels of truthfulness:
</p>

<ul>
    <li>Pants-fire</li>
    <li>False</li>
    <li>Barely-true</li>
    <li>Half-true</li>
    <li>Mostly-true</li>
    <li>True</li>
</ul>

<p>
The dataset is split into training, validation, and test sets and is provided in TSV format.
Preprocessing steps include text cleaning, normalisation, and schema alignment.
</p>

<hr>

<h2>Methodology</h2>
<ol>
    <li>Load and preprocess political statements from the LIAR dataset</li>
    <li>Construct Chain-of-Thought prompts tailored to binary or multi-class classification</li>
    <li>Invoke GPT-4 via API with controlled decoding parameters</li>
    <li>Parse and normalise LLM outputs into structured class labels</li>
    <li>Evaluate predictions using standard classification metrics</li>
    <li>Analyse and visualise results across classes</li>
</ol>

<hr>

<h2>LLM and AI Implementation</h2>
<p>
Large language models are integrated as the core classification engine.
Rather than using traditional supervised classifiers, this project leverages
GPT-4 as a zero-shot / few-shot reasoning model.
</p>

<p>
Key AI implementation details include:
</p>

<ul>
    <li>Chain-of-Thought prompt engineering to encourage step-by-step reasoning</li>
    <li>Schema-controlled label generation to reduce output ambiguity</li>
    <li>Temperature and token constraints to improve determinism</li>
    <li>Response caching to reduce redundant API calls and improve efficiency</li>
    <li>Automated experiment runners for binary and multi-class settings</li>
</ul>

<p>
LLM outputs are programmatically parsed, validated, and compared against ground-truth labels.
This design allows for systematic evaluation of LLM reasoning performance
in a controlled experimental framework.
</p>

<hr>

<h2>Evaluation</h2>
<p>
Model performance is evaluated using:
</p>

<ul>
    <li>Accuracy</li>
    <li>Precision</li>
    <li>Recall</li>
    <li>F1-score</li>
    <li>Confusion matrices and class-wise analysis</li>
</ul>

<p>
Results are visualised to highlight strengths and weaknesses of LLM-bas
