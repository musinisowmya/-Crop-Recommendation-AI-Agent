 Crop Recommendation AI Agent
An AI-powered assistant built using n8n, Cohere Chat Model, and Simple Memory to recommend crops based on soil type, climate, and market demand — all without writing a single line of code!

📌 Features
Asks farmers for details one question at a time:

Soil type

Temperature (°C)

Rainfall (mm)

Season or month

Location

Market preference

Remembers answers using the Simple Memory module (no repeating questions).

Suggests 3–5 crops best suited for the given conditions.

Provides:

Quick summary

Planting window & irrigation tips

Short market advice

🛠 Tools Used
n8n — Workflow automation (No-Code)

Cohere Chat Model — AI language model

Simple Memory — Context persistence in n8n

📂 Workflow Screenshot

(Replace with your actual screenshot)

⚡ How It Works
Trigger: Chat message received in n8n.

AI Agent: Uses Cohere Chat Model + Simple Memory to ask and store answers.

Memory: Stores each response until all required inputs are collected.

Final Output: AI recommends crops with short, practical advice.

🚀 Getting Started
1. Prerequisites
n8n Desktop or n8n Cloud

Cohere API key (get it from Cohere)

2. Steps to Build
Create a new workflow in n8n.

Add When Chat Message Received trigger.

Add AI Agent node and paste the following prompt:

vbnet
Copy
Edit
You are a helpful crop recommendation assistant for farmers.

Goal: Recommend 3–5 crops that best match the user's conditions.

Ask exactly one question at a time in this order:
1. soil_type
2. temperature_c
3. rainfall_mm
4. season
5. location
6. market_preference

After collecting all, respond with:
- Quick summary
- Bullet list of recommended crops with short reasons
- Planting window and irrigation note
- Simple market tip

Rules:
- If the answer is already stored in memory, skip that question.
- Never repeat the same question unless unclear.
- Keep answers short and practical.
Connect the Cohere Chat Model node to the Chat Model slot.

Add Simple Memory node and connect it to the Memory slot.

Deploy your workflow and start chatting!

🎯 Use Cases
Farmer crop planning

Agricultural startup advisory tools
