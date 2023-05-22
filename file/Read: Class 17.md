## Reading Questions

### What are the key differences between scraping static and dynamic websites?

- A dynamic website is a type of website that can update or load content after the initial HTML load. So the browser receives basic HTML with JS and then loads content using received Javascript code. Such an approach allows increasing page load speed and prevents reloading the same layout each time you'd like to open a new page.

---

### Explain at least three techniques or best practices that can be employed to avoid getting blocked while scraping websites.

- Do not follow the same crawling pattern
Humans generally will not perform repetitive tasks as they browse through a site with random actions. Web scraping bots tend to have the same crawling pattern because they are programmed that way unless specified. Sites that have intelligent anti-crawling mechanisms can easily detect spiders by finding patterns in their actions and can lead to web scraping getting blocked.

- Make requests through Proxies and rotate them as needed
Multiple requests coming from the same IP will lead you to get blocked, which is why we need to use multiple addresses. When we send requests from a proxy machine, the target website will not know where the original IP is from, making the detection harder.

- Rotate User Agents and corresponding HTTP Request Headers between requests
A user agent is a tool that tells the server which web browser is being used. If the user agent is not set, websites won’t let you view content. Every request made from a web browser contains a user-agent header and using the same user-agent consistently leads to the detection of a bot. The only way to make your User-Agent appear more real and bypass detection is to fake the user agent. Most web scrapers do not have a User Agent by default, and you need to add that yourself.

---

### What is Playwright, and how does it assist in web scraping tasks? Provide an example of a use case where Playwright would be particularly beneficial.

Playwright is an open-source automation library that enables developers to automate and control web browsers programmatically. It provides a high-level API for browser automation and can be used to perform various tasks, including web scraping. Playwright supports multiple browsers, such as Chromium, Firefox, and WebKit, allowing developers to choose the browser that best suits their needs.

---

### Describe the purpose of using Xpath in web scraping, and provide an example of an Xpath expression to select a specific HTML element from a webpage.

XPath is a powerful query language used to navigate and select elements in XML and HTML documents. In the context of web scraping, XPath allows developers to specify precise patterns or paths to locate specific elements on a webpage. XPath expressions are used to traverse the HTML structure and extract data from targeted elements.