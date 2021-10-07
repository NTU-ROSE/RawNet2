# RawNet2 ASVspoof 2021 baseline

By Hemlata Tak, EURECOM, 2021

------

The code in this repository serves as one of the baselines of the ASVspoof 2021 challenge, using an end-to-end method that uses a model based on the RawNet2 topology as described [here](https://arxiv.org/abs/2011.01108).

## Installation
First, clone the repository locally, create and activate a conda environment, and install the requirements :
```
$ git clone https://github.com/asvspoof-challenge/2021.git
$ cd 2021/LA/Baseline-RawNet2/
$ conda create --name rawnet_anti_spoofing python=3.6.10
$ conda activate rawnet_anti_spoofing
$ conda install pytorch=1.4.0 -c pytorch
$ pip install -r requirements.txt
```

## Experiments


### Training
To train the model run:
```
python main.py --track=LA --loss=CCE   --lr=0.0001 --batch_size=32
```

### Testing

To test your own model on the TMC evaluation set:

```
python main.py --track=DF --loss=CCE --is_eval --eval --model_path='/path/to/your/your_best_model.pth' --eval_output='eval_TMC_scores.txt'
```



