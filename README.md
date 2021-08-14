# RoCS: Knowledge Graph Embedding Based on Joint Cosine Similarity

### Train
```
CUDA_VISIBLE_DEVICES=0 python -u codes/run.py --do_train \
 --cuda \
 --do_valid \
 --do_test \
 --data_path data/FB15k \
 --model RoCS \
 -n 256 -b 1024 -d 1000 \
 -g 24.0 -a 1.0 -u 30 -adv \
 -lr 0.00001 --max_steps 150000 \
 -save models/RoCS_FB15k_0 --test_batch_size 16 -de
```

### Test
```
bash run.sh train RoCS FB15k 1 0 1024 256 1000 12.0 30 1 0.00001 150000 16 -de
```
