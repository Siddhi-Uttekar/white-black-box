# exp21

change gitignore -> .gitignore

npm run install-deps 

npm run start

##########
❓ Possible Question	✅ Ideal Answer
What is white-box monitoring?	It monitors internal app behavior like request latency, memory usage, errors, using internal metrics exposed by the code.
What is black-box monitoring?	It checks app availability from an external user perspective—if the site is up and responding properly.
What metrics are you collecting in white-box?	Request duration, method, route, status code.
What metrics are you collecting in black-box?	Whether the endpoint responded (success/failure), and how long it took.
How is /unstable route useful?	It randomly simulates failure (500 errors), useful for testing error tracking.
Why do we need /slow route?	It adds random delays to simulate latency, useful to test performance monitoring.
How do you expose metrics?	Using /metrics endpoints via prom-client. White-box on port 3000, black-box on 3001.
What is prom-client?	A Prometheus client for Node.js that helps define and expose application metrics.
Can Prometheus scrape these metrics?	Yes. You can configure Prometheus to scrape from http://localhost:3000/metrics and http://localhost:3001/metrics.
How can this help in CI/CD pipelines?	These metrics can trigger alerts or dashboards that give visibility into build-time or runtime performance and errors.

#########
Tool	Purpose
Node.js + Express	Web application framework
prom-client	Prometheus client for collecting and exposing metrics
axios	Makes HTTP requests to simulate external users (black-box)
Prometheus (optional but implied)	Collects metrics from /metrics endpoints
Grafana (optional)	Can visualize metrics for better monitoring
