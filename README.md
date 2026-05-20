## Book Good Read Genre Classification using DistilBERT

This project fine-tunes **DistilBERT (`distilbert-base-cased`)** for good read genre classification of book using the Goodreads dataset. 

The model is trained using the Hugging Face Transformers library on Kaggle GPU infrastructure.

---

## Why DistilBERT?

For this assignment, **DistilBERT** was selected because it provides a strong balance between performance and computational efficiency. 

---


## Training Parameters

The model was fine-tuned using the Hugging Face `Trainer` API with the following configuration:

| Hyperparameter | Value |
|---|---|
| Pre-trained Model | `distilbert-base-cased` |
| Max Sequence Length | 512 |
| Training Epochs | 3 |
| Batch Size (Train) | 16 |
| Batch Size (Eval) | 32 |
| Learning Rate | 3e-5 |
| Warmup Steps | 100 |
| Weight Decay | 0.01 |
| Evaluation Strategy | Per epoch |
| Save Strategy | Per epoch |
| Logging | Every 50 steps → W&B |

---

## Results

After 3 epochs of fine-tuning, the model was evaluated on the held-out test set.

| Metric | Score |
|---|---|
| Accuracy | 0.583125 |
| Weighted F1 Score | 0.5799434836927834 |
| Evaluation Loss | 2.3064844608306885 |

---


## References

- https://huggingface.co/docs/transformers/index
- https://huggingface.co/distilbert/distilbert-base-cased
- https://wandb.ai/site
- https://www.kaggle.com/
