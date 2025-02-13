---
pcx_content_type: configuration
title: Browser close reasons
weight: 30
---

# Browser close reasons

A browser session may close for a variety of reasons, occasionally due to connection errors or errors in the headless browser instance. As a best practice, wrap `puppeteer.connect` or `puppeteer.launch` in a [`try/catch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch) statement. 

The reason that a browser closed can be found on the Browser Rendering Dashboard in the [logs tab](https://dash.cloudflare.com/?to=/:account/workers/browser-renderingl/logs). When Cloudflare begins charging for the Browser Rendering API, we will not charge when errors are due to underlying Browser Rendering infrastructure. 

| Reasons a session may end                            |
| ---------------------------------------------------- |
| User opens and closes browser normally.              |
| Browser is idle for 60 seconds.                      |
| Chromium instance crashes.                           |
| Error connecting with the client, server, or Worker. |
| Browser session is evicted.                          |
