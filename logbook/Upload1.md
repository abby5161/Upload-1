# Web Request Flow 

When we type a URL in a browser, like `https://usiu.ac.ke`, we are basically telling the browser where to find the website and what resource we want. A URL has different parts: the protocol (`https`), the domain name (`usiu.ac.ke`), and optionally a path (`/page1`). The protocol tells the browser how to talk to the server, the domain name tells it which server, and the path points to the exact resource.

Before the browser can connect to the server, it needs to know the server’s IP address. This is where DNS, or Domain Name System, comes in. The browser asks a DNS server to translate the human-friendly domain into an IP address. Once the IP is known, the browser can start talking to the server.

The connection itself uses TCP, which stands for Transmission Control Protocol. TCP makes sure that data is sent and received reliably, in the correct order, and without errors. For HTTPS sites, TLS (Transport Layer Security) is used on top of TCP to encrypt the communication. This prevents attackers from reading sensitive data like passwords or credit card numbers while it travels over the internet.

Once the connection is ready, the browser sends an HTTP request to the server. This request might ask for the main page, images, stylesheets, or scripts. The server processes the request and sends back an HTTP response with the requested data. Each resource may trigger additional sub-requests until the whole page is loaded.

Caching helps speed things up. When a browser or proxy has previously downloaded a resource, it can reuse it instead of downloading it again. This saves time and reduces the load on the server, making websites faster for users.

So basically, loading a web page is a step-by-step process: typing the URL, resolving it with DNS, establishing a TCP/TLS connection, sending HTTP requests, receiving responses, and finally rendering everything. Caching makes this process even smoother. Understanding this flow helps us see how websites work under the hood and why secure, reliable connections are important.
