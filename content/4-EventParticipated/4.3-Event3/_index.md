---
title: "Event 3"
date: 2026-06-06
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

# Summary Report: “FCAJ Community Day: Mini meet up”

### Event Objectives

- Delve into practical technical knowledge: Deploying Multiplayer Games with Godot & AWS WebSockets, Virtualization and Docker, building GraphRAG architecture, and applying Machine Learning for cyberattack detection.
- Orient and share real-world experience regarding the career development path from an IT Helpdesk position to System Admin and DevOps Engineer in large enterprise environments.

### Speakers

- **Tran Trung Vinh** - System Administrator at Central Retail Group
- **Viet Phat** - AI majoring at Swinburne University of Technology
- **Truong Huy Phuoc** - AWS Student
- **Nguyen Quoc Bao** - Student at Swinburne University, AWS Student
- **Le Hoang Gia Dai** - AWS Student
- **Huynh Bao** - Junior Cloud Native Developer of Endava Vietnam | Founder/Head Lab of ITea Lab

### Key Highlights

#### The Future of AI and Advice for the Youth

- **AI will raise the average**: AI will bring consistency and establish a new baseline, replacing average or below-average work performance.
- **Career Orientation**: Those who work solely for a salary without passion will easily be eliminated by AI. The advice is to find a job you are truly passionate about, continuously leverage your strengths to become excellent, and use AI as a supporting tool.
- **Perfecting the Tech Stack**: Before building complex AI agents, enterprises and engineers need to automate and integrate AI into their current software development workflow (tech stack) to ensure safety and speed.

#### Multiplayer Game Architecture on AWS

- **Protocol Selection**: WebSocket is preferred for Turn-based/Lobby/Chat games due to its real-time communication, full-duplex messaging, and guaranteed delivery, overcoming the high latency of HTTP Polling and the complexity of UDP.
- **AWS Architecture**: Connect clients (Godot) via API Gateway (managing $connect, $disconnect, $default). Logic is handled by Lambda Functions, and player state is stored in DynamoDB.
- **Challenges**: Need to properly handle "Stale connections" (ghost connections when the network drops), the cost of DynamoDB scans with a large number of players, and the stateless nature of Lambda.

#### Virtualization and Containerization (Docker)

- **Limitations of Virtual Machines (VM)**: VMs are very heavy because each virtual machine runs its own separate operating system, taking a long time to boot up and consuming significant CPU/RAM resources.
- **The Power of Containers**: Containerization packages the necessary code and libraries, sharing the Host OS via a Container Engine. This enables millisecond boot times, extremely lightweight execution, and high portability (runs in any environment).
- **Docker Layer Caching**: Docker builds images layer by layer from top to bottom. If there are no changes in the upper layers, Docker reuses the cache, saving maximum build time.

#### Upgrading AI with GraphRAG on AWS

- **Limitations of traditional RAG**: Basic RAG only retrieves information based on lexical/semantic similarity and cannot answer complex questions requiring multi-hop reasoning across multiple disjointed documents.
- **GraphRAG Solution**: Uses a Graph Database to store and deeply understand the relationships between entities.
- **Deployment on AWS**: There are 2 approaches. The Fully Managed approach uses Amazon Bedrock (automated chunking, entity extraction) and Amazon Neptune Analytics. The Custom approach allows fine-tuning the pipeline using LlamaIndex combined with Neptune.

#### Cyberattack Detection using WAF and Machine Learning (NIDS)

- **Drawbacks of WAF**: Traditional WAFs rely on predefined rule sets (Rule-based), making them easily bypassed by Zero-day attacks, hybrid attacks, or unprecedented anomalous behaviors.
- **NIDS System with ML**: Build a Machine Learning model (specifically the LightGBM algorithm for high accuracy) trained on the CICIDS2018 dataset to recognize anomalous traffic states.
- **Operation**: Traffic passes through the WAF, then logs are forwarded to Lambda for analysis by the ML model. If an anomaly is detected, the system automatically sends alerts to administrators via Security Hub, Inspector, and SNS.

#### The Journey from IT Helpdesk to Sysadmin/DevOps

