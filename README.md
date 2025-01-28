# Markdown to Google Docs Converter

A Python script that converts markdown-formatted meeting notes into well-formatted Google Docs, preserving styling, hierarchy, and special formatting elements like checkboxes and mentions.

## Features

- Converts markdown headers to appropriate Google Docs styles (H1, H2, H3)
- Preserves nested bullet point hierarchy
- Converts markdown checkboxes to Google Docs checkboxes
- Highlights @mentions with distinct styling
- Maintains document structure and formatting
- Built-in error handling and logging

## Prerequisites

- Python 3.7+
- Google Cloud Project with Google Docs API enabled
- Google Cloud credentials (credentials.json)

## Dependencies

```bash
pip install google-auth-oauthlib google-auth-httplib2 google-api-python-client
```

## Setup Instructions

1. Clone this repository:

```bash
git clone https://github.com/codeizhere/markdown-to-gdoc
cd markdown-to-gdoc
```

2. Set up Google Cloud Project:

   - Go to Google Cloud Console
   - Create a new project
   - Enable the Google Docs API
   - Create credentials (OAuth 2.0 Client ID)
   - Download the credentials and save as `credentials.json` in the project directory

3. Install dependencies:

```bash
pip install -r requirements.txt
```

## Running in Google Colab

1. Upload the repository files to your Google Drive
2. Open the `markdown_to_gdoc.ipynb` notebook in Colab
3. Mount your Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

4. Navigate to the project directory:

```python
%cd /content/drive/My\ Drive/path/to/project
```

5. Run the notebook cells

## Error Handling

The script includes error handling for common issues:

- Authentication failures
- API quota limits
- Invalid markdown format
- Network connectivity issues

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request
