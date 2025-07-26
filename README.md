# 🔐 Google OAuth Authentication App

This project demonstrates how to authenticate users using their **Google Account** via **OAuth 2.0**, with both frontend and backend integration. It's a secure, real-world example of how to implement Google Sign-In using **Node.js** as the backend.

---

## ✨ Features

- 🔑 Login with Google using OAuth 2.0
- 🛡️ Secure token handling and user session management
- 🌐 Backend authentication using Node.js and Google API
- ⚡ Fast and responsive interface
- 📦 Lightweight and easy to integrate into any app

---

## 🛠️ Tech Stack

- **Backend:** Node.js, Express.js  
- **Frontend:** HTML, CSS, JS (or React if applicable)  
- **Authentication:** Google OAuth 2.0  
- **Other:** dotenv, cookie-session, passport, passport-google-oauth20

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Golu-Guptha/google_authentication.git
cd google_authentication
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Create Google OAuth Credentials

1. Go to the [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project (or select an existing one)
3. Go to **APIs & Services > Credentials**
4. Click **Create Credentials > OAuth client ID**
5. Set:
   - Application type: **Web Application**
   - Authorized redirect URI: `http://localhost:5000/auth/google/callback`

6. Copy the **Client ID** and **Client Secret**

### 4. Configure Environment Variables

Create a `.env` file in the root directory:

```env
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
SESSION_SECRET=your_random_session_secret
```

### 5. Run the App

```bash
npm start
```

Visit: [http://localhost:5000](http://localhost:5000)

---

## 🔄 Flow Diagram

```text
User Clicks "Login with Google" →
Redirect to Google Consent Screen →
User Authenticates →
Google Redirects to Callback Route →
Token & Profile Received →
User is Authenticated and Session Stored
```

---

## 📁 Project Structure

```
google_authentication/
├── routes/
│   └── auth.js
├── config/
│   └── passport.js
├── .env
├── server.js
├── package.json
└── README.md
```

---

## 🔐 Security Notes

- All secrets are managed via environment variables.
- Passport.js handles secure token validation.
- Sessions are stored securely using `cookie-session`.

---

## 🌟 Future Improvements

- Add logout functionality
- Support for multiple OAuth providers (GitHub, Facebook, etc.)
- Store authenticated users in a database (MongoDB/PostgreSQL)
- Token refresh and expiry handling

---

## 🤝 Contributing

Contributions are welcome!  
Feel free to fork the repo, open issues, or submit pull requests.

---

## 📄 License

This project is licensed under the **MIT License**.

---

Made with ❤️ by **Golu Gupta**
