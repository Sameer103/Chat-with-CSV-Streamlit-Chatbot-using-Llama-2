# Chat-with-CSV-Streamlit-Chatbot-using-Llama-2
Streamlit with Llama 2

This project implements a chatbot using Streamlit that allows users to upload a CSV file and interact with the data through conversational queries. The chatbot utilizes the Llama 2 language model, enhanced with a Retrieval-Augmented Generation (RAG) technique to provide accurate and relevant responses based on the content of the uploaded CSV file.

[![Video Title](Video Thumbnail URL)]([Video URL](https://youtu.be/tmWMl5y34GE))

# Dataset
The dataset used in this project is Clear Quote's March 2024 dataset, available online on GitHub. This dataset contains comprehensive information suitable for various analytical purposes. Users can upload this or any other CSV dataset to interact with through the chatbot.

# Llama 2 Model
Download the llama-2-7b-chat.ggmlv3.q8_0.bin : https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML
the size would be of 7.16GB but that is neccesary to run our model locally.

# RAG Technique
The project employs a Conversational Retrieval Chain, combining document retrieval and language generation:

Document Retrieval: CSV data is embedded into a vector space using HuggingFace's sentence transformer model (sentence-transformers/all-MiniLM-L6-v2).
Conversational Retrieval Chain: The Llama 2 model generates responses to user queries based on the most relevant information retrieved from the vector database.
This approach ensures that responses are grounded in the actual data from the CSV file, enhancing both accuracy and coherence.

# Vector Database
FAISS (Facebook AI Similarity Search) is used as the vector database for this project. FAISS is chosen for its:

Efficiency: Optimized for fast similarity searches and clustering of dense vectors.
Scalability: Capable of handling large datasets efficiently.
Ease of Integration: Seamlessly integrates with Python and the chosen embedding models.

# Minimizing Model Hallucination
To reduce the risk of hallucination, where the model generates plausible-sounding but incorrect information:

* Grounding Responses in Data: Responses are based on actual data from the CSV file.
* Limited Generation Scope: Responses are generated based on retrieved documents.
* Validation and Filtering: Validation checks and response filtering ensure output aligns with the CSV data.

# Checking Response Correctness
To ensure the correctness of LLM responses:

* Reference Data Comparison: Compare responses against known ground truth or reference data.
* Consistency Checks: Implement consistency checks within the conversation.
* Fact-Checking Modules: Integrate automated fact-checking tools to verify factual accuracy.
* User Feedback: Collect feedback from users to fine-tune and improve the model.
* Anomaly Detection: Use statistical methods to detect anomalies in responses.
  
# Installation and Usage
Prerequisites
* Python 3.7 or higher
* Pip

# Installation
* Clone the repository: git clone https://github.com/Sameer103/Chat-with-CSV-Streamlit-Chatbot-using-Llama-2.git

cd chat-with-csv-streamlit

* Install the required packages:

pip install -r requirements.txt

# Running the App
* Start the Streamlit app:

streamlit run app.py

* Upload your CSV file through the sidebar and start interacting with your data.

# Project Structure
* app.py: The main Streamlit application code.
* requirements.txt: List of dependencies required to run the project.

# License
This project is open-source and available under the MIT License.

# Acknowledgements
* Clear Quote for providing the dataset.
* HuggingFace for the transformer models.
* Facebook AI for FAISS.

#Contributions
Contributions are welcome! Please feel free to submit a Pull Request or open an Issue to discuss any changes.

This project is built with ❤️ by AI Anytime.

Feel free to reach out if you have any questions or need further assistance.
