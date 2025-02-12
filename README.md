## 🏆 **ML FIesta IIIT Bangalore Winning Project**

# Sandalwood Knowledge Preservation System
### MLFIESTA Hackathon Project by Team Init.io

## 👥 Team Members
- Mayank Ravariya
- Asim Shah
- Vinayak Bhatia

*Sardar Patel Institute of Technology*

## 🎯 Project Overview
This project develops a cutting-edge system for preserving and accessing indigenous knowledge about sandalwood cultivation in Karnataka, India. It combines Automatic Speech Recognition (ASR) with an advanced question-answering system to make traditional knowledge accessible and searchable.

## 🌟 Key Features
- Kannada speech recognition optimized for colloquial language
- Real-time translation pipeline (Kannada to English)
- Semantic search capabilities using RAG architecture
- Time-aligned audio segment retrieval
- Interactive query interface supporting both text and voice input

## 🏗️ System Architecture

```mermaid
flowchart TD
    A[Audio Input] --> B[ASR System]
    B --> C[Chunking Module]
    C --> D[LangChain + Gemini]
    D --> E[Translation Pipeline]
    E --> F[FAISS Vector DB]
    G[User Query] --> H[Query Processor]
    H --> I[RAG Model]
    F --> I
    I --> J[Response Generator]
    J --> K[Time-aligned Results]
    K --> L[Audio Segments]
    K --> M[Kannada Transcription]
    K --> N[English Translation]
```

## 🔄 Workflow

```mermaid
sequenceDiagram
    participant U as User
    participant ASR as ASR System
    participant T as Translation Pipeline
    participant DB as Vector Database
    participant QA as QA System
    
    U->>ASR: Submit Audio
    ASR->>ASR: Chunk Audio (10s)
    ASR->>T: Process Chunks
    T->>T: Translate (Kannada to English)
    T->>DB: Index Translations
    U->>QA: Submit Query
    QA->>DB: Search Similar Content
    DB->>QA: Return Relevant Segments
    QA->>U: Present Results with Audio
```

## 🛠️ Technical Implementation

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/sandalwood-knowledge-system.git

# Navigate to project directory
cd sandalwood-knowledge-system

# Create virtual environment
python -m venv venv

# Activate virtual environment
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt
```

### ASR Pipeline
1. Initial transcription using foundational models
2. Audio chunking into 10-second segments
3. Translation using LangChain-powered Gemini
4. Time-aligned parallel corpus creation

### QA System
1. RAG (Retrieval-Augmented Generation) architecture
2. FAISS vector database for semantic search
3. Sentence Transformer embeddings
4. Contextual relevance scoring

## 📊 Dataset
- **Source**: YouTube content on sandalwood cultivation
- **Language**: Colloquial Kannada
- **Characteristics**:
  - Informal speech patterns
  - Background noise
  - Various recording qualities
  - Local dialects

## 🎯 Achievements
- Successful handling of colloquial Kannada despite language barriers
- Innovative chunking method for precise time alignment
- Deep contextual analysis through RAG implementation
- Seamless integration of multiple cutting-edge technologies

## youtube video

Link : https://youtu.be/v5HhDsml4Aw

## output

![Screenshot 2024-11-17 235707](https://github.com/user-attachments/assets/9378f8b6-aef4-4e8a-9038-2fffd5e5ae47)
![Screenshot 2024-11-17 235330](https://github.com/user-attachments/assets/8bcb0676-44fe-488f-b051-3c88de9ba7ce)

## 📝 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



