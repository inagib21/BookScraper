# BookScraper

This project is a simple web scraper built in Go, using the Colly library. It scrapes book information from the "Books to Scrape" website, specifically the travel books category. The scraper extracts data such as the book's link, name, price, and stock availability and outputs it in JSON format.

## Features

- **Async Web Scraping:** Leverages Colly's asynchronous capabilities to scrape web pages efficiently.
- **Data Extraction:** Collects book details including the link, name, price, and stock status.
- **JSON Output:** The scraped data is formatted as a JSON array for easy consumption and further processing.

## Project Structure

- **main.go:** The main Go file containing the logic for the web scraper.

## Dependencies

- [Go 1.18+](https://golang.org/dl/): Ensure you have Go installed on your system.
- [Colly](http://go-colly.org/): A powerful and easy-to-use Go scraping library.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/inagib21/BookScraper.git
   cd BookScraper
Install the required Go packages:

```bash
Copy code
go get -u github.com/gocolly/colly
Run the scraper:
```

```bash
Copy code
go run main.go
```
How It Works
Collector Setup: A new Colly collector is created with asynchronous scraping enabled.
Category Links Extraction: The scraper identifies and visits links to different book categories.
Pagination: The scraper follows pagination links to visit all pages within the category.
Product Data Extraction: For each book, the scraper extracts the title, price, availability status, and link to the product page.
Output: The collected data is serialized into a JSON format and printed to the console.
Example Output
json
Copy code
[
 {
  "link": "catalogue/category/books/travel_2/some-book_1/index.html",
  "name": "Some Book",
  "price": "£51.77",
  "instock": "In stock"
 },
 ...
]
Notes
The initial category link is hardcoded for the "Travel" category on the "Books to Scrape" website.
Modify the Visit URL in main.go to scrape different categories or other pages.
