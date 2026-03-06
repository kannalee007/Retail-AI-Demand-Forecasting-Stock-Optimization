📈 RetailAI – Demand Forecasting & Stock Optimization System
A modern, full-stack web application designed for retail store managers to analyze historical sales data, predict future product demand, optimize inventory, and receive actionable insights from an AI-powered retail assistant. Built as a hackathon project, this system operates entirely locally using JSON storage, making it incredibly fast and easy to deploy.


🌟 Features

🔐 Simple Authentication: Secure dashboard access using local session state.

📊 Inventory Dashboard: High-level metrics including Total Products, Low Stock Items, Predicted Demand, and Stockout Risks.

📦 Product Management: Full CRUD capabilities to add, edit, or delete inventory records dynamically.

📁 CSV Data Ingestion: Upload historical sales data directly via CSV (parsed locally using PapaParse).

📈 Sales Analytics: Visualized historical trends and top-selling products using Recharts.

🔮 Demand Forecasting Engine: Built-in algorithm to calculate expected future demand and generate smart reorder recommendations based on current stock.

🧠 AI Insight Service: Generates plain-text, contextual insights explaining why a product needs restocking.

💬 AI Chat Assistant: An interactive chat interface for store managers to ask questions about their inventory and get instant guidance.


🛠️ Tech Stack
Framework: Next.js 14+ (App Router)
Language: TypeScript
Styling: Tailwind CSS
Charts: Recharts
CSV Parsing: PapaParse
Database/Storage: Local JSON file system (/data directory)


🚀 Getting Started
Follow these instructions to get the project up and running on your local machine.

Prerequisites
Node.js (v18 or higher recommended)
npm or yarn
Installation
Clone the repository
Bash
git clone https://github.com/yourusername/retail-ai-dashboard.git
cd retail-ai-dashboard
Install dependencies
Bash
npm install
Run the development server
Bash
npm run dev
Open the application
Navigate to http://localhost:3000 in your browser.



🔑 Default Credentials
To access the protected dashboard, use the following demo credentials:
Email: admin@retailai.com
Password: admin123
📂 Project Structure
Plaintext
├── src/
│   ├── app/                 # Next.js App Router pages (login, dashboard, api routes)
│   ├── components/          # Reusable UI components (DashboardCards, ProductTable, etc.)
│   └── ai/                  # AI logic and mock services (forecast, insight, chat)
├── data/                    # Local JSON storage acting as the database
│   ├── products.json        # Inventory and product details
│   └── sales_data.json      # Parsed historical sales records
├── public/                  # Static assets
├── tailwind.config.ts       # Tailwind CSS configuration
└── package.json             # Project dependencies


💻 Expected Demo Flow


Login: Authenticate using the default admin credentials.
Upload Sales CSV: Navigate to the data ingestion section and upload a CSV file (date,product_id,units_sold).
View Forecasts: Check the dashboard for automatic demand predictions and stockout risk alerts.
Reorder Recommendations: Look at the product table to see dynamically calculated reorder quantities.
AI Assistant: Open the chat interface to ask questions about inventory optimization.


🔌 API Endpoints Reference
This project utilizes Next.js Server-side API routes to handle logic:
POST /api/forecast: Accepts historical sales arrays and returns calculated demand and reorder quantities.
POST /api/ai-insight: Accepts product details and returns a contextual natural language insight.
POST /api/chat: Processes user queries and returns conversational AI responses.


🔮 Future Improvements (Post-Hackathon)


Integrate a real database (PostgreSQL / MongoDB) instead of local JSON storage.
Connect the AI Chat and Insight endpoints to real LLM APIs (like OpenAI GPT-4 or Google Gemini).
Implement advanced Machine Learning models (e.g., ARIMA, Prophet) for demand forecasting.
Add multi-store support and advanced user role management.
