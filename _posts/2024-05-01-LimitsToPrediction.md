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

- Choosing what to focus on in learning and research is a prediction task in and of itself. What will be super important in the next few years (or decades) that is not receiving enough attention already?
- Strongly-held weak beliefs vs. weakly-held strong beliefs. Strong-held weak beliefs are stances that may not push the envelope super far from established knowledge, but we can be relatively confident in that belief. These beliefs are more foundational than ground-breaking. Weakly-held strong beliefs are beliefs that are "hot takes" but have low confidence.
  Both types of beliefs are important to have in the marketplace of ideas: diversity here is healthy. Matt describes himself as someone having strongly-held weak beliefs, while Arvind considers himself as having weakly-held strong beliefs.

## Evaluations are Everything

- Data Leakage and the ping-pong hacking theorem
- Mismatch between training loss, performance evaluation, and what actually matters post-deployment. For example, for a classification model, we might use maximum likelihood estimation to find the models' parameters, some misclassification rate to evaluate the model, but in practice, what matters is some cost-weighted misclassification.
- LLM- emergent abilities or a product of eval metric?

<!-- > We do not grow absolutely, chronologically. We grow sometimes in one dimension, and not in another, unevenly. We grow partially. We are relative. We are mature in one realm, childish in another.
> —Anais Nin -->
