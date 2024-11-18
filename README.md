![yoututorlogo](https://github.com/user-attachments/assets/bb9d6754-9d51-4de6-a466-5d606854d277)

#YouTutor: Personalized Learning Assistant 🎓🤖

Transform your learning experience with YouTutor, an AI-powered educational assistant that curates, summarizes, and personalizes YouTube content to align with your goals. 📚✨

#📋 Table of Contents

Introduction
🚀 Workflow Diagram
⚙️ Setup and Installation
🛠️ Detailed Component Descriptions
🎯 Usage Example
⚡ Limitations and Future Improvements
🔗 References

#📖 Introduction
YouTutor is your personalized AI learning assistant, designed to enhance your educational journey by leveraging the vast repository of YouTube's educational content. It provides:

Tailored Playlists: Personalized video recommendations matching your interests and skill level. 🎥
AI Summaries: Concise summaries for quick video insights. 📝
Structured Learning Path: Curated playlists for a seamless, focused learning experience. 📂
Key Features:

🧠 Knowledge assessment based on your expertise level and goals.
🎯 Relevant video recommendations using YouTube Data API.
✨ AI-powered summaries with OpenAI GPT models.
💻 Interactive user interface via Streamlit.

🚀 Workflow Diagram!

![Screenshot 2024-11-17 at 10 13 57 AM](https://github.com/user-attachments/assets/8467f02a-8737-45dc-9945-d0b6a1bf10e1)


⚙️ Setup and Installation
Follow these steps to set up YouTutor and start your personalized learning journey:

1️⃣ Install Required Packages
Install all necessary Python libraries:

!pip install -q google-api-python-client langchain-community openai python-dotenv gtts streamlit pyngrok
2️⃣ Set Up Environment Variables
Securely input your API keys:

from getpass import getpass
import os

# Securely input your API keys
os.environ['YOUTUBE_API_KEY'] = getpass('Enter your YouTube API Key: ')
os.environ['OPENAI_API_KEY'] = getpass('Enter your OpenAI API Key: ')
3️⃣ Import Libraries and Modules
Import essential libraries for functionality:

import os
import streamlit as st
from pydantic import BaseModel
from typing import List, Dict
import openai
from googleapiclient.discovery import build
4️⃣ Define Base Classes and Agents
Build the components such as YouTubeAgent, SummarizationAgent, and PlaylistGenerator. Full class definitions are included in the repository.

🛠️ Detailed Langchain/Langgraph Agents Component Descriptions

![yoututor-KUnZxy2tFwQp5Nb3s5RGqX](https://github.com/user-attachments/assets/c1901097-448c-4384-b8aa-4c70c582d44f)


📊 KnowledgeAssessmentAgent
Purpose: Captures user inputs such as experience level, topics of interest, and learning goals.
Output: A UserPreferences object passed to other agents.

🔍 YouTubeAgent
Purpose: Fetches relevant videos from YouTube based on user preferences.
Technology Used: YouTube Data API.

✨ PersonalizationAgent
Purpose: Filters videos to match the user’s preferences.

📝 SummarizationAgent
Purpose: Uses OpenAI GPT models to generate concise summaries for video descriptions.

🎥 PlaylistGenerator
Purpose: Organizes personalized video data into a clickable HTML playlist.

💻 User Interface (Streamlit)
Purpose: Provides an interactive platform for user interaction and playlist display.

![dashboard for the Streamlit appFvtzwRU5mhj9tF2bCWSnMS](https://github.com/user-attachments/assets/88748493-e228-42f7-ad88-5b842819c009)

#🎯 Usage Example

1️⃣ Knowledge Assessment
Users input their:
Experience Level (e.g., Beginner, Intermediate, Advanced).
Topics of Interest (e.g., Python, Data Analysis).
Learning Goals (e.g., Build a data visualization tool).

2️⃣ Video Search and Personalization
Videos are fetched and filtered:
YouTubeAgent searches for videos.
PersonalizationAgent selects relevant results.

3️⃣ Summarization and Playlist Generation
AI summaries provide quick insights:
SummarizationAgent processes video descriptions.
Curated playlists are created:
PlaylistGenerator organizes videos with clickable links.
Sample Output
Videos:

Python Tutorial for Beginners

Summary: Comprehensive introduction to Python programming for beginners.
Data Analysis with Python

Summary: Learn data analysis using Python libraries like pandas and matplotlib.
Generated Playlist:

<a href="https://www.youtube.com/watch?v=XXXXXXXXXXX" target="_blank">Python Tutorial for Beginners</a><br>
<a href="https://www.youtube.com/watch?v=YYYYYYYYYYY" target="_blank">Data Analysis with Python</a>

⚡ Limitations and Future Improvements

🔻 Current Limitations
API Rate Limits: Limited requests to YouTube and OpenAI APIs.
Language Support: Currently supports English content only.

🚀 Future Improvements
Enhanced Personalization:
Add sentiment analysis and topic modeling.
Feedback Loop:
Allow users to rate and review recommendations.
Multi-Language Support:
Expand functionality to support additional languages.
Offline Caching:
Implement local caching for frequently accessed videos.

🔗 References
YouTube Data API Documentation
OpenAI API Documentation
LangChain Documentation
Streamlit Documentation
Google API Python Client
Pyngrok Documentation

🌐 Quick Links
Run YouTutor on Google Colab: Launch Here
GitHub Repository: View Code
Demo Video: Watch on YouTube

💡 Pro Tip: Share your feedback and contribute to YouTutor's development on GitHub. Together, we can make learning smarter and more personalized! 🌟
