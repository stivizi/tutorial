# MCP Tutorials

This directory contains tutorials for using the available Model Context Protocol (MCP) servers and their tools.

## Available MCP Servers

### Time MCP

Provides tools for getting and converting timezones.

*   `get_current_time`: Gets current time in a specific timezone.
*   `convert_time`: Converts time between timezones.

### Brave Search MCP

Provides tools for searching the web with Brave Search.

*   `brave_web_search`: Performs a web search using the Brave Search API.
*   `brave_local_search`: Searches for local businesses and places using Brave's Local Search API.

### Firecrawl MCP

Provides tools for scraping and searching web pages.

*   `firecrawl_scrape`: Scrapes a single webpage with advanced options for content extraction.
*   `firecrawl_search`: Searches and retrieves content from web pages with optional scraping.

### Playwright MCP

Provides tools for automating browser actions with Playwright.

*   `playwright_navigate`: Navigates to a URL.
*   `playwright_screenshot`: Takes a screenshot of the current page or a specific element.

### YouTube MCP

Provides tools for interacting with YouTube.

*   `download_youtube_url`: Downloads YouTube subtitles from a URL.

### Google Calendar MCP

Provides tools for interacting with Google Calendar.

*   `list-calendars`: Lists all available calendars.
*   `create-event`: Creates a new calendar event.

### Google Drive MCP

Provides tools for interacting with Google Drive.

*   `search`: Searches for files in Google Drive.

### Google Maps MCP

Provides tools for interacting with Google Maps.

*   `maps_geocode`: Converts an address into geographic coordinates.
*   `maps_search_places`: Searches for places using Google Places API.

### WhatsApp MCP

Provides tools for interacting with WhatsApp.

*   `search_contacts`: Searches WhatsApp contacts by name or phone number.
*   `list_messages`: Gets WhatsApp messages matching specified criteria.
*   `send_message`: Sends a WhatsApp message to a person or group.

### Slack MCP

Provides tools for interacting with Slack.

*   `slack_post_message`: Posts a new message to a Slack channel.
*   `slack_get_channel_history`: Gets recent messages from a channel.

### GitHub MCP

Provides tools for interacting with GitHub repositories.

*   `create_issue`: Creates a new issue in a GitHub repository.
*   `get_file_contents`: Gets the contents of a file or directory from a GitHub repository.
*   `create_repository`: Creates a new GitHub repository in your account.

### 21st.dev Magic MCP

Provides tools for generating UI components and searching for logos.

*   `21st_magic_component_builder`: Generates a UI component.
*   `logo_search`: Searches and returns logos in specified format (JSX, TSX, SVG).

### Apify Actors MCP

Provides tools for discovering and using Apify Actors.

*   `search-actor`: Discovers available Actors or MCP-Servers in Apify Store using full text search.
*   `get-tool-details`: Gets documentation, readme, input schema and other details about an Actor.

### Filesystem MCP

Provides tools for interacting with the file system.

*   `read_file`: Reads the complete contents of a file from the file system.
*   `search_files`: Recursively searches for files and directories matching a pattern.
*   `write_file`: Creates a new file or completely overwrite an existing file with new content.

### Markdownify MCP

Provides tools for converting various file types to markdown.

*   `audio-to-markdown`: Converts an audio file to markdown, including transcription if possible.
*   `webpage-to-markdown`: Converts a webpage to markdown.

### Memory MCP

Provides tools for interacting with a knowledge graph.

*   `create_entities`: Creates multiple new entities in the knowledge graph.
*   `search_nodes`: Searches for nodes in the knowledge graph based on a query.

### Ollama MCP

Provides tools for running and managing Ollama models.

*   `run`: Runs a model.
*   `list`: Lists models.

### Perplexity MCP

Provides tools for searching and chatting with Perplexity AI.

*   `search`: Performs a general search query to get comprehensive information on any topic.
*   `chat_perplexity`: Maintains ongoing conversations with Perplexity AI.

### Puppeteer MCP

Provides tools for automating browser actions with Puppeteer.

*   `puppeteer_navigate`: Navigates to a URL.
*   `puppeteer_screenshot`: Takes a screenshot of the current page or a specific element.

### Qdrant MCP

Provides tools for storing and finding memories in Qdrant.

*   `qdrant-store`: Keeps the memory for later use.
*   `qdrant-find`: Looks up memories in Qdrant.

### Supabase MCP

Provides tools for interacting with Supabase projects.

*   `list_projects`: Lists all Supabase projects for the user.
*   `get_project`: Gets details for a Supabase project.
*   `create_project`: Creates a new Supabase project.

### WolframAlpha MCP

Provides tools for querying WolframAlpha.

*   `ask_llm`: Asks WolframAlpha a query and get LLM-optimized structured response with multiple formats.
*   `get_simple_answer`: Gets a simplified, LLM-friendly answer focusing on the most relevant information.
