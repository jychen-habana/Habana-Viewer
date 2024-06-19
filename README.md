# projection
Habana-Viewer is a projection tool for LLMs performance and memory analysis on Intel Gaudi platform. You can use this tool as a model optimization guidline on Intel Gaudi.

## Command
1. Simpily run with **run_projection.py** and the results will be saved to folder "data".
    ```sh
    python run_projection.py
    ```
2. Run with jupyter notebook: **run_projection.ipynb** for simpily visualization.

## Models
|Model Name|Projected Data|
|:------:|:------:|
|Llama2-7B|[Link](./data/model/Llama2-7B/)|
|Llama2-13B|[Link](./data/model/Llama2-13B/)|
|Llama3-8B|[Link](./data/model/Llama3-8B/)|
|Qwen-7B|[Link](./data/model/Qwen-7B/)|
|Qwen-14B|[Link](./data/model/Qwen-14B/)|
|Mixtral-8x7B|[Link](./data/model/Mixtral-8x7B/)|

## Example

### Compute
#### Llama2-13B
- Overall Projection [(more details in table)](./data/model/Llama2-13B/IntelGaudi2C_overall_projection.csv)
![Llama2-13B Overall Projection](./data/model/Llama2-13B/IntelGaudi2B_pp1_tp1_overall_projection.png)

- Attn Projection
    - Q@K_T
    [Prefill](./data/model/Llama2-13B/IntelGaudi2B_pp1_tp1_BF16_prefill_attn_qk_projection.csv) |
    [Decode](./data/model/Llama2-13B/IntelGaudi2B_pp1_tp1_BF16_decode_attn_qk_projection.csv)

    - Score@V
    [Prefill](./data/model/Llama2-13B/IntelGaudi2B_pp1_tp1_BF16_prefill_attn_sv_projection.csv) |
    [Decode](./data/model/Llama2-13B/IntelGaudi2B_pp1_tp1_BF16_decode_attn_sv_projection.csv)

- FFN Projection
[Prefill](./data/model/Llama2-13B/IntelGaudi2B_pp1_tp1_BF16_prefill_ffn_up_projection.csv) |
[Decode](./data/model/Llama2-13B/IntelGaudi2B_pp1_tp1_BF16_decode_ffn_up_projection.csv)

#### Llama3-8B
- Overall Projection [(more details in table)](./data/model/Llama3-8B/IntelGaudi2C_overall_projection.csv)
![Llama3-8B Overall Projection](./data/model/Llama3-8B/IntelGaudi2B_pp1_tp1_overall_projection.png)

- Attn Projection
    - Q@K_T
    [Prefill](./data/model/Llama3-8B/IntelGaudi2B_pp1_tp1_BF16_prefill_attn_qk_projection.csv) |
    [Decode](./data/model/Llama3-8B/IntelGaudi2B_pp1_tp1_BF16_decode_attn_qk_projection.csv)

    - Score@V
    [Prefill](./data/model/Llama3-8B/IntelGaudi2B_pp1_tp1_BF16_prefill_attn_sv_projection.csv) |
    [Decode](./data/model/Llama3-8B/IntelGaudi2B_pp1_tp1_BF16_decode_attn_sv_projection.csv)

- FFN Projection
[Prefill](./data/model/Llama3-8B/IntelGaudi2B_pp1_tp1_BF16_prefill_ffn_up_projection.csv) |
[Decode](./data/model/Llama3-8B/IntelGaudi2B_pp1_tp1_BF16_decode_ffn_up_projection.csv)

#### Qwen-7B
- Overall Projection [(more details in table)](./data/model/Qwen-7B/IntelGaudi2B_overall_projection.csv)
![Qwen-7B Overall Projection](./data/model/Qwen-7B/IntelGaudi2B_pp1_tp1_overall_projection.png)

- Attn Projection
    - Q@K_T
    [Prefill](./data/model/Qwen-7B/IntelGaudi2B_pp1_tp1_BF16_prefill_attn_qk_projection.csv) |
    [Decode](./data/model/Qwen-7B/IntelGaudi2B_pp1_tp1_BF16_decode_attn_qk_projection.csv)

    - Score@V
    [Prefill](./data/model/Qwen-7B/IntelGaudi2B_pp1_tp1_BF16_prefill_attn_sv_projection.csv) |
    [Decode](./data/model/Qwen-7B/IntelGaudi2B_pp1_tp1_BF16_decode_attn_sv_projection.csv)

- FFN Projection
[Prefill](./data/model/Qwen-7B/IntelGaudi2B_pp1_tp1_BF16_prefill_ffn_up_projection.csv) |
[Decode](./data/model/Qwen-7B/IntelGaudi2B_pp1_tp1_BF16_decode_ffn_up_projection.csv)

#### Mixtral-8x7B
- Overall Projection [(more details in table)](./data/model/Mixtral-8x7B/IntelGaudi2B_overall_projection.csv)
![Mixtral-8x7B Overall Projection](./data/model/Mixtral-8x7B/IntelGaudi2B_pp1_tp1_overall_projection.png)

- Attn Projection
    - Q@K_T
    [Prefill](./data/model/Mixtral-8x7B/IntelGaudi2B_pp1_tp1_BF16_prefill_attn_qk_projection.csv) |
    [Decode](./data/model/Mixtral-8x7B/IntelGaudi2B_pp1_tp1_BF16_decode_attn_qk_projection.csv)

    - Score@V
    [Prefill](./data/model/Mixtral-8x7B/IntelGaudi2B_pp1_tp1_BF16_prefill_attn_sv_projection.csv) |
    [Decode](./data/model/Mixtral-8x7B/IntelGaudi2B_pp1_tp1_BF16_decode_attn_sv_projection.csv)

- FFN Projection
[Prefill](./data/model/Mixtral-8x7B/IntelGaudi2B_pp1_tp1_BF16_prefill_ffn_up_projection.csv) |
[Decode](./data/model/Mixtral-8x7B/IntelGaudi2B_pp1_tp1_BF16_decode_ffn_up_projection.csv)


## Todo
1. Currently only cover single card perf projection, will support multi-card / multi-node.
2. will cover more models.