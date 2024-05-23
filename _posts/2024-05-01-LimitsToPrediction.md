---
layout: post
title: Limits to Prediction-Biggest Takeaways
date: 2024-04-29
description: What I learned from my favorite class at Princeton. Will continue to update as I parse through my notes.
# tags: formatting links
# categories: sample-posts
---

This spring, I took my favorite class at Princeton: the seminar [Limits to Prediction](https://msalganik.github.io/soc555-cos598J_s2024/), taught by Arvind Narayanan and Matt Salganik. lecture-discussion format where both professors, along with students, would be able to respond to the presented material. The topics, open discussions, and view-altering takeaway made this an eye-opening experience.

## Meta-Level: Choosing What to Learn/Research

- This involves a prediction task: what will be super important that is not receiving enough attention already?

## Evaluations are Everything

- Data Leakage and the ping-pong hacking theorem
- Mismatch between training loss, performance evaluation, and what actually matters post-deployment. For example, for a classification model, we might use maximum likelihood estimation to find the models' parameters, some misclassification rate to evaluate the model, but in practice, what matters is some cost-weighted misclassification.
- LLM- emergent abilities or a product of eval metric?

<!-- > We do not grow absolutely, chronologically. We grow sometimes in one dimension, and not in another, unevenly. We grow partially. We are relative. We are mature in one realm, childish in another.
> —Anais Nin -->
