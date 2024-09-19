# Flux.1 Dev Lora Training with ai-toolkit

## 1. Prepare data
- Prepare sample photos of the product/object to be trained, the number is from 2-20 photos with size from 512 or more
## 2. Tools used
* AI Toolkit: [https://github.com/ostris/ai-toolkit](https://github.com/ostris/ai-toolkit)
(ai-toolkit requires hardware card from 24G Vram or more)
* GPU virtual machine service: Runpod

If you do not have an account, I would appreciate it if you use my referral link to register with the following link: https://runpod.io?ref=rpuub8vb
## Some important concepts:
* **Trigger word (TRIGGER_WORD):** Can be any word that FLUX.1 is not familiar with (usually acronyms that google translate cannot translate). This unique word (e.g. vf9, k3x,...) will trigger the features we train.
* **Number of training steps (STEPS_TRAIN):** Provides enough training time to learn the desired features, but can be time-consuming. 1500 to 4000 steps will give good results, but training time will be longer.
* **Learning rate (LEARNING_RATE):** Determines how much the weights change in the gradient direction in each update step. A value of 0.0001 is suitable for most requirements. When training for faces, a higher LR of 0.0004 will work well.
* **LoRA rank (LORA_RANK):** A value that balances trainable parameters and model capacity. Higher ranks may be needed for more complex tunings but require more VRAM. A setting of 16 is a good starting value, but for images that require better quality a higher Lora Rank value should be set.
## 3. Implementation steps see this video
[![Watch the video](https://i.imgur.com/wbuNJgl.png)](https://vimeo.com/1010943081)
