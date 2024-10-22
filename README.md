# MATRIX-Gen

#### Synthesizing Post-Training Data for LLMs through Multi-Agent Simulation [Paper](https://arxiv.org/abs/2410.14251) 

<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_a97e2bbb27de89e3cc1e906ea2763c0b.png" width="70%" height="auto">
</div>

MATRIX-Tuned-Model outperforms others, including Llama-3-8B-Instruct, with significantly less data.

<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_4728c0179d7ab513c630b602afdcedc3.png" width="70%" height="auto">
</div>


## News
- **To do:** 🔥 Code release 

- **10/18/2024:** We released the preprint paper in arxiv.


## Simulation
Our MATRIX generates realistic and diverse scenarios with 1000 real-world-grounded
agents and structured communication (agent grouping, inter- and intra-group communication )

<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_13b8301d700b5397b315356822dca19a.png" width="90%" height="auto">
</div>



## MATRIX-Gen
Overview of the proposed post-training data generation process (MATRIX-Gen) from scenarios
<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_443522b4634bbdc20315ce40d6b3e77d.png" width="90%" height="auto">
</div>

### Data Quality in the General Domain
- MATRIX-Gen-SFT
<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_eb0bd44ae1f048808e009ce80f4fd05d.png" width="80%" height="auto">
</div>

Models instruction-tuned on Llama3-8B using MATRIX-Gen-SFT consistently outperform those trained on baseline datasets with the same data quantity across both benchmarks. 

<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_336e091a0810a1c8592d3cea9bddb908.png" width="80%" height="auto">
</div>

- MATRIX-Gen-DPO
<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_a4e57f499cb395998fe57bac66aa23f8.png" width="80%" height="auto">
</div>

Models preference-tuned on MATRIX-SFT-Model using MATRIX-Gen-DPO outperform baselines with equivalent data quantities on both benchmarks.

### Data Quality in the Specific Domain

- MATRIX-Gen-Code & MATRIX-Gen-Safe
<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_331bcbe4aea1fb89a8f1068532af58db.png" width="46%" height="auto">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_15ac6cca839e40db9368fbfbc67cc6e8.png" width="44%" height="auto">
</div>

- MATRIX-Gen-MT
<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_57cd8a13e53b67302555cca58fd0f238.png" width="80%" height="auto">
</div>


## Effect of scenario scale & structured communication

Increasing scales of agents and scenarios significantly improves model performances. Agent-grouping-based structured communication produces the highest quality scenarios, while
random communication and no communication yield lower quality results.
<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_c35321243fcd81ba8232fb3184c697dc.png" width="80%" height="auto">
</div>
<div style="text-align: center;">
    <img src="https://notes.sjtu.edu.cn/uploads/upload_2a84121373c312328cb793fba12e6db7.png" width="80%" height="auto">
</div>

## Citation
Please cite our paper if you find the repository helpful.
```
@inproceedings{Tang2024SynthesizingPD,
  title={Synthesizing Post-Training Data for LLMs through Multi-Agent Simulation},
  author={Shuo Tang and Xianghe Pang and Zexi Liu and Bohan Tang and Rui Ye and Xiaowen Dong and Yanfeng Wang and Siheng Chen},
  year={2024},
  url={https://arxiv.org/abs/2410.14251}
}
```


