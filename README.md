# CEDFM
## Dependencies
Pytorch v1.12.1

python=3.9

another run:
```bash
# Python environment setup 
conda create -n cedfm python=3.9 
conda activate cedfm 
pip install -r requirements.txt 
```
## Dataset
The datasets can be downloaded from the github repositories of SSEGCN and DualGCN. The datasets contained therein have been preprocessed by CoreNLP.
## Our train command
```bash
# Restaurant
python train.py --model_name ce-qca --num_layers 1 --ffn_dropout 0.5 --post_dim 30 --attn_dropout 0.2 --balance_loss 
# Laptop
python train.py --model_name ce-qca --num_layers 1 --post_dim 30 --ffn_dropout 0.5 --input_dropout 0.5  --bert_dropout 0.5 --attn_dropout 0.2 --balance_loss --dataset laptop 
# Twitter
python train.py --model_name ce-qca --num_layers 1 --ffn_dropout 0.5 --attn_dropout 0.1 --balance_loss --dataset twitter 
# Ablation Experiment (change model name)
 ce-qa / ce / bert
```