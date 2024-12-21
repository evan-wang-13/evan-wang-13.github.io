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

A tangential discussion is the concept of strongly-held weak beliefs vs. weakly-held strong beliefs. Strongly-held weak beliefs are hypotheses that may not push the envelope super far from established knowledge, but we can be relatively confident in that belief. These beliefs are more foundational than ground-breaking. Weakly-held strong beliefs are beliefs that are "hot takes" but have low confidence.
Some examples: Matt has a strongly-held weak belief that for a domain like music, randomness and luck can significantly determine how popular a song is-merit and quality is not a fool-proof determiner of success.
Arvind has a weakly-held strong belief that the issues with LLM evaluation (contamination, prompt sensitivity, robustness, and more that we will get into in this post) are not fixable, and thus future work should be oriented towards replacing benchmarking rather than fixing it.

Usual discourse pits these against each other-which should an aspiring researcher follow? This may be true at an individual level, but they certainly are not mutually exclusive at a larger scale. Both types of beliefs are important to have in the marketplace of ideas: diversity here is healthy.

Matt describes himself as someone having strongly-held weak beliefs, while Arvind considers himself as having weakly-held strong beliefs.

## Evaluations are Everything

- Data Leakage and the [ping-pong theorem](https://projecteuclid.org/journals/statistical-science/volume-21/issue-1/Classifier-Technology-and-the-Illusion-of-Progress/10.1214/088342306000000060.full). You can read more about data leakage [here](https://reproducible.cs.princeton.edu/).
- Crucially, there is often a mismatch between training loss, performance evaluation, and what actually matters post-deployment. For example, say we are using some classifcation model. We might use maximum likelihood estimation to find the models' parameters, some misclassification rate to evaluate the model, but in practice, what truly matters is a particular cost-weighted misclassification rate. It should be imperative to take time and ensure coherency here.

For a particularly illuminating example, let's look at the discussion over emergent abilities of LLMS.

2022 paper evaluated LLM performance on some popular benchmarks as a function of parameter size. Contrary to traditional scaling laws, models achieve random performance up to a certain scale, then improves-sharply and unpredictably. This is a pretty crucial finding. If models truly exhibit emergent abilities, that makes predicting their predictive power, abilities, and risks much harder. A bunch of steps and research would probably need to follow.

But! A 2023 [paper](https://arxiv.org/abs/2304.15004) suggests this is not the full picture. "emergent abilities seem to appear only under metrics that nonlinearly or discontinuously scale any model's per-token error rate."

Results of testing this hypothesis are shown below, taken from their paper.
For completeness, the first column follows a simple mathematical model, where they assume cross entropy loss decreases monotonically with scale, and thus per-token probability of selecting the right token asymptotes towards 1.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/emergentMirage.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

When we go from a non-linear metric, where the scoring tends to be more binary with a strict threshold, to a non-linear metric, the emergent pattern seems to disappear. So what is the "correct" metric to use? It probably doesn't matter that much-ultimately whatever allows us to make the best predictions for the desired task. But, overall, this recasts emergence from a model property to something about how we evaluate/consider knowledge.

<!-- > We do not grow absolutely, chronologically. We grow sometimes in one dimension, and not in another, unevenly. We grow partially. We are relative. We are mature in one realm, childish in another.
> —Anais Nin -->
