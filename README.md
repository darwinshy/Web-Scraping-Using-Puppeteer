# Web Scraping

## using Puppeteer for Full Browser Rendering

### Working

#### In Postman, get request on http://localhost:5001/wsfunctions/us-central1/scraper

#### {'username':'facebook'}

### Target Website - Instagram

What if you want to scrape a single page JavaScript app, like Angular or React? Or maybe you want to click buttons and/or log into an account before scraping? These tasks require a fully emulated browser environment that can parse JS and handle events.

Puppeteer is a tool built on top of headless chrome, which allows you to run the Chrome browser on the server. In other words, you can fully interact with a website before extracting the data you need.
Instagram Scraper

Instagram on the web uses React, which means we won’t see any dynamic content util the page is fully loaded. Puppeteer is available in the Clould Functions runtime, allowing you to spin up a chrome browser on your server. It will render JavaScript and handle events just like the browser you’re using right now.

First, the function logs into a real instagram account. The page.type method will find the cooresponding DOM element and type characters into it. Once logged in, we navigate to a specific username and wait for the img tags to render on the screen, then scrape the src attribute from them.
