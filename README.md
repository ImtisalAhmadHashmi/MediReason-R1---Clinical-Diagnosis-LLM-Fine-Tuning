# MediReason-R1---Clinical-Diagnosis-LLM-Fine-Tuning
🔹 Domain Adaptation & Model Architecture\
• Fine-tuned DeepSeek-R1 (8B) using 4-bit quantization & LoRA (r=16, α=20)\
• Targeted 7 key layers (q_proj, v_proj, gate_proj, etc.) for surgical parameter efficiency\
• Achieved 75% VRAM reduction while retaining diagnostic accuracy on T4 GPU\
⚙️ Medical Data Engineering\
• Processed 19,000 expert-annotated samples from medical-o1-reasoning-SFT\
• Engineered clinical prompt templates with XML-style reasoning tags\
• Structured inputs as: Clinical context → step-by-step analysis → diagnosis/treatment\
🤖 Training Optimization & Monitoring\
• Implemented gradient checkpointing (batch=2 × accum=4) for memory efficiency\
• Trained for 770 steps with AdamW-8bit (lr=2e-4) and linear scheduling\
• Tracked convergence via Weights & Biases with 10-step logging intervals\
🚀 Validation & Real-World Application\
• Validated on trauma cases (e.g. tension pneumothorax diagnosis)\
• Achieved coherent treatment plans including critical interventions\
• Saved quantized model to Google Drive for clinical deployment\
💡 Why It Matters: Demonstrates how parameter-efficient fine-tuning unlocks specialized medical reasoning in LLMs - crucial for diagnostic support systems!\
Tools: Python, Hugging Face (TRL, Transformers), Unsloth, LoRA, W&B, 4-bit Quantization

