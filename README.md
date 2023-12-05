<h1> Armstracker </h1>

Welcome to armstracker, an interactive web-application visualising the flow of arms ex- and imports and the impact on global conflict.

You can visit the app at <a href=https://www.arms-tracker.app>www.arms-tracker.app</a>

The app is both a passion-project as well as a project for my portfolio. 
If you are interested in the deails on how I created and maintain this project, this is where you can find all the details. 
If you are only interested in the finished product, you can stop reading now.

<h1>Structure</h1>
<img title="Project Structure" alt="This should be a really nice diagram of the project structure and workflow" src="images/taro-schema.svg">

<h1>Repositories</h1>
The app consists of three repositiories, plus this very repo you are reading right now.

TL;DR:
- taro-data: Backend.
- taro-map: Frontend.
- taro-tf: Infrastructure.

<h2>Taro</h2>
This very repository that serves as dcoumentation and a landing page.

<h2><a href=https://github.com/Kafkaese/taro-data>Taro-data</a></h2>
This repository contains the backend of the arms-tracker app. This includes:

<h4>EDA Jupyter Notebooks</h4>
Every data  projects  starts with the collection and exploration of data. Here you can EDA notebooks as well as notebooks containing the first code for data pipelines.
Since some of the additional data is scraped from Wikipedia, you can also find notebooks with web scrapers in this section.

<h4>API Code</h4>
The REST API was written in python using the <a href=https://fastapi.tiangolo.com/>FastAPI</a> package. It is served by a <a href=https://www.uvicorn.org/>Uvicorn Web Server</a>. The API serves as the interface between the Postgresql Database and the Frontend. It contains various endpoints for get requests to retrieve data in a safe way and encapsulates the complexity of the sql queries. 

 <h4>Pipeline</h4>h4>
 In order to get the raw data preprocessed into the Postgresql Database that the API queries, there are various data pipelines. They are in the form of a custom python package named 'taro'. This way they can easily be containerized and quickly run from said container.

 <h4>Tests</h4>
 In order to ensure a good devlopment workflow, the code for both the API, as well as the Pipelines, comes with a number of tests. The <a href=https://docs.pytest.org/en/7.4.x/>Pytest</a> package was used to write these. The tests are crucial for the CI workflow discussed later.
 
<h2><a href=https://github.com/Kafkaese/taro-map>Taro-map</a></h2>
This repository contains the frontend of the arms-tracker app. 

<h2><a href=https://github.com/Kafkaese/taro-tf>Taro-tf</a></h2>
Repository containin Terraform IaaC for provisioning the production environment on Azure.

- Azure Resource Group
- Azure Storage Account
- Azure Postgresql Flexible Server + Database
- Azure Container Registry
- 


<h2>Why taro?</h2>
<a href=https://en.wikipedia.org/wiki/Gerda_Taro>Gerda Taro</a> was a war photographer during the Spanish Civil War. She was immortalized in the Song Taro by indie band Alt-J. 
A taro is also a root vegetable not too dissimilar to a potato, but that is neither here nor their.
