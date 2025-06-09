# ECS 189G Final Project  
**Enhancing Adversarial Robustness of NanoGPT**

## Overview
This repository contains our ECS 189G final project code and notebook exploring adversarial defenses for a miniature GPT (NanoGPT) in open-domain dialogue. We implement and evaluate:
- **Dynamic Attention Rectification (DAR)**
- **Low-Rank Adaptation (LoRA)**
- **Adversarial Reasoning Thinking Module (ARTM)**
- **Positional-Adaptive Attention Fusion (PAAF)** (old method not included in final report; preserved here for posterity)

and compare their effects - both alone and in combination - on the AdvGLUE adversarial benchmarks.

## Files
```
- dev_ann.json                   # AdvGLUE adversarial examples
- dial.txt                       # DailyDialog training examples
- ECS189G_Final_Project.ipynb    # end-to-end Colab notebook: data prep, training variants, eval
- README.md                      # this file
```

## Usage
Clone this repo, open ECS189G_Final_Project.ipynb, and replace the first line with the directory of this project in your computer. Then run the rest of the notebook.

## Results
Example adversarial-accuracy on AdvGLUE:

| Model Variant            | Acc (%) |
| ------------------------ | ------- |
| NanoGPT (base)           | 44.38   |
| NanoGPT + LoRA           | 44.96   |
| NanoGPT + DAR            | 41.21   |
| NanoGPT + LoRA + DAR     | 42.65   |
| NanoGPT + PAAF           | 18.44   |
| NanoGPT + LoRA + PAAF    | 38.62   |
| **NanoGPT + ARTM**       | 42.36   |
| **NanoGPT + LoRA + ARTM**| 43.23   |

## Authors
**Sujash Barman**, **Jeffrey Wang**, & Team  
ECS 189G, Spring 2025