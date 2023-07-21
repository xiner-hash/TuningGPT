# Fine-Tuning GPT for Conditional Generations using Data from .csv files
This repository contains code that facilitates the creation of a fine-tuning model using data from .csv file. We used the "training_data.csv" file for the demonstration. By following the instructions in the repository, users can fine-tune their own language model using their preferred .csv dataset and adapt it to their specific task or domain.

## So what is fine tuning conditional gernatrions?
Fine-tuning conditional Ggnerations is the process of adapting a pre-trained language model, such as GPT, to a specific task or domain. By fine-tuning, we modify the parameters of the pre-trained model based on the new data, allowing it to generate more contextually relevant and accurate responses for the given task.

## So what do I need?
1. An OpenAI API Key: To access OpenAI services, you will need a valid API key. If you don't have one, you can obtain it from the OpenAI website.
2. Installation of OpenAI Library: Install the OpenAI library by running the following command:
```python
!pip install openai
```
3. A .csv File with Prompts and Completions: Prepare a .csv file containing prompts and completions. OpenAI recommends specific formatting guidelines. In particular, ensure that the prompts start with "wh" words (e.g., when, where, who, why, which, what, etc.). Our code will ensure that the prompts start and end with "?->", and the completions start with a whitespace and end with a period (".").
 
### Code to submit
The code that reads prompts and completions from .csv and creates a fine-tuning job can be found in the TuningGPT.ipynb notebook. To run the code successfully, follow these steps:
1. Set the working directory and specify the .csv file with prompts and completions:
```python
new_directory = "<your_working_directory_path>" 
os.chdir(new_directory)
training_data = '<csv_filename>.csv'

2. Provide your API key by reading it from a .txt file:
```python
config_filename = "<your_api_key>.txt"
```
Alternatively, you may directly assign your API key (if you prefer not to use a .txt file)
```python
openai.api_key = "<your_api_key>"
```
