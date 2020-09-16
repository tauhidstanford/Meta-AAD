# [ICDM 2020] Meta-AAD: Active Anomaly Detection with Deep Reinforcement Learning

This is the implementation of ICDM 2020 paper of Meta-AAD: Active Anomaly Detection with Deep Reinforcement Learning. We propose to learn a meta-policy with deep reinforcement learning to optimize the performance of active anomaly detection. Please refer the paper for more deteails.

## Installation
```
git clone https://github.com/daochenzha/Meta-AAD.git
cd Meta-AAD
pip install -r requirments.txt
pip install -e .
```

## Training a Meta-Policy
Train a meta-policy with `train.py`. The important arguments are as follows.

*   `--train`: the datasets used for training, seperated by commas.
*   `--test`: the datasets used for testing, seperated by commas.
*   `--num_timesteps`: the number of training steps of reinforcement learning agents
*   `--log`: where the log and models will be outputed

By default, the reinforcement learning training log will be saved in `log/`, the anomaly discovery curves will be saved in `log/anomaly_curves`, and the trained model will be saved in `log/'.

## Evaluating a Trained Model
You may evaluate a trained model with `evaluate.py`. The important arguments aew as follows.

*   `--load`: the path to `model.zip` file.
*   `--test`: the datasets used for testing, seperated by commas.

## Baselines
We provide two baselines in this repo for comparison: a random query strategy and IForest query strategy. They are available in `evaluate_baselines.py`. For other baselines, please refer to the following repos.

*   *AAD*: [https://github.com/shubhomoydas/ad_examples](https://github.com/shubhomoydas/ad_examples)
*   *FIF*: [https://github.com/siddiqmd/FeedbackIsolationForest](https://github.com/siddiqmd/FeedbackIsolationForest)
*   *SSDO*: [https://github.com/Vincent-Vercruyssen/anomatools](https://github.com/Vincent-Vercruyssen/anomatools)

## Related Work
Our parallel work on graph neural networks have achieved state-of-the-art results on benchmark datasets with deep reinforcement learning. Please check [https://github.com/lhenry15/Policy-GNN](https://github.com/lhenry15/Policy-GNN).
