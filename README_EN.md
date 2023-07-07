# vercel-api-proxy
[简体中文](./README.md)

This project is a Vercel reverse proxy. It's completely free and an all-purpose proxy that can handle all interfaces on the internet, including OpenAI, GitHub, Google, and more. Both HTTP and HTTPS interfaces as well as single pages can be proxied and used in poor network environments. (When accessing the proxy page directly from a browser, some JS and CSS paths may not work correctly causing access issues and minor styling problems.)
## Deploy
[![Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/souying/vercel-api-proxy)


## How to Use
1 Deployment. There are two methods for deployment: one is to directly click the button above for one-click deployment, and the other is to first fork this project and then log in [vercel](https://vercel.com/) to create new one.
![new project](img/newproject.png)

2 Bind your own domain name (not mandatory, you can also use Vercel's built-in subdomain, but the built-in domain vercel.app may not be accessible in poor network conditions in China).
![domain](img/domain.png)
When binding a domain, simply follow the instructions on Vercel to configure it. Essentially, you are setting up a subdomain on your domain and pointing its CNAME record to the Vercel server.
3 To visit the https://yourdomain.com/https/url, or https://yourdomain.com/http/url.
The mapping rule is to map /https/url to the https interface, and /http/url to the http interface.


demo1: visit https://yourdomain.com/https/api.openai.com/v1/chat/completions
Actually will be replaced with https://api.openai.com/v1/chat/completions

demo2: visit https://yourdomain.com/https/raw.githubusercontent.com/souying/serverMmon
Actually will be replaced with https://raw.githubusercontent.com/souying/serverMmon
![demo2](img/demo2.png)
The mapping rule is to map /https/url to the https interface, and /http/url to the http interface.

demo3: visit https://yourdomain.com/https/www.google.com/search?q=vercel-api-proxy
Actually will be replaced with https://www.google.com/search?q=vercel-api-proxy
![demo3](img/demo3.png)
Reverse proxy Google search results page.


