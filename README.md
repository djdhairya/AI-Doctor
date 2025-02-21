# AI Doctor

AI Doctor is an advanced image-based medical assistant powered by Groq's AI models. It allows users to upload medical images and query AI models for insights. The system leverages Llama-3.2 models to provide responses based on image analysis and textual queries.

## Features

- Upload medical images and get AI-generated insights
- Uses Groq's Llama-3.2 models for vision-based inference
- FastAPI-based backend with a web interface
- Supports multiple AI models for better accuracy
- Error handling and logging for better debugging

## Tech Stack

- **FastAPI** for the web server
- **Python** for backend scripting
- **Jinja2** for rendering HTML templates
- **Pillow** for image processing
- **Requests** for making API calls
- **Logging** for debugging and error tracking
- **Groq API** for AI-powered analysis

## Installation

### Prerequisites

- Python 3.10+
- Virtual environment (optional but recommended)

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/djdhairya/AI-Doctor.git
   cd Ai-Doctor
   ```
2. Create a `.env` file and add your Groq API key:
   ```ini
   GROQ_API_KEY=your_api_key_here
   ```

## Running the Application

### Using FastAPI

Run the FastAPI server:

```bash
uvicorn app:app --host 0.0.0.0 --port 8000 --reload
```

Access the web interface at:

```
http://localhost:8000
```

### Using Command Line

To process an image using `main.py`, update the image path and query in the script, then run:

```bash
python main.py
```

## API Endpoints

### `GET /`

- Renders the web interface for image upload and querying.

### `POST /upload_and_query`

- Accepts an image and a text query.
- Returns AI-generated insights from Groq's models.

## Example Usage

### Upload and Query via Web UI

1. Open `http://localhost:8000`
2. Upload an image
3. Enter a query (e.g., "What does this X-ray indicate?")
4. Click submit to receive AI-generated insights

### Direct Image Processing via Python

Modify `main.py` to specify your image path and query:

```python
image_path = "path/to/your/image.png"
query = "What is shown in this image?"
```

Run:

```bash
python main.py
```

## Error Handling

- Ensures the image is valid before processing
- Logs errors for debugging
- Handles API failures with appropriate messages

## Future Enhancements

- Integration with more AI models
- Support for multiple image formats
- Enhanced UI for better user experience

## License

This project is licensed under the MIT License.

![Screenshot 2025-02-21 144755](https://github.com/user-attachments/assets/bc43aeed-4cb2-43ab-a2de-cbf623582552)
![Screenshot 2025-02-21 144812](https://github.com/user-attachments/assets/0d5e1b31-8b37-488e-97a7-a0d298c4ffbe)


