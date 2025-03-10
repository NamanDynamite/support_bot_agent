# SupportBotAgent

## Overview
SupportBotAgent is a Python-based AI-powered chatbot that answers customer queries using a document as its knowledge base. It extracts relevant information from the document and provides responses using a Natural Language Processing (NLP) model. The bot also allows users to provide feedback and refines its responses accordingly.

## Features
- **Document-Based Q&A**: Processes a `.txt` or `.pdf` document and extracts information.
- **AI-Powered Answers**: Uses `distilbert-base-uncased-distilled-squad` for question answering.
- **Semantic Search**: Finds relevant sections using `sentence-transformers`.
- **Confidence-Based Response Filtering**: Avoids low-confidence answers.
- **User Feedback Loop**: Improves responses based on user feedback.
- **Logging**: Logs all interactions for debugging and improvements.

## Technologies Used
- **Python**
- **Transformers (Hugging Face)** for question answering
- **Sentence-Transformers** for document embedding and retrieval
- **PyPDF2** for PDF text extraction
- **Logging module** for tracking bot activity

## Installation
### Clone the Repository:
```sh
git clone <repository-url>
cd customer-support-bot
```

### Prerequisites
Ensure you have Python 3.7+ installed. Then, install the required dependencies:
```sh
pip install -r requirements.txt
```

## Usage
1. **Prepare a Document**: Create a `.txt` or `.pdf` file containing the knowledge base.
2. **Run the Bot**:
   ```sh
   python support_bot_agent.py
   ```
3. **Interact with the Bot**: Enter queries when prompted.

## Example
### Sample Input:
```
How do I reset my password?
```
### Sample Output:
```
Initial Response: "To reset your password, go to the login page and click 'Forgot Password.' Enter your email and follow the link sent to you."
Was this response helpful? (yes/no/more details):
```

## Configuration
- **Log File Path**: The bot logs interactions in `support_bot_log.txt`. Modify `setup_logging()` to change the path.
- **Threshold for Relevance**: Adjust `threshold` in `find_relevant_section()` to refine the relevance filter.

## File Structure
```
customer-support-bot/
│── support_bot_agent.py  # Main bot script
│── faq.txt               # Sample document (or use a PDF)
│── support_bot_log.txt   # Log file
│── requirements.txt      # Dependencies
│── README.md             # Documentation
```

## Future Improvements
- Implement a web-based UI for interactions.
- Store user feedback for continuous learning.
- Support multiple document formats.

## License
This project is licensed under the MIT License.