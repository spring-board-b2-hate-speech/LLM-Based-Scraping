# LLM-Based Recycling Facility Scraper

A Python script that scrapes recycling facility data from Earth911 using Playwright and structures the output with OpenAI/LangChain.

## Features

- Extracts facility data from Earth911's Recycling Center Search
- Uses LLM (GPT-4) for structured data extraction
- Outputs clean JSON with categorized materials
- Handles dynamic JavaScript content
- Implements semantic material categorization

## Prerequisites

- Python 3.8+
- OpenAI API key
- Playwright browsers

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/LLM-Based-Scraping.git
cd LLM-Based-Scraping
```
2. Install dependencies:
```bash
pip install playwright beautifulsoup4 langchain-openai python-dotenv
```
3. Install Playwright browsers:
```bash
playwright install
```
4. Create .env file with your OpenAI API key:
```bash
OPENAI_API_KEY=your_api_key_here
```
## Usage
Run the scraper:
```bash
python scraper.py
```
The script will output structured JSON data for up to 3 recycling facilities that accept electronics within 100 miles of ZIP code 10001.
## Sample Output
```bash
[
  {
    "business_name": "Green Earth Recyclers",
    "last_update_date": "2023-11-04",
    "street_address": "123 5th Ave, New York, NY 10001",
    "materials_category": ["Electronics", "Batteries"],
    "materials_accepted": [
      "Computers, Laptops, Tablets",
      "Lithium-ion Batteries"
    ]
  },
  {
    "business_name": "EcoTech Recycling",
    "last_update_date": "2023-10-15",
    "street_address": "456 Broadway, New York, NY 10003",
    "materials_category": ["Electronics"],
    "materials_accepted": [
      "Monitors, TVs (CRT & Flat Screen)",
      "Printers, Copiers, Fax Machines"
    ]
  }
]
```
