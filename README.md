# Ocean Data Quality Assessment through Outlier Detection-enhanced Active Learning (ODEAL)
Ocean and climate research benefits from global ocean observation initiatives such as Argo, GLOSS, and EMSO. The Argo network, dedicated to ocean profiling, generates a vast volume of observatory data. However, data quality issues from sensor malfunctions and transmission errors necessitate stringent quality assessment. Existing methods, including machine learning, fall short due to limited labeled data and imbalanced datasets. To address these challenges, we propose an ODEAL framework for ocean data quality assessment, employing AL to reduce human experts' workload in the quality assessment workflow and leveraging outlier detection algorithms for effective model initialization. We also conduct extensive experiments on five large-scale realistic Argo datasets to gain insights into our proposed method, including the effectiveness of AL query strategies and the initial set construction approach. The results suggest that our framework enhances quality assessment efficiency by up to 465.5\%  with the uncertainty-based query strategy compared to random sampling and minimizes overall annotation costs by up to 76.9\% using the initial set built with outlier detectors. 

## Download data
Download the data from `https://surfdrive.surf.nl/files/index.php/s/smVrIQWL5uoafAX` and place it at
`data/original_data/Atlantic_2019_03`. 

## Environment setup
`pip install -r requirements.txt`


## Folder explanation
- `preprocessing` module: preprocess argo data, split training and test subsets. The execution order is as follows: 
    1. `argo_preprocessing.ipynb`: Drop NAN, normalization, etc. 
    1.  `train_test_split.ipynb`: Split train, val and test subsets
    1. `initial_unlabeled_split.ipynb`: Split initial and unlabeled subsets
- `classification` module: offline classification without AL
- `active_learning` module: AL
    1. `pool_based.ipynb`: Pool-based AL using different classifiers
- `visualization` module: Visualize argo data



## Citation
If you use the codes in this repository, please cite our paper: 
```
Li, Na and Qi, Yiyang and Xin, Ruyue and Zhao, Zhiming. "Ocean Data Quality Assessment through Outlier Detection-enhanced Active Learning." 2023 IEEE International Conference on Big Data (Big Data). IEEE Computer Society, 2023.
```

```
@inproceedings{li2023ocean,
  title={Ocean Data Quality Assessment through Outlier Detection-enhanced Active Learning},
  author={Li, Na and Qi, Yiyang and Xin, Ruyue and Zhao, Zhiming},
  booktitle={2023 IEEE International Conference on Big Data (Big Data)},
  pages={1--1},
  year={2023},
  organization={IEEE Computer Society}
}
```