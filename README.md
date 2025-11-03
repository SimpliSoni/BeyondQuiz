# BeyondQuiz 🎓

AI-powered quiz generation platform that helps students learn from their coursebooks through interactive quizzes, intelligent chat assistance, and curated video recommendations.

**🚀 Live Demo:** [https://beyond-quiz.vercel.app/](https://beyond-quiz.vercel.app/))

---

## Features

### Quiz Generation
- Upload PDF coursebooks or select from pre-loaded NCERT textbooks
- AI generates three question types: MCQs, Short Answer, and Long Answer questions
- Intelligent scoring with detailed feedback and explanations
- Progress tracking dashboard with performance analytics

### AI Teacher Chat
- ChatGPT-style interface for document-based Q&A
- Context-aware responses based on uploaded materials
- Persistent chat history across sessions
- Multiple concurrent chat sessions

### Video Recommendations
- AI-curated educational YouTube videos based on document content
- Topic-specific recommendations for enhanced learning

### Progress Tracking
- Comprehensive dashboard showing quiz attempts and scores
- Performance trends and improvement metrics
- Detailed attempt history with feedback summaries

---

## Tech Stack

**Backend:** Flask, PyMongo, Google Gemini 2.5 Flash, PyPDF2  
**Frontend:** HTML5, CSS3, JavaScript, PDF.js  
**Database:** MongoDB Atlas  
**Deployment:** Vercel

---

## Quick Start

### Prerequisites
- Python 3.9+
- MongoDB Atlas account
- Google Gemini API key

### Installation

1. Clone the repository:
```bash
git clone [your-repo-url]
cd beyondquiz
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Configure environment variables:
Create a `.env` file:
```env
MONGO_URI="mongodb+srv://username:password@cluster.mongodb.net/dbname"
GEMINI_API_KEY="your_gemini_api_key"
```

4. Run the application:
```bash
python app.py
```

5. Open `http://127.0.0.1:5000` in your browser

---

## Deployment

Deploy to Vercel:
```bash
vercel
```

Configure environment variables in Vercel Dashboard:
- `MONGO_URI`
- `GEMINI_API_KEY`

---

## Project Structure

```
beyondquiz/
├── app.py                 # Flask backend with API endpoints
├── requirements.txt       # Python dependencies
├── vercel.json           # Vercel configuration
├── templates/
│   └── index.html        # Main application template
└── static/
    ├── style.css         # Application styles
    ├── chat-style.css    # Chat interface styles
    ├── script.js         # Application logic
    └── chat-script.js    # Chat logic
```

---

## API Endpoints

- `POST /api/upload` - Upload PDF coursebook
- `GET /api/pdfs` - List all uploaded PDFs
- `POST /api/generate-quiz` - Generate quiz from PDF
- `POST /api/score-quiz` - Score quiz submission
- `POST /api/chat` - Chat with AI teacher
- `POST /api/recommend-videos` - Get video recommendations
- `GET /api/progress` - Retrieve quiz history

---

## Known Limitations

- PDF visual preview not persistent after refresh (serverless constraint)
- No user authentication (global progress tracking)
- Gemini API rate limits on free tier (handled with retry logic)
- Large PDFs (500+ pages) may experience longer processing times

---

## Future Enhancements

- User authentication and personalized progress
- Cloud storage for persistent PDF previews
- Vector embeddings for semantic search
- Export progress reports
- Spaced repetition scheduling
- Mobile application

---

## License

Apache License 2.0
