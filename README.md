Deepfake Detectors – Zero-Shot & Few-Shot
This project explores the use of Visual Language Models (VLMs), specifically InstructBLIP, as deepfake detectors capable of generalizing beyond the training distribution. Rather than treating deepfake detection as a standard binary classification task, the system reframes it as a Visual Question Answering problem: given an image and the prompt "is this photo real?", the model produces a calibrated probability score via a custom probabilistic inference algorithm (logit extraction over Yes/No token subsets + Softmax normalization).
The system is evaluated in Zero-Shot and Few-Shot (Q-Former fine-tuning only) configurations across three datasets: a custom CelebA-HQ / SimSwap benchmark, Celeb-DF-v2, and DFDC. It is benchmarked against Self-Blended Images (SBI) as a traditional artifact-based baseline.
Key results:

Fine-tuned InstructBLIP (DFDC, LR=5e-5): AUC = 0.9808 in-domain, 0.8712 cross-dataset (CelebA-HQ/SimSwap)
SBI baseline on the same cross-dataset benchmark: AUC = 0.8393 / 0.8338
Zero-Shot AUC on CelebA-HQ: 0.7406 (no deepfake training data)

Supervisors: Dr. Renata Avros, Prof. Zeev Volkovich
