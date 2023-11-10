# PDF Summary Generator with Python Script

## Overview

The PDF Summary Generator is a Python-based application that leverages the capabilities of OpenAI's GPT-3.5-turbo language model to automatically generate summaries, notes, and other content from PDF documents. The application provides a RESTful API endpoint that accepts PDF files as input and returns a JSON object containing the generated summaries, notes, and additional content.

The application uses the pdfplumber library to extract text from PDF files, and the openai library to interact with the GPT-3.5-turbo API. The application is built using the Flask web framework, making it easy to deploy and use.

## Features

Extract text from PDF files and convert them to plain text format.

Generate summaries of the extracted text using GPT-3.5-turbo.

Generate notes and summaries of notes from the text.

Generate additional content such as essential information and blog posts.

Provide a RESTful API endpoint for easy integration with other applications.

## Prerequisites

To use the PDF Summary Generator, you need the following:

Python 3.6 or higher

An OpenAI API key (you can obtain one by signing up for an account on the OpenAI platform)

The following Python libraries: flask, pdfplumber, openai, glob2, and textwrap

## Installation

Clone the repository:

```
git clone https://github.com/antoine1anthony/flask-pdf-summary-api.git
```

```
cd flask-pdf-summary-api
```

Install the required Python libraries:

```
pip install -r requirements.txt
```

Copy .env.example in the project directory, name it .env and paste your OpenAI API key into it.

(Optional) Customize the GPT-3.5-turbo prompts and chatbot responses by modifying the text files in the project directory.

## Usage

To run the PDF Summary Generator application, execute the following command in the project directory:

```
python main.py
```

This will start the Flask development server, and the application will be accessible at http://localhost:8000/pdfsummary.

To use the API endpoint, send a POST request to http://localhost:8000/pdfsummary with the PDF files you want to summarize as multipart file attachments. The endpoint will return a JSON object containing the generated summaries, notes, and additional content.

You can use tools like Postman or curl to send requests to the API endpoint.

Example Request

```
curl -X POST -F "pdfs=@example.pdf" http://localhost:8000/pdfsummary
```

Example Response

```
{

  "summary": "This is the summary of the PDF document...",

  "notes": "These are the notes extracted from the document...",

  "notes_summary": "This is the summary of the notes...",

  "essential_info": "This is the essential information extracted..."

}
```

## Contributing

Contributions to the PDF Summary Generator are welcome! If you would like to contribute, please fork the repository, make your changes, and submit a pull request. If you find any issues or have suggestions for improvements, please open an issue on the GitHub repository.

## License

The PDF Summary Generator is released under the MIT License. See the LICENSE file for more details.

## Disclaimer

This application uses the GPT-3 language model provided by OpenAI. The quality of the generated content may vary, and users are advised to review the output before using it for any critical purposes. The application is provided "as is" without any warranties or guarantees. Users are responsible for any consequences resulting from the use of this application and its generated content.
