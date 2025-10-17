# Smart Task Planner AI

An intelligent web application that uses the Google Gemini API to break down high-level goals into detailed, actionable project plans.

This project features a full-stack implementation with a Flask backend that serves a structured JSON API, a simple and responsive web interface, and a SQLite database to save generated plans.



---
## Features

* **AI-Powered Planning**: Leverages the Gemini Pro model to generate logical and comprehensive task breakdowns from a single goal.
* **Database Persistence**: Automatically saves every generated plan to a SQLite database (`plans.db`) for future reference.
* **Interactive Web Interface**: A clean frontend built with HTML, CSS, and JavaScript that displays generated tasks instantly without a page refresh.
* **Local Development Mode**: Test the full application flow without using the AI model to save on API quota consumption.
* **Structured JSON API**: A robust backend API that provides plans in a clean, predictable JSON format.

---
## 🛠️ Technical Stack

* **Backend**: Python, Flask
* **Database**: SQLite
* **AI Model**: Google Gemini Pro
* **Frontend**: HTML5, CSS3, Vanilla JavaScript
* **Deployment**: Production-ready with Gunicorn or Waitress

---
## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* Python 3.8+
* `pip` (Python package installer)
* A Google AI API Key

### Installation & Setup

1.  **Clone the repository:**
    ```powershell
    git clone [https://github.com/kavyavannur14/Smartest_Task_Planner.git](https://github.com/kavyavannur14/smart-task-planner.git)
    cd smart-task-planner
    ```

2.  ** Create and activate a virtual environment:**
    ```powershell
    # Create the environment
    python -m venv venv
    
    # Activate on Windows (PowerShell)
    venv\Scripts\Activate.ps1
    
    # Activate on Windows (Command Prompt)
    venv\Scripts\activate.bat
    
    # Activate on macOS/Linux
    source venv/bin/activate
    ```

3.  **Install the required dependencies:**
    ```powershell
    pip install -r requirements.txt
    ```

4.  **Configure your API Key:**
    Create a file named `.env` in the root of the project directory and add your Google API key to it.

    ```
    # .env
    GOOGLE_API_KEY="your_real_api_key_here"
    ```

5.  **Run the application:**
    ```powershell
    python app.py
    ```
    The application will be available at `http://127.0.0.1:5000`.

---
## 💻 Development & Testing

### Local Mode (No AI)

To run the app without consuming your API quota, you can set the `DISABLE_AI` environment variable. The server will return a dummy plan, allowing you to test the full UI and database functionality.

```powershell
# On Windows (PowerShell)
$env:DISABLE_AI = '1'
python app.py

# On macOS/Linux
DISABLE_AI=1 python app.py


