# Woolworths Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Woolworths Scraper](https://oxylabs.io/products/scraper-api/ecommerce/woolworths?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Woolworths website effortlessly. This brief guide showcases how Woolworths Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Woolworths results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Woolworths page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.woolworths.com.au/shop/browse/specials/online-only-specials?icmpid=sm-prnav-sc-onlineonlyspecials'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/woolworths-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-AU\"><head>\n    <title>Woolworths Supermarket - Buy Groceries Online</t ... </html>",
      "created_at": "2024-02-20 12:39:25",
      "updated_at": "2024-02-20 12:39:29",
      "page": 1,
      "url": "https://www.woolworths.com.au/shop/browse/specials/online-only-specials?icmpid=sm-prnav-sc-onlineonlyspecials",
      "job_id": "7165686383367949313",
      "status_code": 200
    }
  ]
}
```
With our Woolworths Scraper, you can seamlessly pull public data from any Woolworths web page. Gather essential product details, including cost, customer feedback, or product summaries, to evaluate your market standing and stay one step ahead of your business rivals. If you need any assistance, feel free to reach out to our friendly support team via live chat or drop us an email at hello@oxylabs.io.