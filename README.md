# Book Recommendations System

A machine learning-powered book recommendation engine using OpenAI embeddings and FAISS for efficient similarity search.

## What It Is

An intelligent book recommendation platform that analyzes book summaries and reviews to suggest titles based on user preferences. The system processes over 45,000 books, generates semantic embeddings, indexes them with FAISS, and serves recommendations through an intuitive React interface. The backend runs on Google Cloud, while the frontend is hosted on GitHub Pages.

## Tech Stack

### Backend (Python)
- **Flask**: REST API server
- **OpenAI**: Text embeddings for semantic understanding
- **FAISS**: Facebook AI Similarity Search for fast indexing
- **Data Processing**: pandas, numpy
- **Hosting**: Google Cloud

### Frontend (React)
- **Framework**: React 19
- **Build Tool**: Create React App
- **HTTP Client**: Axios
- **Testing**: React Testing Library
- **Hosting**: GitHub Pages

## Getting Started

### Frontend Setup

```bash
cd book-reccomendations-r
npm install
npm start
```

The frontend will be available at `http://localhost:3000`

### Development & Deployment

```bash
# Build for production
npm run build

# Deploy to GitHub Pages
npm run deploy
```

### Backend Setup

Note: Backend requires OpenAI API key and is typically pre-deployed to Google Cloud.

```bash
# For local development
pip install flask openai faiss-cpu pandas numpy
python app.py
```

## Features

- **Book Browsing**: Explore thousands of books with titles, authors, and genres
- **Like System**: Mark favorite books to personalize recommendations
- **Smart Recommendations**: AI generates similar books based on your preferences
- **Book Details**: View full summaries and metadata
- **Efficient Search**: FAISS enables fast similarity matching across 45,000 books

## How It Works

1. **Data Processing**: 45,000 book summaries and reviews are processed
2. **Embeddings**: OpenAI converts text to semantic vectors
3. **Indexing**: FAISS indexes embeddings for O(1) lookup
4. **User Interaction**: Users like books via the React interface
5. **Recommendation**: System finds similar books using cosine similarity
6. **Display**: Results shown with relevance scores

## Project Structure

```
book-reccomendations-r/
├── src/
│   ├── components/        # React components
│   ├── App.jsx           # Main app
│   └── index.jsx         # Entry point
├── public/               # Static files
├── build/                # Production build
├── package.json
└── README.md
```

## Data

The system uses:
- **Dataset**: 45,000 books from major publishers
- **Metadata**: Titles, authors, genres, descriptions
- **Summaries**: Full book summaries for analysis
- **Reviews**: User review data for enhanced understanding

## Acknowledgements

- [OpenAI](https://openai.com/) - Embedding models
- [FAISS](https://github.com/facebookresearch/faiss) - Similarity search
- [Facebook AI Research](https://ai.facebook.com/) - FAISS algorithm
- [Create React App](https://create-react-app.dev/) - Frontend tooling
- [Flask](https://flask.palletsprojects.com/) - Backend framework

## Development Notes

- Frontend deployed to GitHub Pages for free hosting
- Backend deployed on Google Cloud for scalability
- All API calls to backend are CORS-enabled
- Book data is preprocessed and indexed beforehand
- Recommendations use cosine similarity on embeddings
