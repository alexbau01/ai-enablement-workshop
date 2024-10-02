# AI Enablement Workshop

## Introduction
This workshop is designed to help you get started with AI and Machine Learning in the SAP context. We will cover topics in the area of AI, Machine Learning, and Deep Learning. We will primarily Python programming language and how to use it for AI and Machine Learning.

## Prerequisites

- Basic programming knowledge
- Basic understanding of Machine Learning
- Basic understanding of Python
- Basic understanding of Jupyter Notebooks
- Basic understanding of SAP BTP
- Basic understanding of SAP HANA

## Agenda

1. Introduction & Technical Setup Check (~45 min)
2. Machine Learning auf SAP HANA (~45 min)
3. SAP HANA Cloud Vector Engine (~30 min)
4. Image Recognition (Dog/Cat) with AI Core (~1h)
5. Generative AI case (Generative AI Hub in AI Core + HANA Cloud Vector Engine) (~1h)
6. Document Information Extraction (~30min)
7. Wrap Up

## Technical Setup

You need to have the following tools installed on your machine:

### Python Setup

- Python
- Python venv in your project folder
- Jupyter pip package in venv
- Jupyter Notebook Server (e.g. VS Code Jupyter Extension)

You can leverage the functionality of your IDE (preferrably VS Code or PyCharm) to run the Jupyter Notebooks. Feel free to create the venv and activate Jupyter from there. To do it manually, you can use the following commands:

#### Create venv in current folder (make sure you are in the project root folder):
```bash
python3 -m venv venv 
```

#### Activate venv:
Mac/Linux:
```bash
source venv/bin/activate
```
Windows:
```bash
venv\Scripts\activate.bat
```

#### Install jupyter in venv:
```bash 
pip install jupyter
```

### Secrets

Download the secrets for AI Core and HANA Cloud from the BTP subaccount for the workshop. Links will be provided.

Place them in the `secrets` folder.
If the secrets folder does not exist, create it.

Call the secret file for ai core `aicore.json` and the secret for HANA Cloud `hana.json`.

We will import the secrets later in the code.

To work with generative AI and embedding models, you need to store your AI Core key in a config file. This config file can be created through a cli tool:

```bash
aicore configure -k ./secrets/aicore.json
```

If required, adjust the path to the secret file accordingly.
