# 🧠 CS678 - HW2: Post-Training a Language Model (Qwen2.5 via Unsloth)

This project fine-tunes the **Qwen2.5** instruction model using **Unsloth** for efficient LoRA-based training and **Weights & Biases (wandb)** for real-time tracking.  
It demonstrates post-training (supervised fine-tuning) on conversational data with proper masking, quantization, and loss visualization.

---

## 🚀 Key Highlights
- Applied **chat templates** for Qwen2.5 and trained only on assistant responses using `train_on_responses_only()`.  
- Used **LoRA fine-tuning** with <1% trainable parameters and **4-bit quantization** to save GPU memory.  
- Logged training metrics in **wandb** and visualized loss convergence (~0.59 after 60 steps).  
- Compared **quantized (4-bit)** vs **full-precision (FP16)** runs — quantized achieved similar results with 60% less VRAM usage.  

---

## 📈 Results
- Lowest training loss: **~0.59** at step 7  
- Training time: **≈7 minutes** on Tesla T4 GPU  
- Verified loss masking and stable convergence via wandb  
- [wandb run link](https://wandb.ai/samruddhi/CS678_HW2_Llama/runs/e937ul9u)

---

## 🧠 Outcome
This project demonstrates how to efficiently fine-tune and analyze large language models using **LoRA**, **quantization**, and **wandb-based visualization** — providing a lightweight, reproducible pipeline for LLM adaptation.
