# Odyssey: A 30-Day Sustainability Journey
Despite its growing awareness, sustainability often feels confusing, overwhelming, and, for many, unengaging. However, 77% of consumers want to adopt eco-friendly habits (Forbes 2019), yet existing approaches—like flyers and classes—fail to provide actionable, engaging steps. Odyssey is a 30-day challenge app that makes sustainability fun! Each day, complete eco-friendly Quests to reduce waste, save energy, and advocate for the planet. Gamified, AI-powered, and impactful!

Odyssey is a gamified mobile application designed to encourage sustainable living through a series of interactive challenges and engaging storytelling.  Over 30 days, users progress through six chapters, each focusing on a different aspect of sustainability, completing daily quests to unlock new content and ultimately achieve a greener lifestyle.

By Abdullah Naim, Harouna Thiam, Adam Lele, and Yasser Meena

## Features
* **Interactive Storytelling:** Immersive narratives within each chapter engage users and explain the importance of sustainable practices.
* **Daily Quests:**  A series of 5 increasingly challenging quests are presented within each chapter.
* **Gamified Progress:** Users unlock new levels and chapters as they complete quests.
* **AI-Powered Twists:**  After the first chapter, the quests incorporate AI-generated twists to add variability and excitement.  This uses Google Gemini's generative AI capabilities.
* **Progress Tracking:** The app tracks user progress, allowing them to review their achievements and maintain motivation.
* **Personalized Challenges:** The AI can adapt challenges based on user choices.
* **End-of-Journey Celebration:** A celebratory screen rewards users upon completion of all chapters.
* **Background Music:** Ambient background music enhances user experience.

## Usage
The app guides users through a series of chapters and daily quests.  Users interact with the app by reading stories, completing quests (which involve real-world actions), and choosing AI-generated twists for additional challenge. Upon completion of a chapter's quests, the user progresses to the next, eventually completing the 30-day Odyssey.

## Installation
1. **Clone the repository:** `git clone <repository_url>`
2. **Navigate to the project directory:** `cd odyssey`
3. **Install dependencies:** `flutter pub get`
4. **Run the app:** `flutter run`

You'll need to have Flutter installed on your system and a `.env` file with your Google Gemini API key.

```
GEMINI_KEY=<your_gemini_api_key>
```

## Technologies Used
* **Flutter:**  The cross-platform framework for building the user interface.
* **Dart:** The programming language used for Flutter development.
* **Shared Preferences:** Used for local data storage to track user progress.
* **Google Gemini API:** Used for generating AI-powered twists to challenges (requires API key).  This uses the `http` package for API calls and `flutter_dotenv` for secure key management.
* **Audioplayers:** Used for background music playback.
* **Confetti:**  Used for visual celebratory effects.
* **Scratcher:** Used to create a scratch-off effect for revealing quest details.

## API Documentation
The app uses the Google Gemini API for generating creative variations of the daily quests.  The API call is structured as a POST request to `https://generativelanguage.googleapis.com/v1/models/gemini-pro:generateContent`.  The request body is a JSON object containing the prompt for the AI to process. The response is a JSON object containing the generated text.

**Request Example:**

```json
{
  "contents": [
    {
      "parts": [
        {"text": "Modify \"Plant a tree\" by adding a cooperative element that requires players to work together in an interesting way while maintaining the challenge’s original intent."}
      ]
    }
  ]
}
```

**Response Example:**

```json
{
  "candidates": [
    {
      "content": {
        "parts": [
          {
            "text": "Organize a community tree-planting event with friends or neighbors.  Coordinate the planting effort, and share photos of your collaborative success."
          }
        ]
      }
    }
  ]
}
```

## Dependencies
The project uses the following dependencies, all specified in the `pubspec.yaml` file:

* `flutter`
* `shared_preferences`
* `http`
* `flutter_dotenv`
* `audioplayers`
* `confetti`
* `scratcher`

*README.md was made with [Etchr](https://etchr.dev)*
