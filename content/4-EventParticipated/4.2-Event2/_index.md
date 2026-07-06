---
title: "Event 2"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Summary Report: “FCAJ Community Day: Conference Call”

### Event Objectives

- A place for the community to connect, network, proactively initiate conversations, and inspire one another (including the members at the 36th-floor area).
- Update on the IT job market in the AI era and the new core skills (business knowledge, real-world products) that software engineers need to equip themselves with.
- Dive deep into practical sharing sessions ranging from technical to business aspects, specifically focusing on how to design and integrate AI systems (Multi-Agent) into enterprise environments securely and reliably.

### Speakers

- **Truong Tinh** - Platform Engineer of GoTymeX
- **Pham Nguyen Hai Anh** - AWS Community Builder | Cloud Consultant
- **Nguyen Tuan Thinh** - DevOps/Cloud Engineer FCAJ
- **Le Pham Ngoc Uyen, Nguyen Ngoc Quynh Mai, Nguyen Phuong Thao** - Building UTMorpho from Idea to Reality, 36 hrs with LotusHacks team
- **Dao Minh Duc** - Solutions Architect
- **Lam Hoang Cat Vy** - Sr Business Systems Analyst | Applied AI Initiatives Team Lead | IT Young Talents Program Manager of VPBank | AWS AI Engineering Community Builder

### Key Highlights
#### Business Mindset in AI Development

- **User-centric products**: When designing an AI solution, you must not only focus on the technology but also answer 4 core questions: Who uses it? What do they use? Why use it? When is the right time to deploy that solution?
- **Market research and ROI**: You cannot propose an expensive AI system (e.g., 1 billion VND) without proving the market need and feasibility. Every solution must be evaluated based on the Return on Investment (ROI) and the benefits it brings (saving billions of VND rather than making unrealistic claims of millions of dollars).
- **Understanding Stakeholder KPIs**: In an enterprise environment, engineers need to understand the KPIs and workflows of other departments (like Security, Business) to communicate easily, request permissions, and coordinate system deployment.

#### Building a Multi-Agent System for Startup Credit Scoring

- **Limitations of a Single Agent**: For complex problems requiring multi-dimensional input data (financial reports, market data, startup founder team), a Single Agent will face Context Window limits, lack deep expertise, and easily get overloaded.
- **Multi-Agent Architecture**: The system is designed as a "Credit Committee" including: Manager (Orchestrator to divide tasks), Financial Analyst (analyzes financial reports), Research (evaluates market share, competitors), Evaluator (evaluates Founders), and Risk Accessor (assesses risks).
- **Knowledge Transfer**: Providing context to AI is not simply dumping hundreds of PDF pages into it, but Context Engineering—extracting the business "essence" from experts to guide the model to process data accurately.

#### Security, Compliance, and Responsibility in Enterprises

- **Risk control from MCP and Prompt Injection**: In the financial sector, security is the top priority. Plugging in tools (MCP) must be carefully reviewed to prevent data leakage. The system requires Output/Input filtering layers to prevent Prompt Injection.
- **API Key Management (API Key Rotation)**: It is mandatory to frequently rotate the API Key and Access Key of IAM to avoid cost leakages (e.g., keys being stolen to call large models, consuming massive funds).
- **Audit Trail and Responsibility**: Any decision made by AI (like approving a loan of 10 billion or 100 billion) must be logged and reviewed by a human. The person approving the system is the one legally responsible, not the AI platform.

#### Communication Techniques and AI Uncertainty

- **Avoid the "Internet Builder" mindset**: Avoid pulling every piece of code or rule from the internet to use without understanding them. You need to input the specific context (Objectives, Audience, Format) of the company into the prompt.
- **LLMs are always probabilistic**: Even if Temperature = 0, the results can still vary due to how GPUs calculate or how providers optimize costs (Inference optimization - batching multiple prompts). Flexible testing and downstream systems are needed to handle non-standard output formats.

#### Cloud Infrastructure and Hackathon Experience

- **Amazon CloudFront**: Provides a flat-rate pricing mechanism to help enterprises stop the fear of bill spikes when facing DDoS attacks, combined with security layers like VPC Origin and MTLS.
- **Hackathon Experience**: When building an AI app that generates UI in 36 hours, the biggest lesson is to focus on core features (direct editing on UI) instead of "over-thinking" and building too many features. Be wary of token limits and AI "Over-generation" (generating redundant code).

### Key Takeaways

#### Design Mindset & Workflow

- **Foundational technical knowledge is mandatory**: AI is just a supporting tool. To deploy a product to production in an enterprise, core knowledge of Software Engineering (Backend, databases, JWT, encryption) is the decisive factor.
- **Serving end-users**: The system building mindset shouldn't stop at "getting the demo to run," but must ensure the system operates **securely** and **reliably**.

#### Technical Architecture & Security

- Master the design of **Multi-Agent** systems, clearly dividing expertise for each agent so they can **challenge assumptions** and process tasks in parallel.
- Understand the importance of **IaC (Infrastructure as Code)** like Terraform to deploy infrastructure consistently, manage version installations, and log changes.

### Applying to Work

- **Evaluate feasibility using ROI**: Applying the lesson from Ms. Cat Vy, any future AI system proposal needs to include a cost-benefit analysis (ROI) before presenting it to management.
- **Multi-Agent structure for complex tasks**: Transform large document reading comprehension tasks into a pipeline with multiple agents (acting as analysts, summarizers, and risk assessors) to increase accuracy.
- **Tighten Guardrails**: Establish Input filtering layers against Prompt Injection and enforce strict API Key security for personal/company projects.
- **Practice Context Engineering**: Instead of stuffing raw documents, I will learn how to extract essential domain expertise (Knowledge Transfer) to create standard contexts for LLMs.

### Event Experience

#### Learning from highly skilled speakers

- Ms. Cat Vy's sharing session truly opened my mind about **"Enterprise-grade AI"**. I realized the massive gap between doing a personal AI project at home and integrating it into a banking system, especially regarding **Compliance** and data security.
- The strictness in granting tool permissions (even not being allowed to arbitrarily install Ollama due to data leakage concerns) shows the immense responsibility of an engineer in real-world combat.

#### Hands-on technical exposure

- Was guided on how to approach the Credit Scoring problem for startups—a target group lacking traditional financial reports—through the seamless coordination of a Multi-Agent architecture.
- Grasped the standard product lifecycle deployment roadmap in an enterprise: From POC -> Internal testing -> SIT -> UAT -> Pilot up to Scale.

#### Leveraging modern tools

- Experienced the real-world **"Knowledge Transfer"** process, combining the power of LLMs with financial business knowledge.
- Expanded knowledge on enterprise-supporting frameworks like Bedrock Agent Core and Terraform to optimize packaging and infrastructure deployment.

#### Networking and discussions

- The event gave me the opportunity to network, ask questions, and understand the importance of comprehending **Stakeholder KPIs** to ensure smooth teamwork.

#### Lessons learned

- **"Numbers speak louder than words"**: Every technological solution proposed to superiors must be proven by actual numbers instead of empty promises.
- **Humans are always the final checkpoint**: No matter how smart AI gets, the designing engineer and the system approver must bear full responsibility (**Audit**) for the decisions made.
#### Some event photos

![event photo](/images/event2305.jpg)

> Overall, the event not only provided technical knowledge but also helped me reshape my thinking about application design, system modernization, and cross-team collaboration.
