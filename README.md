
 AI Genesis - Integrated Study & Research Assistant

An advanced AI-powered study companion that combines document processing, research capabilities, and educational content generation in one comprehensive platform.

 Features

 Document Processing & Analysis
- PDF Upload & Processing: Upload multiple PDFs and create a searchable vector database
- Intelligent Q&A: Ask questions about your documents and get contextual answers with source citations
- Topic Summarization: Generate comprehensive summaries on specific topics or entire document collections

 Study Materials Generation
- Practice Exams: Create customized practice exams with multiple-choice questions, explanations, and difficulty levels
- Flashcards: Generate interactive flashcards from your documents or specific topics
- File-Based Content: Create study materials directly from PDF, DOCX, and PPTX files

 Research Assistant
- Academic Resource Discovery: Automatically find relevant academic papers and resources from trusted sources
- Concept Explanation: Get detailed explanations of complex academic concepts
- Comprehensive Research: Conduct thorough research on any academic topic with multiple source integration

 Installation

 Prerequisites
- Python 3.8 or higher
- CUDA-compatible GPU (optional, for better performance)
- Groq API key (for LLM functionality)

 Dependencies
bash
pip install torch transformers requests beautifulsoup4 numpy gradio
pip install langchain chromadb sentence-transformers
pip install python-docx python-pptx PyPDF2

 Clone and Setup
bash
git clone <repository-url>
cd integrated-study-assistant
pip install -r requirements.txt


 Quick Start

1. Run the Application
   bash
   python main.py
   

2. Access the Interface
   - Open your browser and navigate to the provided local URL (typically `http://127.0.0.1:7860`)
   - Or use the public share link for remote access

3. Initialize the Assistant
   - Go to the "Setup" tab
   - Enter your Groq API key
   - Click "Initialize Assistants"

4. Upload Documents
   - Upload your PDFs in the "Setup" tab
   - Click "Process PDFs" to create the vector database

5. Start Learning
   - Navigate to different tabs to use various features
   - Ask questions, generate exams, create flashcards, or conduct research

 Usage Guide

 Setup Tab
- Initialize Assistants: Configure the AI models with your API key
- Upload PDFs: Add your study materials to the system
- Process Documents: Create searchable vector embeddings

 Ask Questions Tab
- Enter questions about your uploaded documents
- Get contextual answers with source citations
- Perfect for quick fact-checking and concept clarification

 Generate Materials Tab
- Summaries: Create topic-specific or general document summaries
- Flashcards: Generate study flashcards with questions and answers
- Specify the number of flashcards needed

 File-Based Flashcards Tab
- Upload individual files (PDF, DOCX, PPTX)
- Generate flashcards directly from file content
- Supports various document formats

 Research Assistant Tab
- Enter any academic topic for comprehensive research
- Automatically finds relevant academic resources
- Provides detailed concept explanations
- Links to trusted academic databases

 Configuration

 Supported LLM Providers
- Groq: Fast inference with Llama models (default)
- Hugging Face: Local model execution
- OpenAI: GPT models (with API key)

 Trusted Academic Sources
- Google Scholar
- Semantic Scholar
- arXiv
- ResearchGate
- Educational institutions (.edu domains)
- Research organizations (.org domains)

 Model Configuration
The application uses Googles FLAN-T5-Large model for local processing and Groqs Llama models for advanced reasoning tasks.

 API Keys

 Groq API Key
1. Get your API key through the website
2. Create an account or sign in
3. Generate a new API key
4. Enter the key in the Setup tab

 Security Notes
- API keys are used only for model inference
- No data is permanently stored or transmitted
- All processing happens locally except for LLM calls

 File Structure


integrated-study-assistant/
├── main.py                  Main application file
├── requirements.txt         Python dependencies
├── README.md               This file
├── temp/                   Temporary files (auto-created)
│   ├── pdfs/              Uploaded PDF storage
│   └── vectordb/          Vector database files
└── models/                Local model cache (auto-created)


 Use Cases

 Students
- Exam Preparation: Generate practice tests from lecture notes and textbooks
- Research Projects: Find academic sources and understand complex concepts
- Study Sessions: Create flashcards and summaries for efficient review

 Educators
- Content Creation: Generate assessment materials from course documents
- Research Support: Help students find relevant academic resources
- Concept Explanation: Provide detailed explanations of difficult topics

 Researchers
- Literature Review: Quickly process and summarize research papers
- Concept Exploration: Understand new fields and related topics
- Resource Discovery: Find relevant papers and academic sources

Technical Details

 Architecture
- Frontend: Gradio web interface
- Backend: Python with Transformers and LangChain
- Vector Database: ChromaDB for document embeddings
- LLM Integration: Multiple provider support (Groq, HuggingFace, OpenAI)

 Processing Pipeline
1. Document ingestion and text extraction
2. Text chunking and embedding generation
3. Vector database creation and indexing
4. Query processing and similarity search
5. Context-aware response generation

 Performance Optimizations
- GPU acceleration for model inference
- Efficient vector search algorithms
- Optimized text processing and chunking
- Caching for frequently accessed content

Troubleshooting

 Common Issues

"Error initializing assistants"
- Verify your API key is valid and active
- Check internet connection for model downloads
- Ensure sufficient disk space for model caching

"No PDFs uploaded yet!"
- Upload PDFs in the Setup tab before processing
- Ensure PDF files are not corrupted or password-protected
- Check file size limits (recommended < 50MB per file)

"Unable to generate response"
- Check API key validity and rate limits
- Verify document processing completed successfully
- Try shorter, more specific questions

 Performance Tips
- Use GPU acceleration when available
- Process smaller batches of documents for faster initialization
- Clear temporary files periodically to free disk space

Contributing

We welcome contributions! Please feel free to submit issues, feature requests, or pull requests.

 Development Setup
1. Fork the repository
2. Create a virtual environment
3. Install development dependencies
4. Make your changes and test thoroughly
5. Submit a pull request with detailed description

License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments

- Hugging Face for transformer models and libraries
- Groq for fast LLM inference
- LangChain for document processing capabilities
- Gradio for the intuitive web interface
- ChromaDB for efficient vector storage

Support

For support, issues, or feature requests:
- Open an issue on GitHub
- Check the troubleshooting section above
- Review the documentation and examples

