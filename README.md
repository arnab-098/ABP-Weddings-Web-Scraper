# ABP Weddings Web Scraper

A Python-based web scraper designed to extract matrimonial profiles from the ABP Weddings website.

## Features

* **Automated Scraping**: Fetches profile data from ABP Weddings.
* **Progress Tracking**: Displays scraping progress.
* **File I/O Support**: Reads input data, tracks visited links, and writes output/missing profiles.

## Technologies Used

* **Language**: Python 3
* **Libraries**: `requests`, `BeautifulSoup`, `tkinter`

## Project Structure

* `main.py`: Entry point of the scraper.
* `abpScraper.py`: Main scraping logic.
* `webScraper.py`: Manages HTTP requests and HTML parsing.
* `reader.py`: Loads input data, credentials, and visited links.
* `writer.py`: Saves scraped data, missing links, and visited link records.
* `progressBar.py`: Progress UI component (Tkinter).

## Setup Instructions

### 1. Prerequisites

* Python 3.x installed on your system
* Required libraries: Install via pip:

  ```bash
  pip install requests beautifulsoup4
  ```

### 2. Clone the Repository

```bash
git clone https://github.com/arnab-098/ABP-Weddings-Web-Scraper.git
cd ABP-Weddings-Web-Scraper
```

### 3. Credentials File

Create a text file (e.g., `credentials.txt`) with the following format:

```
Username: <your_username>
Password: <your_password>
```

### 4. Required Paths in Code

Open `reader.py` and `writer.py` and set the appropriate file paths:

#### In `reader.py`:

* **Credential file path** (for username/password)
* **Visited links file path**

#### In `writer.py`:

* **Visited links file path**
* **Output folder path** (where scraped data will be saved)
* **Missing links folder path** (for profiles that couldn’t be scraped)

Example of modifying file paths in `reader.py`:

```python
CREDENTIAL_FILE = "path/to/credentials.txt"
VISITED_LINKS_FILE = "path/to/visited_links.txt"
```

In `writer.py`:

```python
VISITED_LINKS_FILE = "path/to/visited_links.txt"
OUTPUT_FOLDER = "path/to/output_folder/"
MISSING_LINKS_FOLDER = "path/to/missing_links_folder/"
```

### 5. Run the Scraper

```bash
python main.py
```

## Disclaimer

This tool is intended for **educational purposes only**. Make sure you comply with ABP Weddings' terms of service and privacy policy before using this scraper.

## Contributing

Contributions are welcome! Please fork the repo and submit a pull request for improvements or fixes.

## License

*No license is currently specified for this project. Please add one to clarify use cases and rights.*

---

For more tools and projects, visit [arnab-098's GitHub profile](https://github.com/arnab-098/).
