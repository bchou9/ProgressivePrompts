# Progressive Prompts

This repo includes an original implementation of Anastasia Razdaibiedina, Yuning Mao, Rui Hou, Madian Khabsa, Mike Lewis and Amjad Almahairi. ["Progressive Prompts: Continual Learning for Language Models without Forgetting"](https://openreview.net/pdf?id=UJTgQBc91_), 2022.

## :boom: Introduction
We introduce Progressive Prompts – a novel Continual Learning (CL) approach for language models. Our
method is inspired by progressive networks, but is significantly more memory-efficient - it
only learns a fixed number of tokens, or prompt, for each new task. Learning a prompt to adapt
language models on a single downstream task was introduced in prompt tuning (Lester et al., 2021),
and was shown to match the performance of full model finetuning while training <0.01% of the
parameters. In Progressive Prompts, we learn a separate prompt for each incoming task and sequentially concatenate it with previously learned prompts. Importantly, we share input tokens across all
tasks and progressively prepend new prompts while keeping previous prompts frozen (see Figure 1).
Our method can: 1) alleviate catastrophic forgetting by preserving the knowledge acquired in previous prompts, and 2) transfer knowledge to future tasks by sequentially learning new prompts given
previous ones. We also introduce a new technique for prompt embedding reparameterization (Li
& Liang, 2021). We show that by passing the prompt embeddings through a residual MLP we can
stabilize prompt tuning and improve its performance.


![Progressive Prompts schematics](/images/illustration.png)
Figure: *Illustrating our proposed method **Progressive Prompts** and contrasting it with a simple
adaptation of progressive networks using prompt tuning. In the simple adaptation of progressive
networks we learn a separate prompt and repeat the frozen input embeddings for each new task.
This setup requires repeating input tokens for each task. In Progressive Prompts we use the same
input and progressively append new prompt for each new task. Prior task prompts are not modified
by the addition of new prompts.*

## :open_file_folder: What's in this repository

## :wrench: Installation

## :zap: How to run 
