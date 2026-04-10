💎 Jewellery RAG-Based Recommendation System

An advanced Retrieval-Augmented Generation (RAG) system designed to enhance jewellery discovery through semantic search and multimodal intelligence. The platform enables users to find relevant jewellery products using both natural language queries and image-based inputs, delivering highly accurate and context-aware recommendations.

📌 Overview

This project integrates vector search, computer vision, and large language models (LLMs) to build an intelligent recommendation engine tailored for the jewellery domain. It leverages embeddings, OCR, and vision-based reasoning to provide a seamless and scalable product search experience.

🚀 Key Features
Hybrid Semantic Search
Combines vector similarity with keyword-based scoring to improve retrieval precision.
Multimodal Search Capability
Supports both text queries and image uploads for product discovery.
OCR-Driven Metadata Extraction
Extracts textual information such as brand names and labels from images to enhance search relevance.
High-Performance Vector Retrieval (FAISS)
Enables efficient similarity search across large-scale datasets.
Responsive Web Interface
Provides a clean and user-friendly interface for real-time interaction.
🛠️ Technology Stack
Layer	Technologies
Backend	Python, FastAPI, Uvicorn
Vector Database	FAISS
AI/ML Models	OpenAI Embeddings, Gemini Vision LLM, PaddleOCR
Data Processing	Pandas, NumPy, Pillow
Frontend	HTML5, CSS3, JavaScript
⚙️ System Workflow
🔹 Text-Based Retrieval
User query is converted into a vector embedding
FAISS performs similarity search on indexed data
Results are ranked using hybrid scoring:
Final Score = (0.7 × Vector Similarity) + (0.3 × Keyword Matching)
🔹 Image-Based Retrieval
Uploaded image is processed using PaddleOCR for text extraction
A Vision LLM (Gemini) generates a semantic description
The generated description is used as input for the retrieval pipeline
📦 Installation & Setup
Prerequisites
Python 3.9 or above
API keys for LLM services
Setup Instructions
# Clone the repository
git clone https://github.com/ARUN-GR05/jewellery_RAG_basedReccomendation.git

# Navigate to project directory
cd jewellery_RAG_basedReccomendation

# Install dependencies
pip install -r backend/requirements.txt
Environment Configuration

Create a .env file inside the backend/ directory:

GPT_API_KEY=your_api_key_here
GPT_BASE_URL=your_base_url_here

⚠️ Ensure .env is excluded from version control.

Run the Application
cd backend
python main.py

Access the application at:
👉 http://localhost:8000

🚀 Deployment
Render (FastAPI Backend)
Build Command
pip install -r backend/requirements.txt
Start Command
uvicorn backend.main:app --host 0.0.0.0 --port $PORT
Configure environment variables in the deployment dashboard
📂 Project Structure
backend/
 ├── src/            # Core modules (OCR, embeddings, retrieval)
 ├── data/           # FAISS index & metadata
 ├── main.py         # Application entry point
 └── .env

frontend/
 ├── index.html
 ├── style.css
 └── script.js
📈 Future Enhancements
Personalized recommendation engine
Voice-based search integration
AR-based jewellery try-on
Advanced filtering and ranking mechanisms
🤝 Contribution

Contributions are welcome. Please feel free to submit issues or pull requests to improve functionality, performance, or user experience.

📄 License

This project is intended for academic and research purposes.
