# Ada Fall 2023

## 02 Handling data

### Data model

- Flat model
- Relational model
  - Data is stored in tables, containing entities and attributes
  - Use declarative language to query data (specify what you want, not how to get it) (in contrast to imperative language)
  - <b>BRUSH UP ON SQL key operations</b>: select, join, ...
  - SQL implementation: one of the best way is to just import SQL into Python programming. Pandas is a good library sharing the same design philosophy as SQL.
- Document model
  - Data is stored in a hierarchical structure
  - For example: JSON, XML...
  - Good for storing data with a lot of variation (one id can have multiple same attributes, which is not easy to implement in relational model table)
  - Query language: XQuery, jq, ...
- Network model

### Data format

- Consider converting your data to a binary format (e.g. pickle, HDF5...) for faster access and smaller size.

### Data sources and APIs

API = Application Programming Interface

- Wikipedia
  - Apply API
  - Download XML dumps, which are the raw data of Wikipedia pages
  - Work with wikidata items: can be downloaded as JSON (document) or RDF (network)
- Crawling and processing HTML
  - Requests, BeautifulSoup, Scrapy, ...
  - Schema.org: a standard for structured data on the web. Keep an eye on the microformats.
- Web APIs
  - interoperable machine-to-machine interface over the network.
  - Most common framework: REST (Representational State Transfer)
    - Request a URL from the server via HTTP
    - The server returns a response in a format (e.g. JSON, XML, HTML...)
      - via `curl` command
      - the `href` attribute could be used to navigate the API to get more information (from one page to another)


### Data wrangling

Wrangling = cleaning, transforming, and enriching raw data into desired format.

Before you start analyzing data, ask yourself:

- Do I have missing data
- Do I have corrupted data
- Parse data into a format that is easy to work with