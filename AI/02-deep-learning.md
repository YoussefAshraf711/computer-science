[العربي](./02-deep-learning_ar.md)

# <a name="-2-deep-learning"></a>🤖 Chapter 2: Deep Learning (DL)

## 1. What is it?
Deep Learning is a subfield of ML focused on neural networks with many layers that learn hierarchical feature representations. It's the backbone of modern state-of-the-art models in vision, language, and audio.

## 2. What does the specialist do?
A DL specialist designs neural architectures (CNNs, RNNs, Transformers), configures training regimes (optimizers, LR schedules), manages GPU/TPU training, applies transfer learning and model compression, and tunes models for production constraints.

## 3. Sub-domains
- Convolutional Neural Networks (CNNs)  
- Recurrent Neural Networks and sequence models (RNN, LSTM)  
- Transformers and attention models  
- Generative models (GANs, VAEs, Diffusion)  
- Self-supervised and contrastive learning

## 4. Expanded Key Concepts
- Backpropagation, activation functions, normalization layers  
- Optimizers (SGD, AdamW), LR schedules and warmup  
- Regularization: dropout, weight decay, early stopping  
- Mixed precision training, gradient accumulation, distributed training

## 5. Expanded Tools & Technologies
- PyTorch, TensorFlow/Keras, JAX  
- Hugging Face Transformers, torchvision, torchaudio  
- DeepSpeed, Horovod, NVIDIA tools for distributed training  
- Experiment logging: WandB, TensorBoard

## 6. In-Depth Workflow (example: fine-tuning a transformer)
1. Tokenize and prepare datasets.  
2. Select pre-trained backbone and adapt the head.  
3. Use AdamW with warmup and proper weight decay.  
4. Apply gradient accumulation and mixed precision if needed.  
5. Save checkpoints and perform early stopping.  
6. Convert to a serving format (ONNX/TorchScript) for deployment.

## 7. Common Job Roles
- Deep Learning Engineer  
- Research Scientist (DL)  
- Model Optimization Engineer

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Backpropagation`** | The algorithm for training neural networks. |
| **`Checkpoint`** | Saving the model's state during training. |
| **`Data Augmentation`** | Creating new training data by modifying existing data. |
| **`Distillation`** | Training a smaller model to mimic a larger one. |
| **`Epoch`** | One complete pass through the training dataset. |
| **`Fine-tuning`** | Adapting a pre-trained model to a new task. |
| **`GAN`** | Generative Adversarial Network. |
| **`Mixed Precision`** | Using both 16-bit and 32-bit floating-point types during training to make it faster. |
| **`Transformer`** | A neural network architecture based on attention. |
| **`Weight Decay`** | A regularization technique to prevent overfitting. |

</details>

[⬆️ Back to Table of Contents](./README_AI_en.md)
