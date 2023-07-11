# Amazon Scraper API

This is a RESTful API built with Node.js and Express.js that allows you to scrape data from Amazon. It utilizes the **Scraper API** service to retrieve information such as product details, reviews, offers, and search results from the Amazon website. 

## Prerequisites

Before you can use this API, you will need the following:

- Node.js installed on your machine
- An API key from Scraper API. You can sign up for an account and obtain your API key at [Scraper API](https://www.scraperapi.com/)

## Installation

1. Clone or download this repository to your local machine.
2. Open a terminal or command prompt and navigate to the project directory.
3. Run the following command to install the required dependencies:

   ```shell
   npm install
   ```

## Usage

1. Replace `<YOUR_API_KEY>` in the code with your actual Scraper API key.

2. Start the server by running the following command:

   ```shell
   node app.js
   ```

3. The server will start running on the specified port (default is 5000). You should see the message "Server running on port \<PORT\>" in the console.

4. You can now send HTTP requests to the API endpoints listed below.

## API Endpoints

### Get Product Details

- **URL:** `/products/:productId`
- **Method:** GET
- **Description:** Retrieves the details of a specific product on Amazon.
- **Parameters:**
  - `productId` (required): The unique identifier of the product.
- **Example:** `GET /products/B01N5TVQJY`

### Get Product Reviews

- **URL:** `/products/:productId/reviews`
- **Method:** GET
- **Description:** Retrieves the reviews of a specific product on Amazon.
- **Parameters:**
  - `productId` (required): The unique identifier of the product.
- **Example:** `GET /products/B01N5TVQJY/reviews`

### Get Product Offers

- **URL:** `/products/:productId/offers`
- **Method:** GET
- **Description:** Retrieves the offers (prices) for a specific product on Amazon.
- **Parameters:**
  - `productId` (required): The unique identifier of the product.
- **Example:** `GET /products/B01N5TVQJY/offers`

### Get Search Results

- **URL:** `/search/:searchQuery`
- **Method:** GET
- **Description:** Retrieves the search results for a specific query on Amazon.
- **Parameters:**
  - `searchQuery` (required): The search query.
- **Example:** `GET /search/laptop`

## Response

The API will return a JSON response containing the scraped data from Amazon. In case of any errors, an error object will be returned with details of the error.

## License

This project is licensed under the [MIT License](LICENSE).

## Note

This API is for educational and personal use only. Please make sure to comply with Amazon's terms of service and usage policies when utilizing this API.
