required libraries:
torch 
diffusers 
transformers 
accelerate 
lpips 
timm 
safetensors 
scikit-image 
matplotlib

In the code.ipynb notebook, after running the pipeline of our proposed method, we also include the base model code used for result comparison. This baseline model is a standard implementation and does not incorporate the proposed components such as the resampler or attention mechanisms.

Proposed Method (Ours)
We modified Stable Diffusion v1.5 with a Perceiver Resampler to bridge Frozen DinoV2 features into the UNet's cross-attention.
Input: 7-channel input (Noisy Latents + Semantic Map).

Base Model (Baseline)
Structure: A standard UNet2DModel trained from scratch without the Resampler, Attention, or Pre-trained weights.
*Serves as a benchmark to demonstrate the effectiveness of the proposed architecture.

For more details, you can read our [project report](./Report.pdf).