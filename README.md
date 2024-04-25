# fake-news-detection-with-llama2
This repository contains code relevant to the Honours project (CSI4900) completed in Winter 2024.

## Running the code
Note: During the experimental setup, the Python notebooks to fine-tune the model were imported into Kaggle Notebooks, alongside the relevant training/validation/testing datasets.

### Organization of Repo
- `data/`: datasets used for training, including the splits
- `scripts/`: the Python notebooks used to execute the training, validation, and testing of the Llama 2 models
- `scripts/unused-experiments`: contains upsampling, downsampling, changing number of layer experiments which are not used in final results
- `scripts/preprocessing`: contains the preprocessing scripts
- `scripts/test-results-processing-scripts`: contains scripts to process the testing results
- `results/testing_split`: results acquired from running models on their respective test split
- `results/testing_datasets/final_results`: results acquired from running models on their respective testing datasets
- `results/testing_datasets/intermediate_classifier_results`: intermediate results after using the domain classifier
