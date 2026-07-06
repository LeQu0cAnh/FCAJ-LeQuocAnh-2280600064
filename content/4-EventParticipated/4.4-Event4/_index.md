---
title: "FCAJ Community Day: Data Driven, AI Risen"
date: 2026-06-27
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

# Summary Report: "FCAJ Community Day: Data Driven, AI Risen"

### Event Objectives

- Update on the trending impact of AI on the job market, especially for Developer and Cloud Engineer positions.
- Provide deep insights into AI's impact on the labor market, Multi-agent architectures, DevOps Agents, Amazon Q, etc.
- Dive into Generative AI (GenAI) application solutions in enterprises, such as: Voice AI, Agentic Platforms for Cloud infrastructure, DevOps AI Agents, HR process automation, and system security standards.

### Speakers

- **Steve Tran** - Founder/CTO of CloudThinker
- **Trung Vu** - CEO Revve AI
- **Kiet Tran** - AI Engineer | AWS Student Builder Group
- **Danh Hoang Hieu Nghi** - AI Engineer Renova Cloud
- **Phan Kim Bao** - Cloud Engineer
- **Nguyen Minh Nguyen** - Cloud Engineer
- **Tran Truong** - PM, AI & MULTI CLOUD SOLUTIONS of Noventiq Vietnam
- **Dang Cao Minh Anh** - Intern Solution Sales of Noventiq Vietnam
- **Nguyen Duc Toan** - AWS Security Builder

### Key Highlights

#### Reshaping the Job Market and Agentic Platform for Cloud

- **Market shift**: AI tools are accelerating coding speed, causing companies to pause mass hiring of traditional Developers and focus on finding Senior personnel or those with excellent AI utilization skills.
- **Cloud operation problem**: As enterprise systems grow, complexity increases, requiring AI tools not only to assist in coding but also to securely manage and monitor infrastructure.
- **Solution**: Use Multi-Agent systems and Agentic Platforms to assist humans in rapid incident response, security assessments (automated pentesting), and cost optimization (FinOps). However, AI at the production layer requires extremely strict access control (approvals) to avoid risks.

#### Architecture and Voice AI Optimization for the Vietnamese Market

Mr. Trung Vu's presentation provided a practical and profound perspective on deploying voice AI switchboards for major banks in Vietnam, thoroughly resolving language and business barriers.

- **Why not use Speech-to-Speech?** Currently, most Speech-to-Speech models primarily support English and lack resources for Vietnamese.
- **Practical solution**: Use a three-step architecture: Speech-to-Text (voice recognition) -> LLM (text processing) -> Text-to-Speech (text to voice). This architecture helps enterprises strictly control AI output content, avoid "hallucinations," and easily execute Tool Calling (e.g., locking a bank card upon request).
- **Latency optimization**: For Voice AI to respond naturally, the entire process of recognition, text processing, and voice output must be executed through a continuous Streaming mechanism, helping the AI catch the voice and reply almost instantly without waiting to process the entire sentence.
- **Handling specific Vietnamese characteristics**: Vietnamese requires standard pronouns (anh/chị). AI needs to be trained to listen to the voice and automatically recognize the customer's gender for accurate addressing. Furthermore, AI must understand when the customer pauses to think (e.g., recalling a phone number) instead of interrupting. The bot must also automatically stay silent when interrupted by the customer.
- **Applying regional accents**: The training data is supplemented with 10-20% regional accents. This is especially effective in debt collection scenarios, as a bot with a regional accent attracts the listener's attention more than a standard accent.
- **Human Handover**: The system allows humans to monitor calls, and the AI can automatically and naturally transfer (pass) the call to a real agent when scolded by the customer or when it cannot handle the request itself.

#### Operational Automation with DevOps AI Agent

- **Operations engineer's problem**: Logs and telemetry are fragmented across multiple places, causing context loss and prolonging Mean Time To Recovery (MTTR).
- **Solution**: DevOps AI Agent utilizes Context Learning to draw out the system Topology, automatically triggers upon error alerts, collects logs, hypothesizes, and provides the Root Cause.
- **Safety boundaries**: AI only provides a Mitigation Plan but does not execute it automatically. The decision to run the remediation script always depends on human approval.

#### Optimizing HR Processes with Amazon Q

