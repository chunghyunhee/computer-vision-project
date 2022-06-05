# Computer vision final project
## How to Run
### (1) AdaBA : bias measurement
- Here is the sample commands for running the AdaBA (ours)
- If you want to see the scratch notebook code, refer this: [URL](https://github.com/socar-esther/Optimal_labeling_scheme/blob/main/notebook/scracth_AdaBA.ipynb)
```python
## AdaBA script
$ python biased_metric_main.py --model resnet50 \ 
                               --model_path scratch/checkpoint/cifar10_best.pt \ 
                               --data_root ../dataset/stylized_cifar10_set/test_reduced_10
```

### (2) Granular Scheme Experimental Codes
- sample commands for running Granular Scheme experiment: (a) Classification task, (b) OOD Task, (c) Transfer Task
```python                            
## Granular Scheme Baseline code (for classification)
$ python main.py --learning_rate 0.01 \
                 --train_root [TRAIN_DATASET_ROOT] \ 
                 --test_root [TEST_DATA_ROOT] \ 
                 --n_class 10 \
                 --n_style [STYLE_NUMBER] \
                 --lr_decay_epochs '60,80,100,120,140,160,180'

## Granular Scheme Transferability code
$ python transferability_main.py --learning_rate 0.01 \
                                 --train_root [TRAIN_DATASET_ROOT] \ 
                                 --test_root [TEST_DATA_ROOT] \ 
                                 --n_class [NUM_CLASS] \
                                 --n_style [STYLE_NUMBER] \
                                 --lr_decay_epochs '60,80,100,120,140,160,180'
```

## Usage
**Stylized CIFAR-10 Preparation**
- Download the CIFAR-10 dataset from [official website](https://www.cs.toronto.edu/~kriz/cifar.html)
- Get style images (paintings). Download train.zip file from [Kaggles' painter-by-numbers Dataset](https://www.kaggle.com/c/painter-by-numbers/data)



## Model checkpoints
- Experimental checkpoints of labeling scheme : [URL](https://drive.google.com/file/d/1yOz01OVvRCMu8DO_aqDgHNcLuHJfeJUC/view?usp=sharing)
- Transferred downstream weights : [URL](https://drive.google.com/file/d/1qvzIUqMkMfTd5_5wPMOFuRvgTRtPhj2G/view?usp=sharing)




