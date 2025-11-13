# NSDS: A Neural-Symbolic Data System for Geospatial Reasoning
We propose NSDS (Neural-Symbolic Data System), a next-generation framework designed to address the limitations of current AI scaling paradigms. As amassing more data and compute becomes unsustainable, NSDS provides a new approach by efficiently fusing the powerful perceptual capabilities of neural networks with the formal, verifiable logic of symbolic systems.

This project introduces NSDS as a multi-agent framework that supports dynamic, recursive, and multi-stage reasoning across diverse data types and heterogeneous programming environments. It offers a natural solution for automating task decomposition, iterative refinement, and coordinated execution between the neural and symbolic components of the system.

## Framework
![Framework](assets/multi_agent_framework.jpg)
## Project Structure
```text
        Neural-Symbolic-master/
        ├── agent_graph/
        │   ├── nodes/
        │   │   ├── action/
        │   │   │   └── execute_sql.py
        │   │   ├── brain/
        │   │   │   ├── classify_intent.py
        │   │   │   ├── filter_result.py
        │   │   │   ├── generate_answer.py
        │   │   │   ├── generate_sql.py
        │   │   │   ├── llm_chat.py
        │   │   │   └── sql_router.py
        │   │   └── perception/
        │   │       └── detect.py
        │   ├── graph_builder.py
        │   └── state_schema.py
        ├── common/
        │   └── config_loader.py
        ├── data/
        │   └── test1.jpg
        ├── duckdb/
        │   └── demo.db
        ├── llm/
        │   └── qwen_wrapper.py
        ├── models/
        │   └── yolo/
        │       └── yolov8_best.pt
        ├── scripts/
        │   ├── sql/
        │   │   ├── 01_create_geo_table.sql
        │   │   └── 02_insert_geo_data.sql
        │   └── init_db.py
        ├── .gitignore
        ├── config.yaml
        ├── README.md
        └── requirements.txt
```
## Requirements
Based on our `requirements.txt` file:
-   ultralytics==8.3.159
-   langgraph==0.5.1
-   langchain==0.3.26
-   pyyaml==6.0.1
-   pillow~=11.3.0
-   langchain-core~=0.3.68
-   duckdb==1.3.2
# Install dependencies
```shell
# Python version： 3.10
pip install -r requirements.txt
```
# Startup program
```text
Execute the main function in graph_builder within agent_graph.
```
