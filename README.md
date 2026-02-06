# UNWATCH

**Your videos, in words.**

Convert YouTube videos and podcasts into clean, readable transcripts with AI-generated chapters and takeaways.

## Features

- Extracts transcripts from YouTube videos
- Cleans up auto-generated captions using Gemini AI
- Adds chapter headers based on content themes
- Generates top 5 takeaways
- Export as Markdown (.md) or PDF
- Font selection and zoom controls
- Best for videos up to ~1 hour

## Quick Start

1. **Clone the repo**
   ```bash
   git clone https://github.com/iamprakharsingh/unwatch.git
   cd unwatch
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Get a Google AI API key**
   - Go to [Google AI Studio](https://aistudio.google.com/apikey)
   - Create an API key

4. **Create a `.env` file**
   ```bash
   echo "GOOGLE_API_KEY=your_api_key_here" > .env
   ```

5. **Run the app**
   ```bash
   python app.py
   ```

6. **Open http://127.0.0.1:8080**

## Usage

1. Paste a YouTube URL
2. Click "Transcribe"
3. Wait for processing
4. Read, customize font/zoom, and download

## Cloud Deployment

YouTube blocks requests from cloud provider IPs. For cloud deployments (Render, AWS, etc.), you need a proxy service:

1. Sign up for a proxy service like [Webshare](https://www.webshare.io/) (has free tier)
2. Get your proxy URL in format: `http://username:password@proxy-host:port`
3. Add `PROXY_URL` environment variable in your deployment settings

## Tech Stack

- Flask
- youtube-transcript-api
- Google Gemini AI
- fpdf2
- marked.js

## License

MIT

---

Made by [Prakhar](https://www.linkedin.com/in/prakharsingh96/)
