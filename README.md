# 🎓 AI Course Architect

AI Course Architect is a full-stack Streamlit application that uses cutting-edge AI models to automatically generate comprehensive educational courses on any topic. It also integrates video content, quizzes, and PDF export features to provide a complete learning experience.

## 🚀 Features

- ✍️ **Course Generation**: Creates structured courses with titles, descriptions, learning objectives, main topics, subtopics, summaries, and key takeaways using **Groq’s LLaMA 3-70B** model.
- 🔍 **Smart Search**: Optionally enhance course content with real-time Google Search data and YouTube videos using the **Google Search API** and **YouTube Data API**.
- 📺 **Video Integration**: Embeds relevant YouTube videos per topic and subtopic using optimized queries.
- 🧠 **Quiz Generation**: Automatically generates multiple-choice quizzes with explanations to test learners.
- 📄 **Export as PDF**: Download beautifully formatted course content and quizzes as offline-readable PDFs.
- 🧪 **Interactive UI**: User-friendly interface built with **Streamlit** for smooth navigation and configuration.

---

## 🛠 Tech Stack

- **Frontend**: [Streamlit](https://streamlit.io/)
- **AI Model**: [Groq API](https://console.groq.com/) using `llama3-70b-8192`
- **Search APIs**: Google Custom Search API, YouTube Data API
- **PDF Export**: ReportLab
- **Environment**: Python 3.10+

---

## 📦 Installation

1. **Clone the repository**:

```bash
git clone https://github.com/Krish-Mistry-04/AI_Course_Architect.git
cd AI_Course_Architect
```

2. **Install dependencies**:
```bash
pip install -r requirements.txt
```

3. **Create .env file with your API keys**:
```env
GROQ_API_KEY=your_groq_api_key
GOOGLE_API_KEY=your_google_api_key
GOOGLE_CSE_ID=your_google_cse_id
```
## 🚀 Usage

1. Run the Streamlit app:
   ```
   streamlit run app.py
   ```

2. Enter a course topic in the input field
3. Configure options:
   - Toggle Google Search integration for additional context
   - Enable YouTube video integration for visual learning content
   - Adjust advanced settings like temperature and token count
   - Enable quiz generation
4. Click "Generate Course" to create your educational content
5. Navigate between course content and quiz using the tabs
6. Download content as PDF for offline use

## 📊 Advanced Options

- **Temperature**: Controls the creativity/randomness of the generated content (0.0-1.0)
- **Max Tokens**: Limits the length of the generated content
- **Videos Per Topic**: Sets the number of YouTube videos to fetch per topic
- **Quiz Questions**: Configures the number of questions to generate

## 📱 User Interface

The application has three main views:
1. **Course Generator**: Enter topic and configure generation settings
2. **Course View**: Browse the generated course content with expandable topics
3. **Quiz**: Take the generated quiz and see your results

## 🔄 Workflow

1. Enter your topic and configure options
2. The app fetches relevant information from Google (if enabled)
3. The Groq API generates structured course content
4. YouTube videos are fetched and integrated (if enabled)
5. Quiz questions are generated based on course content (if enabled)
6. Course and quiz are saved as JSON files locally
7. PDF export options allow you to save content for offline use

## 🛑 Limitations

- Requires valid API keys for full functionality
- Content quality depends on the AI model's knowledge and limitations
- YouTube integration requires Google API key with YouTube Data API v3 enabled
- Search integration requires Google API key with Custom Search API enabled

## 🧩 Architecture

The application follows a modular design with components for:
- Course generation
- Quiz generation
- PDF export
- User interface
- External API integrations (Groq, Google Search, YouTube)
