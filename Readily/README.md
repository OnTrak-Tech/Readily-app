# Readily - Web Content to Document Converter

<div align="center">
  
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)

</div>

## 📋 Overview

Readily is a web application that extracts content from public web pages and converts it into downloadable document formats (Word or PDF). It's built with Flask and uses Beautiful Soup for web scraping, making it easy to save online content for offline reading or reference.

## ✨ Features

- Extract readable content from any public web page
- Convert web content to Word (.docx) documents
- Convert web content to PDF files
- Clean, responsive user interface
- Docker support for easy deployment
- AWS EC2 deployment instructions included

## 🛠️ Technologies Used

- **Backend**: Python, Flask
- **Web Scraping**: Beautiful Soup 4, Requests
- **Document Generation**: python-docx, fpdf
- **Frontend**: HTML5, CSS3
- **Containerization**: Docker, Docker Compose
- **Deployment**: AWS EC2 (instructions provided)

## 📦 Project Structure

```
Readily/
├── app/                      # Application code
│   ├── templates/            # HTML templates
│   │   └── index.html        # Main page template
│   └── app.py                # Flask application
├── .env                      # Environment variables
├── DEPLOYMENT.md             # AWS deployment instructions
├── docker-compose.yml        # Docker Compose configuration
├── Dockerfile                # Docker configuration
├── README.md                 # This documentation
└── requirements.txt          # Python dependencies
```

## 🚀 Getting Started

### Local Development

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Readily
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the application:
   ```bash
   cd app
   python app.py
   ```

5. Open your browser and navigate to:
   ```
   http://127.0.0.1:5000
   ```

### Using Docker

1. Build and run with Docker Compose:
   ```bash
   docker-compose up --build
   ```

2. Access the application at:
   ```
   http://localhost:5000
   ```

## 🔧 How It Works

1. Enter a public web page URL in the input field
2. Select your preferred output format (Word or PDF)
3. Click "Download" to extract and convert the content
4. The application will return a downloadable document containing the web page content

## 🌐 Deployment

For detailed deployment instructions to AWS EC2, please refer to [DEPLOYMENT.md](DEPLOYMENT.md).

## 🔒 Environment Variables

The application uses the following environment variables (defined in `.env`):
- `KEY`: Sample environment variable (replace with your actual variables)

## 📝 License

© 2025 Readily | Powered by OnTraK Technologies

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 📞 Support

For support, please contact [your-email@example.com](mailto:your-email@example.com).