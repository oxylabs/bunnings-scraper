# Bunnings Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Bunnings Scraper](https://oxylabs.io/products/scraper-api/ecommerce/bunnings?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Bunnings website effortlessly. This brief guide showcases how Bunnings Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Bunnings results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Bunnings page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.bunnings.com.au/products/tools'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/bunnings-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html data-theme=\"retail\" lang=\"en\"><head><meta charSet=\"utf-8\"/><meta content=\"initi ... </html>",
      "created_at": "2024-02-20 12:16:19",
      "updated_at": "2024-02-20 12:16:24",
      "page": 1,
      "url": "https://www.bunnings.com.au/products/tools",
      "job_id": "7165680569370571777",
      "status_code": 200
    }
  ]
}
```
Using our specialized Bunnings Scraper, you can seamlessly gather public data from your chosen Bunnings web pages. This allows you to acquire important product details, like cost, user feedback, and product specifications, in order to perform market analysis and maintain a competitive edge. For any assistance or inquiries, engage with our customer service team through live chat or send us an email at hello@oxylabs.io.
