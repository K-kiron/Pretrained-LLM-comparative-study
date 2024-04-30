# Pretrained RNN vs Pretrained Transformer

## Introduction

This study provides a comprehensive comparison between RNNs, represented by the Mamba model, and pre-trained Transformer models, represented by the Pythia suite. Our study investigates whether RNNs, pre-trained on a large number of datasets, are able to achieve comparable performance to their Transformer counterparts in a variety of NLP tasks, including sequence classification, causal language modelling, and context-aware quizzing. Using standard benchmarks such as the GLUE, WikiText-2, and SQuAD datasets, we evaluate the fine-tuning and zero/few-shot learning capabilities of both model families. Results show that RNNs can not only compete with, but sometimes even outperform Transformer models, marking an important step in understanding the capabilities and limitations of these neural network architectures for language processing tasks.



## How to run the code

The code is written in Jupyter notebooks. The pip installations for necessary packages are provided in the notebook itself. It is highly recommended to run the code in Google Colab as experimented.
In case you want to run the code locally, you can use the provided `requirements.txt` file to install the necessary packages. The instructions for both Conda and Pip + Virtualenv are provided below.


### Conda 

Conda uses the provided `requirements.txt` file.
Make sure you have [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual) installed on your system.
Once installed, open up your terminal (or Anaconda prompt if you're on Windows).
Install the environment from the specified environment file:

    conda create --name ift6289-project --file requirements.txt
    conda activate ift6289-project

After you install, register the environment so jupyter can see it:

    python -m ipykernel install --user --name=ift6289-project

You should now be able to launch jupyter and see your conda environment:

    jupyter-lab



### Pip + Virtualenv

An alternative to Conda is to use pip and virtualenv to manage your environments.
This may play less nicely with Windows, but works fine on Unix devices.
This method makes use of the `requirements.txt` file.

Ensure you have installed the [virtualenv tool](https://virtualenv.pypa.io/en/latest/installation.html) on your system.
Once installed, create a new virtual environment:

    vitualenv ~/ift6289-project-venv
    source ~/ift6289-project-venv/bin/activate

Install the packages from a requirements.txt file:

    pip install -r requirements.txt

As before, register the environment so jupyter can see it:

    python -m ipykernel install --user --name=ift6289-project-venv

You should now be able to launch jupyter and see your conda environment:

    jupyter-lab

If you want to create a new `requirements.txt` file, you can use `pip freeze`:

    pip freeze > requirements.txt