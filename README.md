# ⚡ Neural Network Visualizer

Watch a Multilayer Perceptron (MLP) learn **live in your browser** — no server, no dependencies, no build step. A single `index.html` file.

![what you see](https://img.shields.io/badge/features-decision%20boundary%20%C2%B7%20loss%20curve%20%C2%B7%20neuron%20activations-6d8bff)

## Features
- 🌀 **Live decision boundary** — the background is the network's prediction over the whole input space; watch it morph as it learns (temporally smoothed for buttery animation)
- 📉 **Loss curve** dropping in real time + live accuracy / epoch stats
- 🧠 **Network diagram** — neurons glow by activation, edges colored red (negative) / green (positive) by weight
- 📊 4 datasets: Spiral, Circle, Clusters, XOR
- 🔧 Tweak architecture (2 hidden layers), learning rate, and training speed live

## Deploy via Git (GitHub Pages)
```bash
git init
git add index.html README.md
git commit -m "neural network visualizer"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```
Then: repo **Settings → Pages → Source: `main` branch / root** → your site is live at `https://<your-username>.github.io/<your-repo>/`

Any static host works too (Netlify, Vercel, Cloudflare Pages) — just drop the folder in.

## Run locally
Just open `index.html` in a browser. Or: `python3 -m http.server` → http://localhost:8000

## How it works
Plain JS implements forward pass (tanh hidden, sigmoid output, binary cross-entropy) + full backprop, trained with vanilla SGD. Everything renders on `<canvas>`.
