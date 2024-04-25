# fake-news-detection-with-llama2
This repository contains code relevant to the Honours project (CSI4900) completed in Winter 2024.

## Running the code
*Note: During the experimental setup, the Python notebooks to fine-tune the model were imported into Kaggle Notebooks, alongside the relevant training/validation/testing datasets.
Meanwhile, the preprocessing Python notebooks that acquired and split the training and testing datasets were imported into Google Collab, alongside the relevant datasets.*

In order to run any of the notebooks, the file paths to the relevant data need to be updated and the enironment needs to be set up in such a way that there are no conflicting dependencies.

### Prerequisites
- Request access from Meta website to use Llama 2 model (may take several days)
- Setup a HuggingFace account in order to authenticate the use of private models
- Set up and Weights & Biases account

### Packages and Dependencies 
pip installations and imports are included in the notebooks where they are needed
- Accelerate
- PEFT
- BitsAndBytes
- Transformers
- trl
- Pandas
- NumPy
- Scikit-learn model selection, Scikit-learn metrics
- imblearn metrics
- Torch
- HuggingFace Datasets
- HuggingFace Hub 

## Organization of Repo
- `datasets/ForTraining`: Original training datasets
- `datasets/ProcessedTestingDatasets`: The processed versions of the datasets used for testing 
- `scripts/`: the Python notebooks used to execute the training, validation, and testing of the Llama 2 models
- `scripts/unused-experiments`: contains upsampling, downsampling, changing number of layer experiments which are not used in final results
- `scripts/preprocessing`: contains the preprocessing scripts
- `scripts/test-results-processing-scripts`: contains scripts to process the testing results
- `results/testing_split`: results acquired from running models on their respective test split
- `results/testing_datasets/final_results`: results acquired from running models on their respective testing datasets
- `results/testing_datasets/intermediate_classifier_results`: intermediate results after using the domain classifier

## Where to find the best performing models?
*Note: all of the best-performing models can be found on Hugging Face. However, you may need to request access to use them.*

For the 2 step predictor:
- Domain classifier: `FakeNewsLlama/CombinedDomainClassifier_E1_7`
- Politics True/Fake predictor: `FakeNewsLlama/PoliticsTrueFakeClassifier`
- Social True/Fake predictor: `FakeNewsLlama/SocialTrueFakeClassifier_E1_LR4`
- Health True/Fake predictor: `FakeNewsLlama/HealthTrueFakeClassifierFinal`
- Crime True/Fake predictor: `FakeNewsLlama/CrimeTrueFakeClassifier5e-4`
- Science True/Fake predictor: `FakeNewsLlama/ScienceTrueFakeClassifier_E7_LR1_4`

Baseline model: `FakeNewsLlama/TrueFakeBaseline`

## Where to find the datasets?
Processed Training Datasets can be found in this HuggingFace Dataset: `FakeNewsLlama/ProcessedTrainingDatasets`
The Dataset also includes the processed training datasets split by domain for true/fake training in TrueFakeTraining.zip
