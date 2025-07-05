# College Inquiry Chatbot System

A Python-based intelligent chatbot system designed to provide information about college courses, admission requirements, facilities, and other college-related queries. Built with TensorFlow, NLTK, and natural language processing techniques.

## Features

- **Intelligent Conversation**: Uses machine learning to understand and respond to user queries
- **College Information**: Provides detailed information about:
  - Available courses (BIT and BBA)
  - Course duration and semesters
  - Admission requirements
  - Fee structure
  - College facilities and location
  - Teaching methodology
  - Extra-curricular activities
- **Natural Language Processing**: Understands various ways users might ask the same question
- **Interactive Interface**: Simple command-line interface for easy interaction

---

## Quick Start

### Prerequisites

Before running the chatbot, make sure you have the following installed:

- **Python 3.7 or higher**
- **pip** (Python package installer)

### Installation

1. **Clone or download this project** to your local machine

2. **Install required dependencies** by running:
   ```bash
   pip install tensorflow nltk numpy
   ```

3. **Download NLTK data** (required for text processing):
   ```python
   python -c "import nltk; nltk.download('punkt'); nltk.download('wordnet'); nltk.download('omw-1.4')"
   ```

### Running the Chatbot

1. **Navigate to the Scripts directory**:
   ```bash
   cd Scripts
   ```

2. **Run the main chatbot**:
   ```bash
   python main.py
   ```

3. **Start chatting!** The chatbot will greet you and you can ask questions about the college.

### Example Conversations

```
| You: hello
| Bot: Hello!

| You: what courses are available
| Bot: Informatics College Pokhara has been in direct partnership with London Metropolitan University...

| You: what is the fee structure
| Bot: Course BIT
Admission fee=RS 96,000...

| You: bye
| Bot: Sad to see you go :(
|===================== The Program End here! =====================|
```

## Training Your Own Model

If you want to modify the chatbot's responses or add new capabilities:

1. **Edit the training data** in `JSONFiles/intents.json`
2. **Run the training script**:
   ```bash
   cd Scripts
   python TrainingSetup.py
   ```
3. **The new model will be saved** in `Model/chatbotmodel.h5`

### Training Data Format

The `intents.json` file contains patterns and responses in this format:
```json
{
  "tag": "intent_name",
  "patterns": ["user input 1", "user input 2"],
  "responses": ["bot response 1", "bot response 2"]
}
```

## How It Works

1. **Text Processing**: User input is tokenized and lemmatized using NLTK
2. **Feature Extraction**: Text is converted to a bag-of-words representation
3. **Intent Classification**: A neural network predicts the user's intent
4. **Response Generation**: A random response is selected from the matching intent

## System Requirements

- **Operating System**: Windows, macOS, or Linux
- **Python Version**: 3.7 or higher
- **Memory**: At least 2GB RAM
- **Storage**: 100MB free space

## Troubleshooting

### Common Issues

1. **ModuleNotFoundError**: Make sure all dependencies are installed
   ```bash
   pip install tensorflow nltk numpy
   ```

2. **NLTK Data Error**: Download required NLTK data
   ```python
   python -c "import nltk; nltk.download('punkt'); nltk.download('wordnet'); nltk.download('omw-1.4')"
   ```

3. **Model Loading Error**: Ensure you're running from the correct directory (Scripts/)

4. **File Path Issues**: Make sure all files are in their correct directories as shown in the project structure

## Customization

### Adding New Intents

1. Open `JSONFiles/intents.json`
2. Add a new intent object with patterns and responses
3. Run `TrainingSetup.py` to retrain the model

### Modifying Responses

1. Edit the responses in `JSONFiles/intents.json`
2. Retrain the model using `TrainingSetup.py`

## Contributing

Feel free to contribute to this project by:
- Adding new intents and responses
- Improving the neural network architecture
- Enhancing the user interface
- Adding new features

##  Author

**Priyanshu Yadav**(https://github.com/priyanshuyadav48)

---

**Note**: This chatbot is specifically designed for Informatics College [Pokhar](https://icp.edu.np/) and contains information relevant to that institution. Modify the training data to adapt it for other colleges or purposes.