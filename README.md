# <p align=center>Dagonet</p>

<p align="center">
<img align="center" src="https://github.com/user-attachments/assets/573129ff-909c-4749-af5d-520e351990cb">
</p>

Making a full process from data collection to GRPO for a decent Mini model

Features/roadmap:

 - [ ] Webscraping, HF downloads, Annas Archive, etc to text files in a folder
 - [ ] Multiple tokenizers, chars, BPE
 - [x] Sharded Data loader, txt files to config sizeable bin shards
 - [x] Modeled out base LM arch, Dense Transformer, DS-MoE, MLA+NSA, RoPE, KVcache
   - [ ] other experimentals (MLP-mixer, etc)
 - [ ] Multimodal Input (Image, audio/video)
 - [ ] Training strats, like Curriculum learning, interleaving data, etc (settle as I code)
 - [ ] Layer 2 thinking (KV deliberation, memory layers, byte latent, theory of mind, Quiet Star, CocoNut, settle as I code)
 - [ ] Fully distributed Training Runs
   - [x] 0D (1 GPU)
   - [ ] DDP
   - [ ] FSDP
   - [ ] TP
   - [ ] CP
   - [ ] EP
   - [ ] Pipelining
 - [x] SFT (take train checkpoint, add sft_iters to max_iters, put sft dataset in)
 - [ ] Posttraining (PRM, RLHF, TULU, settle as I code)
 - [ ] RL (probably GRPO)
 - [ ] Inference
   - [ ] Sampler settings (topk, topp, minp, temp, etc)
   - [x] KV Cache
 - [ ] benchmark evaluation script + benchmark numbers
 - [ ] websearch / tool use / Mech interp tricks (Activation boosting/patching, hallucination circuits, refusal circuits, control vectors, settle as I code) 

Deprecated Features (were tested, removed):

 - MTP: It needs scale to work, probably need 7b+
 - Mixture of a Million experts and Ultra Mem: I liked them, but its oddities and other performance issues force me to stay away, may keep just MoM though, more robust

Citations:

```
@misc{vaswani2023attentionneed,
      title={Attention Is All You Need}, 
      author={Ashish Vaswani and Noam Shazeer and Niki Parmar and Jakob Uszkoreit and Llion Jones and Aidan N. Gomez and Lukasz Kaiser and Illia Polosukhin},
      year={2023},
      eprint={1706.03762},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/1706.03762}, 
}

@misc{modded_nanogpt_2024,
      author={Keller Jordan and Jeremy Bernstein and Brendan Rappazzo and @fernbear.bsky.social and Boza Vlado and You Jiacheng and Franz Cesista and Braden Koszarsky and @Grad62304977},
      title={modded-nanogpt: Speedrunning the NanoGPT baseline},
      year={2024},
      url={https://github.com/KellerJordan/modded-nanogpt}
}

@misc{moe_essay,
     author={1a3orn},
     title={Introduction to Mixture of Experts (MoE)},
     year={2025},
     url={https://1a3orn.com/sub/essays-intro-to-moe.html},
     note={Accessed: 2025-03-06}
}

@misc{deepseekai2024deepseekv3technicalreport,
      title={DeepSeek-V3 Technical Report}, 
      author={DeepSeek-AI},
      year={2024},
      eprint={2412.19437},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2412.19437}, 
}

@misc{deepseekai2025deepseekr1incentivizingreasoningcapability,
      title={DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning}, 
      author={DeepSeek-AI},
      year={2025},
      eprint={2501.12948},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2501.12948}, 
}

@misc{yuan2025nativesparseattentionhardwarealigned,
      title={Native Sparse Attention: Hardware-Aligned and Natively Trainable Sparse Attention}, 
      author={Jingyang Yuan and Huazuo Gao and Damai Dai and Junyu Luo and Liang Zhao and Zhengyan Zhang and Zhenda Xie and Y. X. Wei and Lean Wang and Zhiping Xiao and Yuqing Wang and Chong Ruan and Ming Zhang and Wenfeng Liang and Wangding Zeng},
      year={2025},
      eprint={2502.11089},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2502.11089}, 
}
```

Image from [Reddit](https://www.reddit.com/r/balatro/comments/1cuv4sa/what_if_there_were_more_than_5_legendary_jokers/)
