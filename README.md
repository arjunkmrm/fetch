# Fetch MCP Server
[![smithery badge](https://smithery.ai/badge/@arjunkmrm/fetch)](https://smithery.ai/server/@arjunkmrm/fetch)

A Model Context Protocol (MCP) server for making HTTP requests and extracting data from web pages.

## Features

- **Fetch URL**: Make HTTP requests and get basic page information
- **Extract Elements**: Extract HTML elements using CSS selectors
- **Get Page Metadata**: Extract comprehensive metadata including Open Graph tags, Twitter cards, and more

## Tools

### `fetch_url`
Fetch a URL and return basic information about the page.

**Parameters:**
- `url` (string): The URL to fetch

**Returns:** Status code, headers, content type, title, and description

### `extract_elements`
Extract specific elements from a web page using CSS selectors.

**Parameters:**
- `url` (string): The URL to fetch
- `selector` (string): CSS selector (e.g., 'img', '.class', '#id')
- `attribute` (optional string): Specific attribute to extract (e.g., 'href', 'src')
- `limit` (number, default: 10): Maximum number of elements to return

**Returns:** Array of extracted elements with their attributes

### `get_page_metadata`
Extract comprehensive metadata from a web page.

**Parameters:**
- `url` (string): The URL to analyze

**Returns:** Title, description, Open Graph tags, Twitter card data, canonical URL, and more

## Configuration

- `userAgent` (string): Custom User-Agent header (default: "Fetch-MCP-Server/1.0")
- `timeout` (number): Request timeout in milliseconds (default: 10000)
- `followRedirects` (boolean): Follow HTTP redirects (default: true)

## Development

```bash
# Install dependencies
npm install

# Run in development mode
npm run dev

# Build for production
npm run build
```

## Deployment

This server is designed to be deployed on [Smithery](https://smithery.ai) as a remote MCP server.

## License

MIT

