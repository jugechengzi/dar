
**If the code has any bugs, please open an issue. We will be grateful for your help.**

You can also refer to our team's other complementary work in this series：[FR (NeurIPS2022)](https://arxiv.org/abs/2209.08285), [DR (KDD 2023)](https://dl.acm.org/doi/abs/10.1145/3580305.3599299), [MGR (ACL 2023)](https://arxiv.org/abs/2305.04492), [MCD (NeurIPS 2023)](https://arxiv.org/abs/2309.13391), [DAR (ICDE 2024)](https://arxiv.org/abs/2312.04103).

## Environments
torch 1.10.2+cu113. python 3.7.9.
## Datasets
BeerAdvocate: you can get it from [here](http://people.csail.mit.edu/taolei/beer/). Then place it in the ./data/beer directory.  
Hotel Reviews: you can get it from [here](https://people.csail.mit.edu/yujia/files/r2a/data.zip). 
Then  find hotel_Location.train, hotel_Location.dev, hotel_Service.train, hotel_Service.dev, hotel_Cleanliness.train, hotel_Cleanliness.dev from data/oracle and put them in the ./data/hotel directory. 
Find hotel_Location.train, hotel_Service.train, hotel_Cleanliness.train from data/target and put them in the ./data/hotel/annotations directory.  
Word embedding: [glove.6B.100d.txt](https://nlp.stanford.edu/projects/glove/). Then put it in the ./data/hotel/embeddings directory.

## Running example
### Beer
Appearance: python -u teacher_beer.py --pre_epoch 100 --save 0 --dropout 0.2 --lr 0.0001 --batch_size 128 --gpu 1 --sparsity_percentage 0.167 --sparsity_lambda 11 --continuity_lambda 12 --epochs 200 --aspect 0





## Acknowledgement

The code is largely based on [Car](https://github.com/code-terminator/classwise_rationale) and [DMR](https://github.com/kochsnow/distribution-matching-rationality). Most of the hyperparameters (e.g. the '--cls_lambda'=0.9) are also from them. We are grateful for their open source code.





