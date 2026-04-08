# Echo – Multimodal AI Virtual Assistant

Echo is a high-performance, voice-driven AI ecosystem that goes beyond simple chatbots. It utilizes a **Multi-Layered Decision Model (DMM)** to classify user intent and execute complex workflows, including real-time web intelligence, image generation, and system automation.

## 🚀 Key High-Level Features

* **Intelligent Intent Routing:** Uses a custom-prompted Cohere `command-r-plus` model to classify queries into `general`, `realtime`, `automation`, or `image generation`.
* **Real-time Intelligence (RAG):** Combines Google Search scraping with Llama-3-70B to provide up-to-date information, bypassing the knowledge cutoff of standard LLMs.
* **Task Automation:** Asynchronous execution of system commands, application control (AppOpener), and web searches.
* **Multimodal Capabilities:** Integrated Stable Diffusion (via HuggingFace) for text-to-image generation and Edge-TTS for natural, human-like voice synthesis.

## 🧠 System Architecture

Echo isn't just a script; it's a modular pipeline:

1. **Input Layer:** Headless Selenium-based Speech Recognition for high-accuracy voice-to-text.
2. **Brain Layer (DMM):** A Cohere-powered classifier that decides if a query needs a search engine, a creative writer, or a system command.
3. **Action Layer:** * `Chatbot.py`: Handles general conversational logic using Groq-hosted Llama-3.
   * `Automation.py`: Manages asynchronous system tasks using `asyncio`.
   * `RealtimeSearchEngine.py`: Performs live web-scraping to augment AI responses.
4. **Output Layer:** Dynamic TTS that adjusts response length based on content complexity.

## 🛠️ Tech Stack

* **LLMs/APIs:** Groq (Llama-3-70B/8B), Cohere (Command-R+), HuggingFace (Stable Diffusion XL).
* **Languages & Libraries:** Python, Selenium (Voice UI), Pygame (Audio), PyQt5 (GUI), Asyncio.
* **Data Handling:** JSON-based persistent chat logging for context-aware conversations.

## 🔧 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/kanan-pandey1612/Echo.git
   ```

2. **Install dependencies:**
   ```bash
   pip install -r Requirements.txt
   ```

3. **Configure your `.env` file** (see `.env.example`):
   * `GroqAPIKey`, `CohereAPIKey`, `HuggingFaceAPIKey`.

## 📈 Future Scope

* **Contextual Memory:** Moving from JSON logs to a Vector Database (like ChromaDB) for long-term user memory.
* **EdTech Integration:** Fine-tuning the persona to act as a Socratic math tutor, aligning with interactive learning platforms.