# ⚡ Neural Network Visualizer

Watch a Multilayer Perceptron (MLP) learn **live in your browser** — no server, no dependencies, no build step. A single `index.html` file.

![what you see](https://img.shields.io/badge/features-decision%20boundary%20%C2%B7%20loss%20curve%20%C2%B7%20neuron%20activations-6d8bff)

## Features
- 🌀 **Live decision boundary** — the background is the network's prediction over the whole input space; watch it morph as it learns (temporally smoothed for buttery animation)
- 📉 **Loss curve** dropping in real time + live accuracy / epoch stats
- 🧠 **Network diagram** — neurons glow by activation, edges colored red (negative) / green (positive) by weight
- 📊 4 datasets: Spiral, Circle, Clusters, XOR
- 🔧 Tweak architecture (2 hidden layers), learning rate, and training speed live

## How it works
Plain JS implements forward pass (tanh hidden, sigmoid output, binary cross-entropy) + full backprop, trained with vanilla SGD. Everything renders on `<canvas>`.
