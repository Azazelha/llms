# Llama-2

This repository contains a PyTorch implementation of the Llama-2 model. The dataset used for training includes dialogues from a play. Please note that this version of Llama-2 is a miniature variant due to infrastructure constraints.

* **Epochs:** 30
* **Batch Size:** 32
* **Max Sequence Length:** 512
* **Dimension:** 128
* **Decoder Blocks:** 2
* **Total Heads:** 8
* **Total Key-Value Heads:** 2
* **Vocabulary Size:** 32001

# DDP-Based Distributed Training

* Command to initiate training on a single node with multiple GPUs: 
  **torch run --standalone --nproc-per-node=<NUM_GPUS> ddp_train.py**

# Results

* **Text Generation**
```
Test Sample 1: 
<s> 
CORIOLANUS:
I am subtle; I am here to kiss my son's cheek, which is as good as anything can be, and I wish I had heard that you are inclined.
```q
MENENIUS:
I am bound to you.

MENENIUS:
I am bound. You are the cause, sir; we are sure to be prone.

Both:
I am a part of your report.

MENENIUS:
I am a Roman, and I am not like your country. In the better now, you are no lesser than it seems to your country than you can. For the thing I have well as cruelty, as if you be remembered.

MARCIUS:
</s>

Test Sample 2: 
<s> 
QUEEN ELIZABETH:
O, my lord, frown with bravery.

KING RICHARD III:
Sweet father, love!

QUEEN ELIZABETH:
She speaks and in the hateful duke.

QUEEN ELIZABETH:
You spoke today early; take it away.

KING RICHARD III:
So long has been balm with your banishment, to make a fellow of ripe fellow and lay the white three-table open.
</s>
```