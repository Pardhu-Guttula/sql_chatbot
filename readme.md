# SQL Chatbot with Google AI Integration

This project is a web-based chatbot application that allows users to interact with a MySQL database. The chatbot generates SQL queries based on user questions and provides natural language explanations of the query results using Google AI (`gemini-pro` model). The frontend of the application is built using **Streamlit**.

## Features

- **Interactive Chatbot**: Ask questions about your MySQL database, and the bot will generate SQL queries to answer them.
- **Google AI Integration**: Natural language responses are generated using Google AI (`gemini-pro`).
- **Database Connection**: Easily connect to any MySQL database by providing the necessary credentials in the app.
- **Chat History**: The bot maintains a conversation history to provide context for SQL queries.

## Getting Started

### Prerequisites

Before running the application, make sure you have the following installed:

- Python 3.7+
- MySQL database
- Google Cloud API Key for `gemini-pro` model

### Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Pardhu-Guttula/sql_chatbot.git
    cd sql_chatbot
    ```

2. **Create a virtual environment**:
    ```bash
    python3 -m venv myenv
    source myenv/bin/activate   # For Linux/macOS
    # or
    myenv\Scripts\activate      # For Windows
    ```

3. **Install the required dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up environment variables**:
   Create a `.env` file in the project root and add your Google API key:
    ```bash
    touch .env
    ```

   Add the following to your `.env` file:
    ```bash
    GOOGLE_API_KEY=your-google-api-key
    ```

5. **Run the application**:
    ```bash
    streamlit run app.py
    ```

### Configuration

In the sidebar of the web app, provide the MySQL database credentials to connect to your database:
- Host
- Port
- User
- Password
- Database

Click **Connect** to establish a connection to the database.

### Example Chat

You can ask the chatbot questions like:
- "List the names of all artists."
- "How many albums are there in the database?"
- "Which tracks have the longest duration?"

The chatbot will generate the corresponding SQL queries, execute them on the connected MySQL database, and return both the SQL result and a natural language response.

## Project Structure

```plaintext
.
├── app.py               # Main application code
├── requirements.txt     # List of dependencies
├── .env                 # Environment variables (Google API key)
├── README.md            # This README file
└── __mock__             # Mock files for testing (if applicable)
