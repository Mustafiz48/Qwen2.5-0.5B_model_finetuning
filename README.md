# Fine tuning QWEn2.5-0.5B on databricks-dolly-15k dataset

In this Notebook I mainly tried how to fine tune llm with local data. Here I have fine tuned a small model Qwen2.5-0.5B. I used free colab with T4 gpu to train the model. I used PEFT with LoRA. The model was trained only on 5k data samples to see how it adapts. 

After running it only for 3 epohs, we can see how it performs better for a sample question. 
For reference, we asked the model a question 

**Who wrote harry potter?** 

before and after the fine tuning. We can see a huge change in response. 

### Response Before Training:

```
Who wrote harry potter? A. Rowling B. Rowling C. Rowling D. Rowling
Answer:
A

Which of the following statements about the relationship between the Communist Party of China and the democratic parties is incorrect?
A. The Communist Party of China and the democratic parties are both the ruling party and the participating party in the country.
B. The Communist Party of China and the democratic parties are both the ruling party and the participating party in the country.
C. The Communist Party of China and the democratic parties are both the ruling party and the participating party in the country.
D. The Communist Party of China and the democratic parties are both the ruling party and the participating party in the country.
Answer:
B

The main reason for the formation of the 'Three Gorges Dam' is ____
A. The terrain is high and the river is long
B. The terrain is low and the river is short
C. The terrain is high and the river is short
D. The terrain is low and the river is long
Answer:
A

Which of the following statements about the geographical characteristics of the four countries is incorrect?
A. Country A has a tropical monsoon climate.
B. Country B has a temperate oceanic climate.
C. Country C has a temperate continental climate.
D. Country D has a tropical rainforest climate.
...
C. Country C has a temperate continental climate.
D. Country D has a tropical rainforest climate.
Answer:
D
```
We can see the response is not good. It generates many unrelated responses.

### Response After Training:
```
Who wrote harry potter? 
 
 J.K. Rowling
```

We can see, it's a clear concise answer. 

This shows how powerful model finetuning is! By training only 0.0795 % params only for 3 epochs, it generates a way better response. 

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
