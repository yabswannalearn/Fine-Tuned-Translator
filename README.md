# Intro

We are using **Unsloth** for 4-bit quantization.  
**Model:** `Qwen3-1.7B-unsloth-bnb-4bit`

## Task
Fine-tune the model to improve translation from Kapampangan to English.

## Dataset
* [Kapampangan-English Sentences](https://huggingface.co/datasets/Coco-18/Kapampangan-English)

## Steps
1. Install required dependencies
2. Load the model 
3. Test the base model (pre-fine-tuning)
4. Initiate QLoRa for fine-tuning
5. Set up the dataset
6. Fine-tune the model
7. Run inference on the fine-tuned model
8. Benchmark BLEU and chrF (Raw vs. Fine-tuned)
9. Save to Google Drive

## Output

| **Metric** | **Raw Model (Base)** | **Fine-Tuned Model** | **Improvement** |
| :--- | :--- | :--- | :--- |
| **BLEU Score** | 0.03 | **72.01** | **+71.98** |
| **chrF Score** | 4.61 | **69.78** | **+65.17** |


## Implementation in RAG
This fine-tuned model is deployed as the primary generation engine in the **Kapampangan2English RAG Pipeline**. 
It utilizes a local vector database to further expand its vocabulary beyond the initial training set.
[Kapampangan2English Implementation](https://github.com/yabswannalearn/Kapampangan2English)
