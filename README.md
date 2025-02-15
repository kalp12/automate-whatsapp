# The Red Velvet Bakery WhatsApp Bot 🎂

A WhatsApp chatbot for handling customer interactions and cake orders. Built with Flask, Twilio, and MongoDB.

---

## 1. Features ✨
- **Customer Support Options**:  
  Get contact info and working hours.
- **Cake Order System**:  
  Choose from 9 cake options and provide address.
- **Order Tracking**:  
  Stores all orders in MongoDB with timestamps.
- **Conversation History**:  
  Saves complete chat history for every user.
- **State Management**:  
  Maintains user session states (main menu/ordering/address).

---

## 2. Prerequisites 📋
Before running the bot, ensure you have the following:
- **Python 3.7+**: Install Python from [python.org](https://www.python.org/).
- **MongoDB Atlas Account**: Create a free account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).
- **Twilio Account**: Sign up at [Twilio](https://www.twilio.com/) and enable WhatsApp Sandbox.
- **Heroku Account** (for deployment): Sign up at [Heroku](https://www.heroku.com/).
- **Git**: Install Git from [git-scm.com](https://git-scm.com/).

---

## 3. Setup & Installation 🛠️

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/bakery-bot.git
cd bakery-bot
```
### Step 2: Install Dependencies
Install the required Python packages:

bash
Copy
pip install -r requirements.txt
### Step 3: Set Up Environment Variables
Create a .env file in the root directory and add the following:

env
Copy
MONGODB_URI="mongodb+srv://<username>:<password>@cluster0.tzle5.mongodb.net/myFirstDatabase?retryWrites=true&w=majority"
TWILIO_AUTH_TOKEN="your_twilio_auth_token"
Replace <username>, <password>, and your_twilio_auth_token with your actual credentials.

## 4. Configuration 🔧
Twilio Setup
Go to the Twilio Console.

Enable WhatsApp Sandbox.

Set the Webhook URL to your server URL (e.g., https://your-heroku-app.herokuapp.com/).

MongoDB Setup
Create a database named bakery.

Create two collections: users and orders.

## 5. Deployment 🚀
Step 1: Heroku CLI Setup
Install the Heroku CLI: Heroku CLI Installation.

Log in to Heroku:

bash
Copy
heroku login
Create a new Heroku app:

bash
Copy
heroku create your-app-name
Set environment variables on Heroku:

bash
Copy
heroku config:set MONGODB_URI=$MONGODB_URI TWILIO_AUTH_TOKEN=$TWILIO_AUTH_TOKEN
Step 2: Deploy the Application
Push your code to Heroku:

bash
Copy
git push heroku main
## 6. Bot Workflow 💬
Main Menu
When a user messages the bot, they see:

Copy
1 - Contact Info
2 - Start Order
3 - Working Hours
4 - Store Address
Ordering System
User selects a cake (options 1-9).

Bot prompts for the delivery address.

Order is confirmed and stored in MongoDB.

Post-Order
User is returned to the main menu.

Order details are saved with a timestamp.

## 7. Project Structure 📂
    .
      ├── app.py              # Main application logic
      ├── Procfile            # Heroku deployment config
      ├── requirements.txt    # Python dependencies
      └── README.md           # Documentation
## 8. Future Improvements 🔮
Add payment integration.

Implement order status updates.

Send menu images via sms.

Add multi-language support.

Build an admin dashboard for order management.

## Happy Ordering! 🧁🍰
