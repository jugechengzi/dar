
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


## Result

You will get a result like "best_dev_epoch=158" at last. Then you need to find the result corresponding to the epoch with number "158". 

Train time for epoch #158 : 9.995826 second  
traning epoch:158 recall:0.8604 precision:0.8812 f1-score:0.8707 accuracy:0.8722  
Validate  
dev epoch:158 recall:0.8583 precision:0.9337 f1-score:0.8944 accuracy:0.8462  
Validate Sentence  
dev dataset : recall:0.9232 precision:0.8854 f1-score:0.9039 accuracy:0.8510  
Annotation  
annotation dataset : recall:0.8819 precision:0.9975 f1-score:0.9362 accuracy:0.8814  
The annotation performance: sparsity: 18.2168, precision: 80.5168, recall: 79.2232, f1: 79.8647  
Annotation Sentence  
annotation dataset : recall:0.9339 precision:0.9988 f1-score:0.9653 accuracy:0.9338  
Rationale  
rationale dataset : recall:0.8353 precision:0.9987 f1-score:0.9097 accuracy:0.8365  

The F1 score corresponding to Table 2 is in the line "The annotation performance: sparsity: 18.2168, precision: 80.5168, recall: 79.2232, f1: 79.8647". 







