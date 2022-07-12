# Lightweight-NAS: A Comparison Framework
The aim of NAS is to find optimal neural network architectures within a defined Search Space in an automated way. Search Spaces can be very large, and training every single architecture in order to find the best can be very expensive, both in terms of time and resources.
This is what drives the research to find some proxy that could give an estimate of the performance of a network without training it, as well as to find some algorithm that could help exploring the Search Space more efficiently.
In our paper, we implement three training-free metrics (ReLU, Synflow and Grad Norm) and two algorithms (Random Search and Regularized Evolutionary Aging), and perform an empirical study with every (metric, algorithm) combination on the NATS-Bench Topological Search Space, to understand whether these metrics can be used as surrogates of network’s training and also to find possible synergies between a certain metric and a certain algorithm. 


The Lightweight NAS procedure is composed by those 3 elements:
- Search Space: NATS-Bench Topological Search Space
- Search Strategies: Random Search, Regularized Aging Evolution
- Performance Estimators: Valid_accuracy 12 epochs, ReLU Score, Synflow, GradNorm.

The Project consists in the development of 3 CSV files, one for each vision dataset (Cifar10,Cifar100, ImageNet16-120), composed by the Scores obtained applying each Performance Estimator.
Major Implementation Details can be found in the report.

However to lunch our code we propose two possible environments:
1) Run it entirely, running through the steps that starting from  the CSV files generation brought to the Experiments perfomed with Random and Regularized Aging Evolution Search Strategies. 
2) Load the reported CSV files (cifar10_results.csv, cifar100_results.csv, ImageNet16_120_results.csv) and run Search Experiments. 
