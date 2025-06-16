# SarkasamAI
Advanced Sarcasm Detection System powered by Machine Learning and AI

📋 Overview
Sarkasam AI is a professional-grade sarcasm detection system that combines traditional machine learning with cutting-edge AI to identify and explain sarcastic content in text. The system offers two distinct analysis modes and provides detailed AI-powered explanations for its predictions.
✨ Key Features

🎯 High Accuracy: Achieves 84%+ accuracy using Bernoulli Naive Bayes
🤖 AI-Powered Explanations: Detailed analysis using Google's Gemini 2.0 Flash
📝 Dual Analysis Modes:

Single text analysis
Conversation context analysis


💬 Context-Aware: Understands sarcasm in conversational contexts
📊 Confidence Scoring: Provides prediction confidence levels
🎨 Professional Interface: Clean, user-friendly command-line interface

🚀 Quick Start
Prerequisites

Python 3.7 or higher
Google AI Studio API key
Sarcasm dataset (JSON format)

Installation

Clone the repository
bashgit clone https://github.com/yourusername/sarkasam-ai.git
cd sarkasam-ai

Install required packages
bashpip install -r requirements.txt

Get Gemini API Key

Visit Google AI Studio
Create a new API key
Copy your API key


Configure the system

Open the main script
Replace "YOUR_GEMINI_API_KEY_HERE" with your actual API key
Ensure your sarcasm dataset is at /content/Sarcasm.json


Run the application
bashpython sarkasam_ai.py


📦 Dependencies
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
google-generativeai>=0.3.0
🎯 Usage
Option 1: Single Text Analysis
Perfect for analyzing individual sentences, paragraphs, or social media posts.
Enter text to analyze: "Oh great, another meeting that could have been an email."
Classification: SARCASTIC
Confidence: 87.5%
Option 2: Conversation Analysis
Ideal for analyzing responses in context of the original message.
Enter your original message: "Did you finish the report?"
Enter the response you received: "Oh absolutely, I had nothing better to do all weekend."
Response Classification: SARCASTIC
Confidence: 92.3%
🏗️ System Architecture
┌─────────────────────────────────────────────────────────────┐
│                    Sarkasam AI System                       │
├─────────────────────────────────────────────────────────────┤
│  Input Layer                                                │
│  ├─ Single Text Input                                       │
│  └─ Conversation Context Input                              │
├─────────────────────────────────────────────────────────────┤
│  Processing Layer                                           │
│  ├─ Text Preprocessing (CountVectorizer)                    │
│  ├─ Feature Extraction                                      │
│  └─ ML Classification (Bernoulli Naive Bayes)              │
├─────────────────────────────────────────────────────────────┤
│  AI Analysis Layer                                          │
│  ├─ Context Understanding                                   │
│  ├─ Pattern Recognition                                     │
│  └─ Explanation Generation (Gemini 2.0 Flash)              │
├─────────────────────────────────────────────────────────────┤
│  Output Layer                                               │
│  ├─ Sarcasm Classification                                  │
│  ├─ Confidence Score                                        │
│  └─ Detailed AI Explanation                                 │
└─────────────────────────────────────────────────────────────┘
📊 Performance Metrics

Accuracy: 84.48%
Training Dataset: News Headlines Sarcasm Dataset
Model: Bernoulli Naive Bayes
Features: Count Vectorization
Response Time: < 2 seconds per analysis

🛠️ Configuration
Dataset Format
The system expects a JSON Lines file with the following structure:
json{"headline": "Text content here", "is_sarcastic": 1}
{"headline": "Another text sample", "is_sarcastic": 0}
API Configuration
pythonGEMINI_API_KEY = "your-api-key-here"
DATA_PATH = "/path/to/your/sarcasm.json"
🔧 Advanced Usage
Custom Training
To train with your own dataset:

Format your data as JSON Lines
Ensure columns: headline and is_sarcastic
Update the DATA_PATH variable
Run the system

Batch Processing
For processing multiple texts programmatically:
pythondetector = SarcasmDetector(api_key)
detector.load_and_train_model(data_path)

texts = ["Text 1", "Text 2", "Text 3"]
for text in texts:
    prediction, confidence = detector.predict_sarcasm(text)
    print(f"{text}: {prediction} ({confidence:.2%})")
🤝 Contributing
We welcome contributions! Please follow these steps:

Fork the repository
Create a feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request

📝 License
This project is licensed under the MIT License - see the LICENSE file for details.
🙏 Acknowledgments

Dataset: News Headlines Dataset for Sarcasm Detection
ML Framework: scikit-learn
AI Model: Google Gemini 2.0 Flash
Inspiration: Natural Language Processing community

📞 Support
For support, questions, or suggestions:

📧 Email: support@sarkasamai.com
🐛 Issues: GitHub Issues
📖 Documentation: Wiki

🔄 Changelog
v1.0.0 (Current)

✅ Initial release
✅ Bernoulli Naive Bayes implementation
✅ Gemini 2.0 Flash integration
✅ Dual analysis modes
✅ Professional CLI interface

Upcoming Features

🔜 Web interface
🔜 API endpoints
🔜 Multiple language support
🔜 Real-time social media integration
