# My finetuning scripts for llama3.2-1B-physics-finetuned on 🤗 
## with RX7800XT, AMD Navi customer card

Since Navi Card don't fully support flash attention, so using unsloth etc is not feasible, in this repo I will show you how to do that without FA enabled for AMD consumer cards.

My huggingface 🤗 Profile [benhaotang](https://huggingface.co/benhaotang)
Model: [benhaotang/llama3.2-1B-physics-finetuned](https://huggingface.co/benhaotang/llama3.2-1B-physics-finetuned)

Checkout the jupyter notebook to start training on your RX7700/7800/7900 cards!

# Instruction

1. you will need to install pytorch from ROCm repo

```
pip install --pre --upgrade --force-reinstall torch torchvision torchaudio numpy pytorch-triton pytorch-triton-rocm --index-url https://download.pytorch.org/whl/nightly/rocm6.2
```

2. you also need to compile transformers from ROCm/transformers
```
git clone https://github.com/ROCm/transformers.git
python setup.py install
```

3. install huggingface hub and get your access token from huggingface 🤗

4. open [finetune-llama.ipynb](./finetune-llama.ipynb) and you are set! Now load any dataset from huggingface to get started!