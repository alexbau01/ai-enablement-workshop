# AI Enablement Workshop

## Introduction
This workshop is designed to help you get started with AI and Machine Learning in the SAP context. We will cover topics in the area of AI, Machine Learning, and Deep Learning. We will primarily Python programming language and how to use it for AI and Machine Learning.

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

### Git

If you want to clone the GitHub repository, you need to have Git installed on your machine. Alternatively, you can download the repository as a ZIP file.

### Python Setup

- Python
- Python venv in your project folder
- Jupyter pip package in venv
- Jupyter Notebook Server (e.g. VS Code Jupyter Extension)

You can leverage the functionality of your IDE (preferrably VS Code or PyCharm) to run the Jupyter Notebooks. Feel free to create the venv and activate Jupyter from there. To do it manually, you can use the following commands:

#### Warning
_Note: Make sure you have access to the internet to install the required packages. If you are behind a proxy, make sure to set the proxy settings accordingly._

_If you have troubles with your local setup, you can also use the SAP Business Application Studio for this workshop. Make sure to enable the Python capability for your Dev Space._

#### Create venv in current folder 
You can create and activate a virtual environment in the console. If you want to use the built-in feature of your IDE for creating the environment, you can skip this step.

Make sure you are in the project root folder.
```bash
python3 -m venv venv 
```

#### Activate venv:
The venv can be activated in the console. How you activate the venv in your IDE and select it for the Jupyter Notebook Server depends on the IDE you are using.

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
