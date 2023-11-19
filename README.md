# GPT Content and Product Retrieval API

## Overview
This API retrieves relevant documents for a given query, utilizing vector stores and advanced embeddings. It's designed to serve different domains including nursing and baby care (Ammehjelpen), brewing products (Brewshop), and running shoes (Löplabbet).

## Features
- **Multiple Domains**: Retrieve information from various specialized domains.
- **Advanced Search Capabilities**: Leverages OpenAI embeddings for efficient and relevant document retrieval.
- **Easy Integration**: Designed for straightforward integration with existing systems.

## Getting Started

### Prerequisites
- Python 3.x
- Quart
- Other dependencies listed in `requirements.txt`

### Installation
1. Clone the repository:
   ```bash
   git clone [repository-url]
   ```
2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Start the server:
   ```
   python main.py

   ```

## Running the API
To start the server, run `python main.py`. The API will be available at `http://localhost:5003`.

## API Endpoints

### 1. Ammehjelpen Retrieve
- **Endpoint**: `/ammehjelpen_retrieve`
- **Method**: POST
- **Description**: Retrieves documents related to nursing and baby care from Ammehjelpen.

### 2. Brewshop Retrieve
- **Endpoint**: `/brewshop_retrieve`
- **Method**: POST
- **Description**: Retrieves documents related to brewing products from Brewshop.

### 3. Löplabbet Retrieve
- **Endpoint**: `/loplabbet_retrieve`
- **Method**: POST
- **Description**: Retrieves documents related to running shoes from Löplabbet.

### Additional Endpoints
- **Plugin Manifest**: `/.well-known/ai-plugin.json`
- **OpenAPI Specification**: `/openapi.yaml`

## Usage
To use the API, send a POST request to the desired endpoint with a JSON payload containing the query. For example:

```json
{
  "query": "best running shoes for marathons"
}