- **Breaking out of the comfort zone**: Moving beyond trivial tasks (installing Windows, fixing printers, crimping network cables) requires defining a 5-year roadmap and equipping oneself with knowledge of Linux, Networking, and Virtualization to advance to System Admin.
- **Real-world battle experience**: Facing major incidents (Concurrent users crashing the database, RAID 5 hardware failures) highlights the importance of the Cloud (Auto-scaling, RDS) in solving On-premise limitations.
- **Interview Mindset**: Employers (especially at large corporations) only ask 30% technical questions; the majority focuses on Mindset and Systems Thinking (e.g., how to debug a flow from a user request to the database when an error occurs).

#### The Art of Teamwork Efficiency

- **4 Golden Rules**: 
    + Clear and shared goals
    + Right person, right place
    + Open communication and active listening
    + Personal accountability
- Proficient use of digital tools like Trello, ClickUp, Slack, Discord, and Google Workspace for task management.

### Key Takeaways

#### Design Mindset & Workflow

- **Operational Mindset**: In system administration, the ultimate rule is "Never test in production". You must always backup, maintain comprehensive documentation, and establish monitoring before incidents happen.
- **Master technology instead of chasing it**: Do not use AI to replace learning. Instead, build a solid foundation to use AI as a leverage tool for increased productivity.
- **Attitude and Preparation**: When interviewing, having hands-on personal projects helps form a troubleshooting mindset, which employers value far more than degrees.

#### Technical Architecture

- **Resource Optimization**: Understand the difference between VMs and Containers to design Microservices systems that are lightweight, flexible, and infrastructure-cost-efficient.
- **Event-driven & Serverless**: Grasp the API Gateway - Lambda - DynamoDB connection flow to process low-latency real-time applications (like Multiplayer Games).
- **Multi-layer Security**: Fortify the system not only with WAF (perimeter defense) but also with an AI-integrated NIDS (detecting anomalous internal behaviors).
- **Complex Data Processing**: Master the GraphRAG methodology to solve GenAI problems that require linking and cross-referencing between multiple diverse data sources.

### Applying to Work

- **Application packaging with Docker**: Apply Docker immediately to the local development environment to completely solve the "It works on my machine but fails on others" problem, synchronizing the team's environment.
- **Refactor Data Architecture**: Pilot Amazon Bedrock and Neptune to upgrade current internal chatbot systems from RAG to GraphRAG, helping the bot accurately answer cross-functional business processes.
- **Build a Personal Lab**: Set up basic network models, Linux servers, and CI/CD pipelines following the shared DevOps roadmap to practice end-to-end system debugging.
- **Clean Security Data**: Apply data preprocessing procedures (removing NaNs, corrupted data, balancing rare labels) before feeding system logs into anomaly analysis.

### Event Experience

Attending this event was a highly rewarding experience, giving me a comprehensive view from the Infrastructure layer, Security, and Applications (App/Game) to the latest AI trends. Key experiences included:

#### Learning from highly skilled speakers

- Listening to the macro perspective from AWS's Global AI Expert on how AI is reshaping the workforce helped me escape ambiguity and define the spirit of "Using AI as a tool to become excellent."
- Experiencing the "sweat-soaked" real-world stories of Mr. Vinh when the system crashed due to user overload or RAID 5 hard drive failure. This was far more practical than any theoretical lesson in school.

#### Hands-on technical exposure

- Directly viewing comparison tables of Machine Learning algorithms (like LightGBM) analyzing PCAP files to track down hackers.
- Gaining a deeper understanding of how Docker's Cache memory works when building Images, avoiding repetitive and unnecessary installation steps when writing Dockerfiles.

#### Networking and discussions

- The event provided an open space to connect with experts via LinkedIn and GitHub, creating opportunities to seek mentorship on my career development path.

#### Lessons learned

Working in IT isn't just about keeping your head down to write code; it's about solving business problems safely, cost-effectively, and with High Availability. Meticulousness, teamwork, and a resilient spirit are the keys to advancing from entry-level positions to core roles.

#### Some event photos

![event photo 1](/images/event0606.jpg)
![event photo 2](/images/event0606_2.jpg)

> Overall, the event not only provided technical knowledge but also helped me reshape my thinking about application design, system modernization, and cross-team collaboration.