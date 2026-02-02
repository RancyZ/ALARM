<h2 align='center'>
    ALARM
</h2>

<h4 align='center'>
ALARM: Automated MLLM-Based Anomaly Detection in Complex-EnviRonment Monitoring with Uncertainty Quantification
</h4>

Our paper is available at https://arxiv.org/pdf/2512.03101.

All the experiments are run by Python 3.12.2 on Apple M3 Pro with 18GB of memory. 

## Installation

1. Download and unzip the project folder.
2. The repository contains two case studies: Smart Home and Wound. Each case study is organized into two subfolders: one for code and one for data.
3. Smart Home case study:
   - The metadata files and ground-truth annotations for the video data are provided under Smart Home/Data. Due to the large size of the SmartHome-Bench dataset (1,203 videos), the raw video files are not included in this repository.
   - To download the videos, please follow the instructions in the original [SmartHome-Bench](https://github.com/Xinyi-0724/SmartHome-Bench-LLM/tree/main) repository under the “Download Videos” section. Baseline methods are implemented following the same repository.
   - For ALARM LLM output generation, each LLM produces two files:
        - Step 1: Initial model responses, including Data Comprehension and Analytical Thinking.
        - Step 2: Refined outputs corresponding to the Reflection stage.
4. Wound case study:
   - The wound dataset is fully provided in this repository.
   - The original dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/yasinpratomo/wound-dataset).
   - For ALARM LLM output generation, the corresponding code is implemented in llm_gen.ipynb.


## Reproducibility Workflow

| Which results to reproduce | Data File        | Code File | Output | Run time at the above-specified computer conditions |
|---|---|---|---|---|
| Table 1 | `Smart Home/Data` | `Smart Home/Code/LLM_output_generation`<br>`Smart Home/Code/UQ_calculation/desc`<br>`Smart Home/Code/UQ_calculation/reas`<br>`Smart Home/Code/UQ_calculation/ref`<br>`Smart Home/Code/UQ_calculation/All` | The performance results in Table 1 | 14 hours |
| Figure 5 | `Smart Home/Data` | `Smart Home/Code/UQ_calculation/desc`<br>`Smart Home/Code/UQ_calculation/reas`<br>`Smart Home/Code/UQ_calculation/ref`<br>`Smart Home/Code/UQ_calculation/All` | The results under different P values in Figure 5 | 2 hours |
| Figure 6 | `Smart Home/Data` | `Smart Home/Code/UQ_calculation/smooth_weight` | The results of smooth weights | 1 minute |
| Figure 7 | NA | `Smart Home/Code/UQ_calculation/cost`<br>`Wound/Code/UQ_calculation/cost` | The results of optimal P vs. unit cost | 1 minute |
| Table 2 | `Wound/Data` | `Wound/Code/LLM_output_generation`<br>`Wound/Code/UQ_calculation/desc`<br>`Wound/Code/UQ_calculation/reas`<br>`Wound/Code/UQ_calculation/ref`<br>`Wound/Code/UQ_calculation/All` | The performance results in Table 2 | 14 hours |
| Figure 10 | `Wound/Data` | `Wound/Code/UQ_calculation/desc`<br>`Wound/Code/UQ_calculation/reas`<br>`Wound/Code/UQ_calculation/ref`<br>`Wound/Code/UQ_calculation/All` | The results under different P values in Figure 10 | 2 hours |
| Figure 11 | `Wound/Data` | `Wound/Code/UQ_calculation/smooth_weight` | The results of smooth weights | 1 minute |
