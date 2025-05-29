# Job Recommendation System using Knowledge Graphs
Comparing standalone models with an ensemble model using knowledge graphs for a job recommendation system.


## Table of Contents

* [CUDA Environment Setup](#cuda-environment-setup)
* [Installation of dependencies](#installation-of-dependencies)
* [Installation of Neo4j Desktop for Knowledge Graphs](#installation-of-neo4j-desktop-for-knowledge-graphs)
* [Dataset Links](#dataset-links)


* Make sure you are in the "JobRecommendationSystem" folder before installing anything


## CUDA Environment Setup

Follow these commands to set up the CUDA environment for Jupyter Notebooks in VSCode, adapted from [Aman Singh’s guide](https://amansingh3110.medium.com/how-to-set-up-cuda-environment-for-jupyter-notebooks-vscode-a-comprehensive-guide-669f00ba07f7):

```bash
# 1. Create a Virtual Environment
python -m venv virtualenvname

# 2. Installing Jupyter and IPykernel
pip install ipykernel jupyter

# 3. Installing PyTorch with CUDA Support
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

# 4. Upgrade pip if necessary
python.exe -m pip install --upgrade pip

# 5. Creating a CUDA Kernel for Jupyter
python -m ipykernel install --user --name=cuda --display-name "cuda-gpt" #<- can be any name

# 5. Using the CUDA Kernel in Jupyter Notebooks
jupyter notebook

# 6. Press the kernel, then click on "Existing Jupyter Server" and enter the link given to you in the terminal after you entered "jupyter notebook" into the terminal
```

## Installation of dependencies

Step-by-step instructions on how to get the development environment running.

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Verify installation
pip list
```


## Installation of Neo4j Desktop for Knowledge Graphs

1. Go to the following website and download the Neo4j for Desktop: https://neo4j.com/download/?utm_source=GSearch&utm_medium=PaidSearch&utm_campaign=Evergreen&utm_content=EMEA-Search-SEMBrand-Evergreen-None-SEM-SEM-NonABM&utm_term=download%20neo4j&utm_adgroup=download&gad_source=1&gad_campaignid=20769286940&gclid=CjwKCAjw87XBBhBIEiwAxP3_A9ZQiNelEUwPnIQxSUZLN6XswSeSYuQdrHsjqKZJQ0k3MVcohHtwjBoCNCkQAvD_BwE
2. Once the application has been installed, open the application
3. Click on the Projects tab, then click "New" to open a new project
4. Click on "Add" and add a Local DBMS to the new project you have created
5. Enter a name for the GraphDBMS (can be this: Job Recommendation System using Knowledge Graphs) and enter the password, "jobrecsys"
6. Before you create the GraphDBMS, ensure the version is on 5.26.6(latest)
7. Once you have created your GraphDBMS, click on the DBMS and on the right hand panel, click on "Plugins" and install APOC and Graph Data Science Library
8. Before you run the code for "Visualising the Knowledge Graph" onwards, make sure the GraphDBMS has been started (click "Start" if not)


## Dataset Links

1. Careerbuilder Job Listing 2020: https://www.kaggle.com/datasets/promptcloud/careerbuilder-job-listing-2020
2. O*NET® 29.3 Database: https://www.onetcenter.org/database.html#overview
