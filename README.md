
### WebScraper Implementation with OpenAI

This WebScraper application is designed to scrape selected websites and collect topics. It uses AI to analyze and predict the categorization of the collected topics. The analysis and scraped data are stored in an SQLite database. Additionally, the application provides an API that can be used to extract data for frontend applications and other purposes. This app is primarily designed to run locally and operates via the command line.

## Technologies
- C# (.NET)
- Github Actions
- SQLite database
- OpenAI
- APIs
- Web Scraping

## Prerequisites

- .NET 9.0 SDK
- SQLite

## Installation

1. Clone the repository:
```bash
   git clone https://github.com/jannepaakkari/Web-scraper.git
   cd WebScraper
```

2. Set up settings
- Set up .env file and add OPENAI_API_KEY='your_key'
- Modify appsettings.json:
```bash
    "Url": Set url you want to scrape,
    "RunAPI": Set true you want to run APIs, not neccessary for scraper itself,
    "ScrapingNodes": Nodes you want to scape, depends on site what you should add here, by default we scape headers,
```

3. Restore dependencies:
```bash
dotnet restore
```

4. Build the project:
```bash
dotnet build
```

5. Run the application:
```bash
dotnet run
```

6. To apply the latest database migrations, use the following command:
```bash
dotnet ef database update
```

## Usage

1. After you have run application (dotnet run) successfully you can view content from HeadersDatabase.db (should be created automatically).
2. You can also use API: /api/content to view the content.

## Screenshots
![Small example of scraped content](screenshots/webscraper0.png)