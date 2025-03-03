# Fine tuning QWEn2.5-0.5B on databricks-dolly-15k dataset

In this Notebook I mainly tried how to fine tune llm with local data. Here I have fine tuned a small model Qwen2.5-0.5B. I used free colab with T4 gpu to train the model. I used PEFT with LoRA. The model was trained only on 5k data samples to see how it adapts. 

## Prerequisites
- Jupyter Notebook or Google Colab access

## Running the Notebook

### Locally with Jupyter Notebook

1. Download the ipynb file, and open it with jupyter notebook. Start executing it. Please check you have gpu set up for the code to run smoothly. 

### On Google Colab
1. Open google colab
2. Upload the ipynb file to colab
3. Change runtime type to use gpu
4. Start executing the cells!! 
