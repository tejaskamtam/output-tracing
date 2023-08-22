# Plans

Goal: visualize activations to explain important neurl circuits (directed chains of neurons) in output selection.

Implement using PyTorch weight extraction. E.g.: https://youtu.be/Fw9VqcqFP_c?si=Za-ifH9BQKXgJZvZ

Visualize using Manim library developed by 3Blue1brown

Work on an example using MNIST, using 2 64-node (or 128) hidden layers with activations.
Then project into a graph using Manim an visualize chains that correspond to activations resulting in >0.5 accuracy.

Log stats of each chain on each test instance and visualize. Hypothesis: There may be neural chains that always contribute to bad activations or output encodings - we an prune these to increase performance.

Question: How to check for causality of outputs based on weights?
1. There may be some direct scaling of weights that repreent how much they contribute to the final softmax
2. Zero ablation - explained in causal scrubbing paper (https://www.lesswrong.com/posts/JvZhhzycHu2Yd57RN/causal-scrubbing-a-method-for-rigorously-testing) - we corrupt activations, then reintroduce ativations and check differences in outputs and weights



