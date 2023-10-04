# Brazil-E-Commerce-Data-Engineering-and-Analysis

Link to dataset: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

A brief description of the implementation process:
1.	Connected Power Automate to Azure Blob Storage using the connection strings. As soon as a file is created in OneDrive folder, the file is fetched by Power Automate and placed into Azure Blob Storage.

2.	For Azure Cosmos Document DB implementation, the files from blob are imported into AZURE DATA FACTORY in the Dataset section. The files are cleansed, integrated, transformed, aggregated as per required hierarchy and nesting and finally, sink it into the destination Azure Cosmos Document DB.

3.	For Azure Graph DB implementation, we first use Azure data factory to combine the multiple .csv files required for graph implementation into one file. We established a connection from python to our azure blob storage where the combined file is placed to directly fetch from there. Then, established a connection from python to Azure Cosmos Graph DB using Gremlin API. Once the connection was established, we created the vertices and edges using the Gremlin API, ingesting data into Azure Cosmos Graph DB.

Data Architecture Diagram:</br>
<img width="1030" alt="image" src="https://github.com/Shrutika-Salian/Brazil-E-Commerce-Data-Engineering-and-Analysis/assets/91072559/48a018cd-1209-4744-8d86-9c402cfdfd02">




