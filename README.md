
### Web scraper Implementation with OpenAI

This Web scraper application is designed to scrape selected websites and collect topics. It uses AI to analyze and predict the categorization of the collected topics. The analysis and scraped data are stored in an SQLite database. Additionally, the application provides an API that can be used to extract data for frontend applications and other purposes. This app is primarily designed to run locally and operates via the command line.

Potential use cases include detecting ongoing discussions and identifying emerging trends. With minimal to no refactoring, you can also filter results to track specific topics or keywords, such as 'X' or 'Y', to see if they are being mentioned.

## Technologies
- C# (.NET 9.0)
- Web scraping (HTML Agility Pack)
- SQLite database
- OpenAI
- APIs
- Github Actions

## Installation

1. Clone the repository:
```bash
   git clone https://github.com/jannepaakkari/Web-scraper.git
   cd OpenAI-WebScraper
```

2. Set up settings
- Set up .env file and add OPENAI_API_KEY='your_key'
- Modify appsettings.json:
```bash
    "Url": Set url you want to scrape,
    "RunAPI": Set true you want to run APIs, not neccessary for scraper itself,
    "ScrapingNodes": Nodes you want to scrape, depends on site what you should add here, by default we scrape headers,
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
2. You can also use API: /api/content to view the content. Make sure RunAPI is set true at appsettings.json.

## Screenshots
![Small example of scraped content](screenshots/webscraper0.png)