- **Challenge**: HR spends a lot of time manually screening CVs, easily missing talents, and often evaluates based on intuition without a standard framework.
- **AI Application**: Amazon Q acts as a smart assistant to help build candidate evaluation skills. The system can automatically read CV files, cross-reference with the Job Description (JD), automatically score skills, and provide clear recommendations on whether to accept or reject candidates.
- **Flexible integration**: Allows secure extraction from enterprise document sources (OneDrive, SharePoint, Google Workspace, GitHub) without being restricted to a single ecosystem.

#### Securing MCP (Model Context Protocol) Server Connections

- **Risk**: When AI Agents call third-party tools (MCP Servers) over the public Internet, the system easily becomes a target for DOS attacks or data theft via Man-in-the-middle.
- **Security architecture**: Place the MCP Server in a Private Subnet, use VPC Connections (internal routing) along with an Application Load Balancer (ALB) for TLS encryption. All query data between the AI and MCP will flow internally, not exposed publicly, adhering to strict enterprise security standards.

### Key Takeaways

#### Design Mindset

- **AI is a supporting tool, not a complete human replacement**: Whether it's a Cloud infrastructure management application or Voice AI for a switchboard, core systems still require highly skilled personnel for action approval and monitoring.
- **Customer-Centric in AI design**: Building Voice AI is not just piecing technologies together, but understanding customer psychology (addressing norms, interruption habits, annoyance when interrupted by AI) to fine-tune the model.
- **Readiness for process changes**: When applying Agentic systems, enterprises may have to change up to 50% of their operational processes compared to using traditional personnel.

#### Technical Architecture

- **Voice Pipeline Architecture**: Breaking down into Speech-to-Text -> LLM -> Text-to-Speech along with a Streaming architecture is the key to deploying low-latency Vietnamese Voice bots with strictly controlled outputs.
- **Security-First Architecture**: Any connection from AI to business systems (MCP) must go through private Endpoints (VPC Connection, Private DNS) to protect information security.
- **Custom Agent Skills**: You can custom-design features for AI Agents based on MD (Markdown) files describing tasks, clearly defining execution steps to serve specific departments (e.g., HR Talent Review).

#### Applying to Work

- **Deploy internal Voice bots**: Apply the STT-LLM-TTS processing model to build automated internal support bots in Vietnamese, establishing additional context analyzers (recognizing latency, silence) for smoother communication.
- **Optimize Troubleshooting**: Pilot the DevOps AI Agent by linking it with CloudWatch/Datadog to reduce the manual effort of combing through logs when system incidents occur.
- **Build Custom AI Assistants for the team**: Use Amazon Q (or equivalent AI platforms) to create automated CV scoring criteria, thereby helping HR and technical teams shorten candidate screening time.
- **Review security architecture**: Ensure all API connections from LLMs to internal tools/databases are established via a Private VPC, rejecting direct public API exposure to the Internet.

### Event Experience

Attending the **“FCAJ Community Day: Data Driven, AI Risen”** workshop was a highly rewarding experience, giving me a comprehensive view of how to modernize applications and databases using modern methods and tools. Key experiences included:

#### Learning from highly skilled speakers

- Mr. Trung Vu's sharing session truly expanded my mindset on how to build practical **Voice AI** products. Delving into details like gender distinction, understanding pauses when reading phone numbers, and applying regional accents showed the difference between a "demo" and a real-world "Enterprise" product.

#### Hands-on technical exposure

- Watched a live demo of a Voice Agent querying MacBook information and a simulated DDoS attack demo to see how the DevOps AI Agent automatically extracted the Root Cause and provided a remediation plan in just a few minutes.
- Witnessed Amazon Q's "work comprehension" capability as it automatically analyzed Vietnamese CVs, providing accurate pros/cons assessments.

#### Leveraging modern tools

- Broadened my vision on Model Context Protocol (MCP) and how to establish secure connections via VPC.
- Learned the concept of "Agent Space" – a restricted permission space for AI to safely learn system context (Topology) without touching restricted data.

#### Lessons learned

- **Deeply understand the context instead of just chasing technology**: A good AI model is not about how massive or modern it is, but how it solves the specific language and business problems of the enterprise (like how Revve AI handles Vietnamese).
- **Always keep the Human-in-the-loop loop**: Even though AI has extremely powerful automation capabilities, from DevOps to HR, humans must remain the final decision-makers to ensure safety and transparency.

#### Some event photos

![event photo](/images/event2706.jpg)

> Overall, the event not only provided technical knowledge but also helped me reshape my thinking about application design, system modernization, and cross-team collaboration.
