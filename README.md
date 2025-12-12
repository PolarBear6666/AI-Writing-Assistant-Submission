# AI-Writing-Assistant-Submission
AI Writing Assistant (Java MVC + Strategy)
# AI Writing Assistant (Java MVC + Strategy Pattern)

This project is a desktop application developed in Java Swing that serves as an AI Writing Assistant. It interacts with the OpenAI API for text generation and demonstrates several core software engineering principles, including the Model-View-Controller (MVC) pattern and Object Serialization for persistence.

## ⚙️ Core Technologies & Architecture

* **Language:** Java (Built with Java SDK 24)
* **Architecture:** Model-View-Controller (MVC)
* **API Integration:** OpenAI Chat Completions API (`gpt-3.5-turbo`)
* **Dependencies:** Jackson (for JSON handling), Java HttpClient.
* **Design Patterns:** Strategy Pattern (for dynamic writing modes).
* **Persistence:** Java Object Serialization (for session management).

## ✨ Key Features Implemented

1.  **Asynchronous Text Generation:** The application makes non-blocking API calls, preventing the UI from freezing while waiting for the AI response.
2.  **Strategy Pattern Implementation:** Allows users to select different `WritingStrategy` modes (Creative, Professional, etc.) which dynamically changes the system prompt sent to the AI.
3.  **Complete Session Management:** Users can **Save Session** and **Load Session** buttons to serialize and deserialize the entire conversation history (Input/Output pairs) using the `WritingSession` model.
4.  **Robust API Parsing:** Includes necessary `@JsonIgnoreProperties` annotations across the `OpenAIResponse` model to handle new, unrecognized fields from the OpenAI API gracefully.

## 🚀 Setup & Run Instructions

To run this application, you must have the Java SDK installed and set up your OpenAI API key as an environment variable.

### 1. Set Environment Variable (Crucial)

The application requires your secret key to be set as a system environment variable for security.

* **Variable Name:** `OPENAI_API_KEY`
* **Variable Value:** Your `sk-proj-` key obtained from the OpenAI platform.

*(If using IntelliJ IDEA, you can set this variable in the **Run/Debug Configurations** menu under "Environment variables.")*

### 2. Compile and Run

1.  Clone this repository or open the project folder in your Java IDE (IntelliJ IDEA recommended).
2.  Ensure all Maven/Gradle dependencies (Jackson) are downloaded.
3.  Compile and run the `Main.java` class.

### 3. Usage

1.  Select a **Mode** from the dropdown (e.g., Creative Storytelling).
2.  Type a prompt in the **Your Input Prompt:** box.
3.  Click **Generate Text**.
4.  To save your conversation history, click **Save Session** and choose a `.session` file name.
