# What is serverless?

Serverless is a cloud computing application development and execution model that enables developers to build and run application code without provisioning or managing servers or backend infrastructure.

Serverless lets developers put all their focus into writing the best front-end application code and business logic they can. All developers need to do is write their application code and deploy it to containers managed by a cloud service provider. The cloud provider handles the rest, provisioning the cloud infrastructure required to run the code and scaling the infrastructure up and down on demand as needed.

# Serverless does not mean 'no servers'

The name notwithstanding, there are most definitely servers in serverless computing. 'Serverless' describes the developer’s experience with those servers—they are are invisible to the developer, who doesn't see them, manage them, or interact with them in any way.

# FaaS
 FasS is the compute model central to serverless, and the two terms are often used interchangeably. But serverless is much more than FaaS. Serverless is an entire stack of services that can respond to specific events or requests, and scale to zero when no longer in use—and for which provisioning, management and billing are handled by the cloud provider and invisible to developers. In addition to FaaS, these services include:

Serverless databases and storage: Databases (SQL and NoSQL) and storage (particularly object storage) are the foundation of the data layer. A serverless approach to these technologies involves transitioning away from provisioning “instances” with defined capacity, connection and query limits, and moving toward models that scale linearly with demand in both infrastructure and pricing.

Event streaming and messaging: Serverless architectures are well-suited for event-driven and stream-processing workloads most notably the open source Apache Kafka event streaming platform.

# API gateways: 
API gateways act as proxies to web actions and provide HTTP method routing, client ID and secrets, rate limits, CORS, viewing API usage, viewing response logs, and API sharing policies.

Because serverless, platform as a service (PaaS), containers, and virtual machines (VMs) all play a critical role in the cloud application development and compute ecosystem, it’s useful to compare how serverless compares to the others across some key attributes.

Provisioning time: Measured in milliseconds for serverless, vs. minutes to hours for the other models.

Administrative burden: None for serverless, compared to a continuum from light to medium to heavy for PaaS, containers and VMs respectively.

Maintenance: Serverless architectures are managed 100% by the provider. The same is true for PaaS, but containers and VMs require significant maintenance including updating/managing operating systems, container images, connections, etc.

Scaling: Auto-scaling—including auto-scaling to zero—is instant and inherent for serverless. The other models offer automatic but slow scaling that requires careful tuning of auto-scaling rules, and no scaling to zero.

Capacity planning: None needed for serverless. The other models require a mix of some automatic scalability and some capacity planning.

Statelessness: Inherent for serverless, which means scalability is never a problem; state is maintained in an external service or resource. PaaS, containers and VMs can leverage HTTP, keep an open socket or connection for long periods of time, and store state in memory between calls.

High availability (HA) and disaster recovery (DR): Both are inherent in serverless with no extra effort and at no additional cost. The other models require additional cost and management effort. In the case of both VMs and containers, infrastructure can be restarted automatically.

Resource utilization: Serverless is 100% efficient because there are no such things thing as idle capacity—it is invoked only upon request. All other models feature at least some degree of idle capacity.

Billing granularity and savings: Serverless is metered in units of 100 milliseconds. PaaS, containers and VMs are typically metered by the hour or the minute.

# Pros and cons of serverless
# Pros

Given all of the preceding, it should be no surprise that serverless computing offers a number of technical and business benefits to individual developers and enterprise development teams.

Improved developer productivity: As noted above, serverless enables development teams to focus on writing code, not managing infrastructure. It gives developers much more time to innovate and optimize their front-end application functionality and business logic.

Pay for execution only: The meter starts when the request is made, and ends when execution finishes. Compare this to the infrastructure as a service (IaaS) compute model, where customers pay for the physical servers, virtual machines (VMs) and other resources required to run applications, from the time they provision those resources until the time they explicitly decommission them.

Develop in any language: Serverless is a polyglot environment, enabling developers to code in any language or framework—Java, Python, JavaScript, node.js—with which they're comfortable.

Streamlined development/DevOps cycles. Serverless simplifies deployment and, in a larger sense, simplifies DevOps because developers don't spend time defining infrastructure required to integrate, test, deliver and deploy code builds into production.

Cost-effective performance. For certain workloads—embarrassingly parallel processing, stream processing, certain data processing tasks—serverless computing can be both faster and more cost-effective than other forms of compute.

Usage visibility. Serverless platforms provide near-total visibility into system and user times and can aggregate usage information systematically.

# Cons

With so much to like about serverless, organizations are using it for a wide variety of applications (see Figure 2 below). But there are drawbacks—some of which are related to specific applications, and others which are universal.

Unacceptable latency for certain applications: Because serverless architectures forgo ongoing processes in favor of scaling up and down to zero, they also sometimes need to start up from zero to serve a new request. For many applications the resultant delay would not be detrimental or even noticeable to users. But for others—say, a financial trading application—this cold-start latency might be unacceptable.

Higher costs for stable or predictable workloads: Because serverless scales up and down on demand in response to workload, it offers significant cost savings for spiky workloads. But it does not offer the same savings for workloads characterized by predictable, steady or long-running processes; in these cases, a traditional server environment might be simpler and more cost-effective.

Monitoring and debugging issues: These operational tasks are challenging in any distributed system, but serverless architecture (or microservices architecture, or a combination of the two) only exacerbates the complexity. For example, teams may find it difficult or impossible to monitor or debug serverless functions using existing tools or processes.

Vendor lock-in: As noted, one of the biggest advantages of serverless is that the cloud provider manages all the computing resources. While this frees up considerable time for developers to focus on writing and improving their code, it also means that migrating code to a new cloud provider could prove challenging. Many cloud provider’s serverless platforms are designed to provide an ecosystem of managed cloud services and are not portable like virtual machines (VMs) or Docker containers. Application code that triggers several services offered by one cloud provider’s serverless platform might have to be partially or completely rewritten to get get the same results in another provider’s platform.

# Common applications for serverless
In a recent IBM survey, IT professionals reported using serverless across a wide range of applications, including customer relationship management (CRM), analytics and business intelligence, finance and more:

