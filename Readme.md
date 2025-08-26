# 📞 AWS Connect IVR System  

## 📌 Overview  
This project demonstrates how to build an **Interactive Voice Response (IVR)** system using **Amazon Connect**.  
The IVR allows customers to interact with your call center through automated menus (e.g., *Press 1 for Sales, Press 2 for Support*) and routes calls to the appropriate agents or queues.  

AWS Connect helps businesses automate call distribution, monitor real-time metrics, and integrate with other AWS services like **Lex** and **S3**.  

---

## 🚀 Features  

### ✅ Automated Call Distribution  
Distribute inbound calls across available agents automatically.  
- Example: If your team receives **100 calls per day**, AWS Connect helps balance the load among agents.  

### ✅ Interactive Voice Response (IVR)  
Every company, from small shops to large enterprises, needs IVR.  
Example menu:  
- *Press 1 for Sales*  
- *Press 2 for Support*  
- *Press 3 to talk to an Agent*  

### ✅ Real-Time Metrics & Analytics  
- Track call origin (location).  
- Measure average call handling time.  
- Monitor queue wait times.  

### ✅ Integration with Other AWS Services  
- Connect with **Amazon Lex** (chatbots).  
- Store call recordings in **Amazon S3**.  
- Analyze calls with **AWS Comprehend & Transcribe**.  

---

## 👥 Users & Agents  

- You can create multiple users (agents).  
- Example:  
  - **Sales Team**: 2 agents handling sales calls.  
  - **Support Team**: 4 agents handling support calls.  

Each agent is a **user** in AWS Connect and logs in via the **Agent Portal**.  

---

## ☎️ Phone Number  
- A phone number is required so customers can call your contact center.  
- Example: *BestBuy claims a phone number from AWS Connect so customers can call directly.*  

---

## 🎧 Queues  
Queues hold customer calls until an agent is available.  
- Example: If 100 people call the Sales team but only 2 agents are available, the rest wait in a **queue**.  

---

## 🕒 Hours of Operation  
Define the time when agents are available.  
- Example: *Sales team is available 9 AM – 6 PM, Support team 24/7.*  

---

## 🔄 Flows (IVR Logic)  
**Flow Example:**  
ENTRY → Play Prompt → Get Customer Input → Set Working Queue → Assign Agent → Disconnect


### Example: BestBuy IVR Flow  
1. Caller dials BestBuy’s phone number.  
2. IVR plays: *“Thank you for calling BestBuy. Press 1 for Sales, Press 2 for Support.”*  
3. If the caller presses **1**, they go to the **Sales Queue**.  
4. If the caller presses **2**, they go to the **Support Queue**.  
5. If no input → prompt repeats.  
6. If timeout → call disconnects with error prompt.  

---

## 🖥️ AWS Connect Portals  

- **Admin Portal**:  
  - Manage users (agents).  
  - Configure IVR flows.  
  - Assign phone numbers.  

- **Agent Portal**:  
  - Where agents log in and answer calls.  

---

## 🛠️ Steps to Create IVR in AWS Connect  

1. **Claim a phone number**.  
2. **Create users/agents** (e.g., Sales team, Support team).  
3. **Design the flow**:  
   - Play prompt (*Welcome message*).  
   - Get customer input (e.g., Press 1, Press 2).  
   - Set working queue.  
   - Assign agent.  
   - Disconnect.  

---

## 📊 Real-Life Example  

**Company: BestBuy**  
- Phone Number: `+1-800-123-4567`  
- Agents:  
  - Sales → John  
  - Support → Tom  
- IVR Flow:  
  1. *“Welcome to BestBuy!”*  
  2. *Press 1 for Sales (John)*  
  3. *Press 2 for Support (Tom)*  
  4. Calls distributed automatically.  
  5. If queue is full → customer waits until agent is available.  

---
## 📎 References

[ AWS IVR Best Practices](https://aws.amazon.com/connect/resources/)

[Getting Started with Amazon Connect](https://aws.amazon.com/connect/getting-started/)

[AWS Connect Documentation](https://docs.aws.amazon.com/connect/)

## 📌 Architecture Diagram  

```mermaid
flowchart TD
    A[Customer Calls Number] --> B[Play Prompt: Welcome Message]
    B --> C{Customer Input}
    C -->|Press 1| D[Sales Queue → Sales Agent]
    C -->|Press 2| E[Support Queue → Support Agent]
    C -->|No Input| F[Repeat Prompt]
    F -->|Timeout| G[Disconnect]


