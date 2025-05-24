# 🤖 QnA Application with OpenAI and Ollama

An interactive question-answering chatbot app that leverages OpenAI and Ollama models using the Langchain framework — deployed via Streamlit. Built to compare the performance and user experience of commercial and open-source LLMs in a practical use case.

## 📌 Features
* Supports both OpenAI GPT models and open-source LLMs via Ollama
* Real-time Q&A interaction in a Streamlit interface
* Adjustable model settings: temperature, max tokens, and model selection
* Modular, easy-to-extend codebase using Langchain components

## 🧠 Technologies Used
* Streamlit
* Langchain
* OpenAI API
* Ollama (open-source LLM framework)
* Python dotenv
* Prompt Engineering with ChatPromptTemplate

## 🌍 Project Structure
```
├── app.py           # Streamlit app using OpenAI GPT models
├── ollama.py        # Streamlit app using Ollama (open-source LLMs)
├── requirements.txt # All dependencies for environment setup
└── .env             # (You must create this)
```

## ⚙️ Environment Setup
1. Clone the Repo
```
git clone https://github.com/bhaskar2311/QnA-Application-with-OpenAI-and-Ollama
cd QnA-Application-with-OpenAI-and-Ollama
```
2. Create a Virtual Environment (optional but recommended)
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
3. Install Dependencies
```
pip install -r requirements.txt
```
4. Setup Environment Variables
  * Create a .env file in the root directory and add your API keys like this:
```
# .env
OPENAI_API_KEY=your_openai_api_key_here
LANGSMITH_API_KEY=your_langsmith_key_here
```
🔐 Note: Never share your .env file publicly — it contains sensitive keys.

## 🚀 How to Run
#### 🧠 Using OpenAI (app.py)
```
streamlit run app.py
```
* Input your OpenAI API key in the sidebar
* Choose model (e.g., gpt-4o)
* Adjust temperature and max tokens
* Ask your question and view responses in real-time

#### 🦙 Using Ollama (ollama.py)
```
streamlit run ollama.py
```
* Select the open-source LLM (e.g., llama3.1)
* Adjust parameters like temperature and token length
* Ask questions — powered by Ollama


## 📝 Detailed Logic
#### 🔹 app.py – OpenAI Chatbot
* Loads .env using load_dotenv()
* Reads API key from sidebar input
* Sets LangSmith tracking with project metadata
* Uses ChatOpenAI model from Langchain
* Chains prompt → model → output parser
* Supports configurable temperature and max_tokens from UI
* Displays real-time answers in a friendly UI

#### 🔹 ollama.py – Ollama Chatbot
* Similar structure to app.py
* Uses Ollama model via langchain_community.llms
* Requires no API key (for local open-source models)
* Reads model and parameters from Streamlit sidebar
* Uses the same ChatPromptTemplate and StrOutputParser
* Ideal for testing LLMs like llama3.1

## 📦 Reusability
* The requirements.txt is designed for reuse across all LLM projects.
* Only .env setup and model choice will vary.

## 📸 Screenshots
#### With OpenAI
![Output of OPEN AI Project](https://github.com/user-attachments/assets/c99165be-9e19-4ebb-a168-0ba7382fd140)

#### With Ollama
![Output of Ollama AI Project](https://github.com/user-attachments/assets/11cf9021-678a-4910-be31-7638664cb106)

## 📝 Notes
This project was fully developed by me. The README was written based on my knowledge and experience, with support from generative AI tools to refine its structure and presentation.

## 📄 License
This project is open source and available under the MIT License.

## 🙋‍♂️ Author
Made with ❤️ by Bhaskar Shivaji Kumbhar









