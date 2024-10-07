Development of this IPB AI Agent is temporarily paused.  The project requires specific data and localized IPB information that I cannot currently access due to security clearance restrictions.


# IPB AI Agent
#This is just a start the 3 required models need work. I am just learning. I think that the predictive model needs the most work. 

This is an AI-powered agent for Intelligence Preparation of the Battlefield (IPB). It combines terrain analysis, predictive modeling, risk assessment, and natural language processing to provide insights and recommendations for military operations.

## Features

* **Automated Terrain Analysis:** Analyzes terrain data (elevation, imagery) to identify key features like avenues of approach, chokepoints, and cover and concealment.
* **Predictive Modeling:** Predicts enemy courses of action (COAs) based on historical data, enemy order of battle (ORBAT), and terrain analysis.
* **Risk Assessment:**  Assesses the risk associated with different COAs, considering factors like enemy strength, terrain difficulty, and potential casualties.
* **Natural Language Interaction:**  Allows users to interact with the agent using natural language to ask questions, request information, and explore different scenarios.
* **Visualization:**  Provides 3D/4D visualizations of the battlefield, including terrain, unit positions, predicted enemy movements, and risk assessments.

## Architecture

The agent uses a hybrid AI approach, combining:

* **Machine Learning:**  Neural networks and other machine learning models are used for terrain analysis, predictive modeling, and risk assessment.
* **Knowledge Graph:**  A knowledge graph stores and represents relationships between entities (units, locations, events) and military doctrine.
* **Vector Database:**  A vector database stores embeddings of terrain features, enemy units, and other key elements for efficient similarity search and retrieval.
* **Natural Language Processing (NLP):**  The ChatGPT API is used for natural language understanding and generation, allowing for intuitive interaction with the agent.

## Modules

* **`data_acquisition.py`:**  Handles the acquisition of data from various sources (terrain data, weather data, ORBAT, etc.).
* **`data_processing.py`:**  Preprocesses and transforms the acquired data into a suitable format for the AI models.
* **`models/`:**
    * **`terrain_analysis_model.py`:**  Implements the terrain analysis model.
    * **`predictive_model.py`:**  Implements the predictive model for enemy COAs.
    * **`risk_assessment_model.py`:**  Implements the risk assessment model.
* **`vector_store.py`:**  Manages the vector database.
* **`knowledge_graph.py`:**  Manages the knowledge graph.
* **`visualization.py`:**  Handles the visualization of the battlefield.
* **`main.py`:**  The main entry point of the AI agent.

## Getting Started

1.  **Clone the repository:** `git clone https://github.com/your-username/ipb-ai-agent.git`
2.  **Install dependencies:** `pip install -r requirements.txt`
3.  **Set up environment variables:** Create a `.env` file and add your OpenAI API key:

    ```
    OPENAI_API_KEY=your_actual_api_key_here
    ```

4.  **Run the agent:** `python main.py`

## Usage

Once the agent is running, you can interact with it by sending HTTP requests to the `/query` endpoint.

```bash
curl -X POST http://localhost:5000/query \
     -H "Content-Type: application/json" \
     -d '{"input": "What are the enemy's most likely avenues of approach?"}'
