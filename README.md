# NCodebase

NCodebase is a .NET/Angular application built for scraping, parsing, and delivering structured data from a wide range of websites. Its architecture includes multiple backend services and a modular Angular frontend. The system is designed for extensible parsing logic and a flexible configuration layer that makes onboarding new data sources straightforward.

## Status:

[![[DEV] CI Pipeline](https://github.com/holzschuhkv/NCodebase/actions/workflows/dev_ci.yml/badge.svg?branch=dev-main)](https://github.com/holzschuhkv/NCodebase/actions/workflows/dev_ci.yml)<br/>
[![[DEV] Deployment](https://github.com/holzschuhkv/NCodebase/actions/workflows/dev_deploy.yml/badge.svg)](https://github.com/holzschuhkv/NCodebase/actions/workflows/dev_deploy.yml)

## Key Features

- **Multi‑Website Support**
  - Clean architecture enables seamless onboarding of new website parsers. Currently supported websites:
    - Alternate
    - Hobauer
    - Kaufland
    - Mueller
    - Otto
    - In development (ebay, amazon, bricklink, brickowl, proshop)

- **Modular Service Architecture**
  - Clear separation of concerns with dedicated services for article search, blog management, database operations, and sandbox testing

- **Background Processing**
  - The background service executes asynchronous scraping tasks in the background without blocking the main application

- **Extensible Design**
  - Interface‑driven abstractions allow rapid extension of functionality and new integrations

- **Comprehensive Data Models**
  - Structured DTOs for blog articles, website metadata, and article information across all services

- **Smart Configuration System**
  - Centralized configuration (timeout parameters, XPath constants, and flexible static & dynamic parsing rules, ...)

- **Robust Logging Framework**
  - Dedicated logging utilities ensure consistent error tracking and debugging across all services

- **AI‑Powered Data Intelligence (coming soon)**
  - An upcoming AI analysis layer will evaluate scraped data, detect patterns, and generate enriched insights beyond the raw information

## Example Data

Below is an example JSON output produced by the scraper (last updated: 13.04.2026):

```json
[
  {
    "ShopName": "Alternate",
    "Id": "75431",
    "Brand": "Lego",
    "Theme": "Star Wars",
    "Title": "LEGO 75431 Star Wars Klonsoldaten des 327. Sternenkorps Battlepack, Konstruktionsspielzeug",
    "PriceUvp": "39,99",
    "PriceReduced": "29,29",
    "PriceDiff": "10,70",
    "PriceDiffPercentage": "26,76",
    "Currency": "EUR",
    "Availability": "true",
    "Url": "https://www.alternate.de/LEGO/75431-Star-Wars-Klonsoldaten-des-327-Sternenkorps-Battlepack-Konstruktionsspielzeug/html/product/100123525",
    "ImageUrl": "https://www.alternate.de/p/160x160/5/2/LEGO_75431_Star_Wars_Klonsoldaten_des_327__Sternenkorps_Battlepack__Konstruktionsspielzeug@@100123525.jpg",
    "TimeParsed": "20:17:05",
    "DateParsed": "26.10.2025"
  }
]
```

## Status and Availability

NCodebase is currently in active development and progressing toward its first public release.

The project’s domain is already accessible at **https://www.ncodebase.com**, serving as an early technical preview. It does not yet contain production data or finalized features. Its purpose is to reserve the domain, validate the hosting pipeline, and ensure a stable foundation for future releases.
