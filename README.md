# Mcmaster-Carr Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Mcmaster-Carr Scraper](https://oxylabs.io/products/scraper-api/ecommerce/mcmaster-carr?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Mcmaster-Carr website effortlessly. This brief guide showcases how Mcmaster-Carr Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Mcmaster-Carr results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Mcmaster-Carr page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.mcmaster.com/products/abrading-polishing/'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/mcmaster-carr-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html xmlns=\"http://www.w3.org/1999/xhtml\" lang=\"en\" class=\"csstransitions\"><head>\n   ... </html>",
      "created_at": "2024-02-20 12:50:55",
      "updated_at": "2024-02-20 12:51:16",
      "page": 1,
      "url": "https://www.mcmaster.com/products/abrading-polishing/",
      "job_id": "7165689274229107713",
      "status_code": 200
    }
  ]
}
```
With our Mcmaster-Carr Scraper, you can seamlessly gather public data from any Mcmaster-Carr webpage. Accumulate the necessary information about various industrial tools and products, including their specifications, availability, and pricing details. This valuable data could help optimize your purchasing decisions and keep you ahead of your business rivals. If you need any assistance, please reach out to our dedicated support team through live chat or email us at hello@oxylabs.io.