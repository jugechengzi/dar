
## Environments
torch 1.10.2+cu113. python 3.7.9.
## Datasets
Beer Reviews: you can get it from [here](http://people.csail.mit.edu/taolei/beer/). Then place it in the ./data/beer directory.  
Hotel Reviews: you can get it from [here](https://people.csail.mit.edu/yujia/files/r2a/data.zip). 
Then  find hotel_Location.train, hotel_Location.dev, hotel_Service.train, hotel_Service.dev, hotel_Cleanliness.train, hotel_Cleanliness.dev from data/oracle and put them in the ./data/hotel directory. 
Find hotel_Location.train, hotel_Service.train, hotel_Cleanliness.train from data/target and put them in the ./data/hotel/annotations directory.  
Word embedding: [glove.6B.100d.txt](https://nlp.stanford.edu/projects/glove/). Then put it in the ./data/hotel/embeddings directory.

## Running example
### Beer
Appearance: python -u teacher_beer.py --pre_epoch 100 --save 0 --dropout 0.2 --lr 0.0001 --batch_size 128 --gpu 1 --sparsity_percentage 0.167 --sparsity_lambda 11 --continuity_lambda 12 --epochs 150 --aspect 0


## Result

You will get a result like "best_dev_epoch=116" at last. Then you need to find the result corresponding to the epoch with number "116". 

Train time for epoch #116 : 11.720709 second
traning epoch:116 recall:0.8292 precision:0.8693 f1-score:0.8488 accuracy:0.8523
Validate
dev epoch:116 recall:0.8660 precision:0.9219 f1-score:0.8931 accuracy:0.8426
Validate Sentence
dev dataset : recall:0.9374 precision:0.8749 f1-score:0.9051 accuracy:0.8508
Annotation
annotation dataset : recall:0.8873 precision:0.9976 f1-score:0.9392 accuracy:0.8868
The annotation performance: sparsity: 18.5996, precision: 81.4948, recall: 81.8705, f1: 81.6822
Annotation Sentence
annotation dataset : recall:0.9545 precision:0.9977 f1-score:0.9756 accuracy:0.9530
Rationale
rationale dataset : recall:0.8732 precision:0.9988 f1-score:0.9318 accuracy:0.8739


The F1 score corresponding to Table 3 is in the line "The annotation performance: sparsity: 18.5996, precision: 81.4948, recall: 81.8705, f1: 81.6822". It's a little higher than the result in Table 3, because we report the average results of five experiments.










