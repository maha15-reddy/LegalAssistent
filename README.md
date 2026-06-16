The AI-Powered Legal Assistant is a chatbot designed to help users find relevant Indian IPC sections and provide legal guidance on property disputes, criminal law, and other legal matters. It is implemented as a data science project and deployed as a web application using React, Django REST Framework, and Gemini API.

🚀 Features
User Authentication: Secure login using Bearer Token Authentication.
AI-Powered Legal Advice: Uses the Gemini API (gemini-pro model) to generate responses.
Search IPC Sections: Users can query legal issues and get relevant Indian Penal Code (IPC) sections.
Interactive Chatbot UI: Built with React and Tailwind CSS for a seamless experience.
Backend API: Developed using Django REST Framework (DRF).
Database Storage: Stores user information and queries securely.
🛠️ Tech Stack
Frontend:
React (for UI development)
Tailwind CSS (for styling)
Backend:(legal_assistant)
Django REST Framework (DRF) (for API development)
Gemini API (gemini-pro) (for AI-powered legal responses)
Authentication:
Bearer Token Authentication (Secure user authentication)
📂 Project Structure
AI-Powered-Legal-Assistant/
│── legal_assistant/                # Django REST Framework (Backend)
│   ├── api/                # API Endpoints
│   ├── models.py           # Database Models
│   ├── views.py            # API Logic
│   ├── serializers.py      # DRF Serializers
│   ├── urls.py             # API Routes
│   ├── settings.py         # Django Settings
│
│── frontend/               # React Frontend
│   ├── src/
│   │   ├── components/     # UI Components
│   │   ├── pages/          # Page Components
│   │   ├── App.js          # Main App File
│   │   ├── index.js        # Entry Point
│   ├── package.json        # React Dependencies
│
│── dataset/                # CSV file with IPC sections
│── README.md               # Project Documentation
🖥️ Installation Guide
🔹 Backend Setup (Django)
# Clone the repository
git clone https://github.com/your-repo/legal-assistant.git
cd legal-assistant/legal_assistant

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Start the backend server
python manage.py runserver
🔹 Frontend Setup (React)
cd ../frontend

# Install dependencies
npm install

# Start the frontend server
npm start
The frontend runs at http://localhost:3000/, and the backend at http://localhost:8000/.

🔗 API Endpoints
🔹 User Authentication
POST /api/login/ → Logs in user and returns Bearer token.
POST /api/register/ → Registers a new user.
🔹 Legal Queries
POST /api/legal-query/ → AI chatbot processes legal questions and returns relevant IPC sections.
GET /api/ipc-sections/ → Fetches all IPC sections from the database.
