# vibe-coding-2.0

HomeworkHelper KE 📚
HomeworkHelper KE is an AI-powered web application designed to assist students and parents with homework questions across various subjects. It provides instant answers, supports image uploads for questions, tracks user progress, and offers a credit-based system with premium upgrade options.

✨ Features
AI-Powered Question Answering: Get immediate answers to your homework questions using the Gemini AI model.

Image Upload Support: Upload photos of your homework problems for AI analysis and solutions.

User Authentication: Not fully working, but will work in the near future

Personalized Dashboard: View your credits, questions solved, monthly activity, and top subjects.

Question History: Keep track of your past questions and their AI-generated answers.

Credit System: Utilize a credit-based system for asking questions, with options to purchase more.

Subject Coverage: Support for various subjects including Mathematics, Life Sciences, Physical Sciences, Chemistry, Physics, History, Geography, and English.

Responsive Design: Optimized for seamless use across different devices (mobile, tablet, desktop).

🚀 Technologies Used
Frontend: HTML, CSS, JavaScript

Framework: React (via CDN for simplicity)

Styling: Tailwind CSS (via CDN for development)

Transpilation: Babel (for JSX in the browser)

Backend & Database: Firebase (Authentication and Firestore for data storage)

AI Integration: Google Gemini API (using gemini-2.0-flash model)

Deployment: Netlify (as indicated by the live URL)

🛠️ Getting Started
To run this project locally for development, follow these steps:

Prerequisites
A modern web browser.

A Firebase Project with Firestore and Authentication enabled.

A Google Cloud Project with access to the Gemini API.

Local Setup
Clone the repository:

git clone <repository-url>
cd homework-helper-ke

(Replace <repository-url> with the actual URL of your Git repository.)

Firebase Configuration:
This application is designed to run within an environment that injects Firebase configuration variables (__app_id, __firebase_config, __initial_auth_token). For local development outside such an environment, you would typically:

Go to your Firebase project settings in the Firebase Console.

Find your project's web app configuration.

Replace the placeholder values for firebaseConfig and potentially __app_id in the <script type="module"> block of index.html with your actual Firebase configuration.

For authentication, signInWithCustomToken is used, which relies on a token provided by the environment. For standalone local testing, you might need to adjust the initial authentication flow (e.g., remove signInWithCustomToken and rely solely on email/password or anonymous sign-in).

Gemini API Key:

Obtain an API key for the Google Gemini API from the Google AI Studio or Google Cloud Console.

Locate the apiKey variable in the ChatInterface component's handleSendMessage function (index.html, around line 350).

Replace the placeholder AIzaSyCoHNFBHZwRJDr_qt3I0d-Y3gVGN1GaIaU with your actual Gemini API key.

Note: Hardcoding API keys directly in client-side code is not recommended for production environments due to security risks. For a production deployment, consider using a backend proxy or serverless function to securely handle API calls.

Run the Application:
Since this is a single HTML file with CDN dependencies, you can simply open index.html in your web browser.

# From your project directory
open index.html # On macOS
start index.html # On Windows
xdg-open index.html # On Linux

💡 Usage
Access the App: Open index.html in your browser or navigate to the deployed Netlify URL.

Login/Sign Up: Use the "Login / Sign Up" button in the top right to create an account or log in with your email and password.

Ask a New Question: Click the "New Question" button (either on the dashboard or in the top navigation).

Type or Upload: Enter your homework question in the text input field or click the camera icon to upload an image of your question.

Get Answers: Click "Send" to get an AI-generated answer.

Dashboard: Return to the dashboard to view your stats, recent questions, and account status.

🚧 Future Enhancements
The following features are planned for future development:

Full History View: A dedicated page to view all past questions and answers.

Buy Credits Functionality: Implementation of a secure payment gateway for purchasing additional credits.

Explore All Subjects: An expanded section to browse and filter questions by all available subjects.

Question Details View: Ability to click on a recent question to see its full details and conversation.

Advanced Analytics: More detailed insights into user activity and learning patterns.

Secure API Key Handling: Move the Gemini API key to a more secure server-side setup for production.

⚠️ Known Issues
Tailwind CSS CDN Warning: The current setup uses the Tailwind CSS CDN, which is not recommended for production due to performance and optimization limitations. For production, a build process (e.g., using PostCSS or Tailwind CLI) should be implemented to purge unused CSS.

Hardcoded Gemini API Key: The Gemini API key is currently hardcoded in the client-side JavaScript. This is a security risk for production applications.

🤝 Contributing
Contributions are welcome! If you have suggestions or want to contribute, please feel free to fork the repository and submit pull requests.
