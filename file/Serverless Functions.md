## Reading Questions

### What are the key characteristics of serverless computing, and how does it differ from traditional server-based architectures?

Function-as-a-service, or FaaS, is a cloud computing service that enables developers to run code or containers in response to specific events or requests, without specifying or managing the infrastructure required to run to code.

- Provisioning time: Measured in milliseconds for serverless, vs. minutes to hours for the other models.
- Administrative burden: None for serverless, compared to a continuum from light to medium to heavy for PaaS, containers and VMs respectively.
- Maintenance: Serverless architectures are managed 100% by the provider. The same is true for PaaS, but containers and VMs require significant maintenance including updating/managing operating systems, container images, connections, etc.
- Scaling: Auto-scaling—including auto-scaling to zero—is instant and inherent for serverless. The other models offer automatic but slow scaling that requires careful tuning of auto-scaling rules, and no scaling to zero.
- Capacity planning: None needed for serverless. The other models require a mix of some automatic scalability and some capacity planning.
- Statelessness: Inherent for serverless, which means scalability is never a problem; state is maintained in an external service or resource. PaaS, containers and VMs can leverage HTTP, keep an open socket or connection for long periods of time, and store state in memory between calls.
- High availability (HA) and disaster recovery (DR): Both are inherent in serverless with no extra effort and at no additional cost. The other models require additional cost and management effort. In the case of both VMs and containers, infrastructure can be restarted automatically.
- Resource utilization: Serverless is 100% efficient because there are no such things thing as idle capacity—it is invoked only upon request. All other models feature at least some degree of idle capacity.
- Billing granularity and savings: Serverless is metered in units of 100 milliseconds. PaaS, containers and VMs are typically metered by the hour or the minute.

---

### How can one get started with Vercel, and what are the main steps involved in deploying a serverless function using Vercel?

1. Create a Vercel Account
2. Install the Vercel CLI.
3. Initialize Your Project
4. Configure Project Settings
5. Write Your Serverless Function
6. Deploy Your Function
7. Configure Environment Variables
8. Test Your Deployment
9. Monitor and Manage Deployments

---

### What are APIs, and how can they be utilized in Python applications to access and manipulate data from external sources?

An API, or application programming interface, is a set of defined rules that enable different applications to communicate with each other. It acts as an intermediary layer that processes data transfers between systems, letting companies open their application data and functionality to external third-party developers, business partners, and internal departments within their companies.

1. API Documentation
2. HTTP Requests
3. Authentication
4. Making API Requests
5. Processing API Responses
6. Data Manipulation
7. Error Handling
8. Integration and Application Logic

---

### What is the Requests library in Python, and how can it be used to interact with APIs by sending HTTP requests? Can you provide an example of a basic GET request using the Requests library?

All interactions between a client—in this case your Python console—and an API are split into a request and a response:

- Requests contain relevant data regarding your API request call, such as the base URL, the endpoint, the method used, the headers, and so on.
- Responses contain relevant data returned by the server, including the data or content, the status code, and the headers.
Using TheDogAPI again, you can drill down a bit more into what exactly is inside the Request and Response objects:

>>> response = requests.get("https://api.thedogapi.com/v1/breeds")
>>> response
<Response [200]>
>>> response.status_code
200
>>> response.reason
'OK'