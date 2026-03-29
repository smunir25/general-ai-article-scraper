# Article Scraper

A Python-based web scraper that fetches AI-related articles from **The Guardian** using their public API. Each article's title and body content are extracted and saved to organized text files, grouped by the date and time of the scraping session.

## Features

- Fetches articles from The Guardian's AI/Technology section via their Content API
- Extracts article titles and paragraph content using BeautifulSoup
- Automatically organizes saved articles into timestamped subdirectories
- Handles errors gracefully for individual article fetches

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Requests | HTTP API calls |
| BeautifulSoup4 | HTML parsing & content extraction |
| The Guardian API | Article data source |

## Project Structure

```
article-scraper/
├── app.py                  # Main scraper script
├── requirements.txt        # Python dependencies
├── saved_articles/         # Output directory (auto-created)
│   └── HH_MM_DD_MM_YYYY/   # Timestamped session folders
│       ├── article_0.txt
│       ├── article_1.txt
│       └── ...
└── NoteBook_Experiment/    # Jupyter notebook for exploration
```

## Getting Started

### Prerequisites

- Python 3.7+
- A Guardian API key (free at [open-platform.theguardian.com](https://open-platform.theguardian.com/access/))

### Installation

```bash
git clone https://github.com/smunir25/general-ai-article-scraper.git
cd general-ai-article-scraper
pip install -r requirements.txt
```

### Configuration

Open `app.py` and replace the API key in the URL with your own Guardian API key:

```python
url = "https://content.guardianapis.com/technology/artificialintelligenceai?&api-key=YOUR_API_KEY&type=article&page=1"
```

### Usage

```bash
python app.py
```

Articles will be saved under `Saved_Articles/<timestamp>/` in the project root.

## Output Format

Each article is saved as a `.txt` file with the following structure:

```
Title: <Article Headline>


<Paragraph 1>
<Paragraph 2>
...
```

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
