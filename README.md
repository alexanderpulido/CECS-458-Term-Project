# CECS-458-Team-Project
Term Project for Group 3 CSULB CECS 458 Deep Learning Spring 2026

This is a Netflix-style movie discovery website powered by an AI chatbot.

How to Run:
Step 1 — Open the file

Step 2 — Get your API keys (TMDB API Key, Gemini API Key)

Step 3 — Enter keys and launch 

Step 4 - Use AI powered system
- AI Chatbot (Two Entry Points)
- AI Search button — next to the search bar in the navigation. Click it to open the chatbot in search mode.
- AI Movie Chat button — floating red button in the bottom-right corner. Always visible while scrolling. Click it to open the chatbot in chat mode.

How the AI Works
- The chatbot is called CineAI. Here is what happens when you send a message:
A function called buildSystemPrompt() builds a text list of all 24 movies — title, year, genres, rating, and a short description from TMDB
That list is sent to Gemini as a system instruction before every chat message

- Gemini follows these 7 rules:
Only recommend movies from the list — never make up a title
Be warm and conversational
Ask one follow-up question per response to learn more about your preferences
Format each recommendation as Movie Title (Year) ★rating — reason
Include a match percentage (e.g., "97% match")
Keep responses under 220 words
Occasionally mention that data comes from MovieLens + TMDB

- The full conversation history is sent with every message, so the chatbot remembers what you said before and can refine its suggestions

