# Network Intrusion Detection System

ML-based IDS for identifying and classifying network intrusions using the KDD Cup 99 dataset. Compares Decision Tree and Neural Network approaches for real-time threat detection. Built as a cybersecurity project at VIT Chennai.

## The Problem

Network intrusion detection sits at the core of operational security — you need a system that can process high-volume traffic in real time, flag anomalies, and ideally tell you what kind of attack it is. The tradeoff is between accuracy and interpretability: a model that catches more attacks but can't explain why is harder to trust in a production security context.

## Dataset

**KDD Cup 99**
- Standard benchmark for network IDS research
- Four attack categories:
  - **DoS** (Denial of Service) — overwhelm resources to prevent legitimate access
  - **Probe** — reconnaissance attacks scanning for vulnerabilities
  - **R2L** (Remote to Local) — unauthorised access from a remote machine
  - **U2R** (User to Root) — privilege escalation attacks
- Plus normal (non-attack) traffic
- Features: protocol-based, content-based, and host-based traffic metrics

## Models Compared

### Decision Tree
- Produces human-readable classification rules
- Useful in a SOC (security operations) context where analysts need to understand why something was flagged
- Fast inference — important for real-time traffic
- Weakness: can overfit on specific attack signatures, less generalisation to novel variants

### Neural Network
- Better generalisation across unseen attack types
- Handles high-dimensional feature space better
- Higher detection rate on U2R and R2L (rarer, harder attack types)
- Weakness: black-box — harder to audit and explain

**Key finding:** Decision Trees are more useful when you need explainable alerts. Neural Networks outperform on volume and novelty. A hybrid (rule-based pre-filter + neural network for anomalies) is the practical production approach.

## Repository Contents

| File | Description |
|---|---|
| `INTRUSION DETECTION IN A NETWORK USING MACHINE LEARNING AND NEURAL NETWORK-1.pdf` | Research paper |
| `INTRUSION_DETECTION_IN_A_NETWORK_USING_MACHINE_LEARNING_AND_NEURAL_NETWORK[1].pdf` | Reviewed research paper |
| `Intrusion-Detection-in-a-Network-using-Machine-Learning-and-Neural-Network-Approaches.pptx` | Presentation slides |

## Stack

Python · scikit-learn · Neural Networks · pandas
